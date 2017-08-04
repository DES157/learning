# Variables


https://www.sitepoint.com/joys-block-scoping-es6/


ES6 introduced `let` and `const`, both of which have block scope, and the latter cannot be re-assigned or redeclared.

Current best practice is to use const by default, let if you need to rebind, or var to indicate legacy code.


`=== undefined` to test for undefined
`== undefined` test for undefined or null (they are abstractly equal)
