# ng-unit-testing-leak
Demo of Angular unit testing memory leaks
-------------------
##1. set up the project
<pre>
npm install 
bower install
npm i karma-cli -g
</pre>

##2. start unit test case.
<pre>
karma start karma.conf.js
</pre>

##3. observer the memory usage of phantomjs process.
the usage of memory is stable at 120Mb approximable.

##4. uncomment the lines in heavyLoad-directive.spec.js
<pre>
  // define multiple suits with the same definition just for showcase
  /* TODO: uncomment this if you want to see the memory leaks
  for (var i = 0; i < 2000; i += 1) {
    describe('heavyLoad directive #' + i, testDefinition);
  }
  */
</pre>

##5. start unit test case.
<pre>
karma start karma.conf.js
</pre>

##6. observer the memory usage of phantomjs process.
the usage of memory is climbing to 800Mb.
The memeory leaks show up.
