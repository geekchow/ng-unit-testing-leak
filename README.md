# ng-unit-testing-leak
Demo of Angular unit testing memory leaks
-------------------
uncomment the lines in heavyLoad-directive.spec.js
<pre>
  // define multiple suits with the same definition just for showcase
  /* TODO: uncomment this if you want to see the memory leaks
  for (var i = 0; i < 1000; i += 1) {
    describe('heavyLoad directive #' + i, testDefinition);
  }
  */
</pre>
The memeory leaks will show up.
