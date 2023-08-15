INSTALL

To include jQuery in Node, first install with npm.

npm install jquery
For jQuery to work in Node, a window with a document is required. Since no such window exists natively in Node, one can be mocked by tools such as jsdom. This can be useful for testing purposes.

const { JSDOM } = require( "jsdom" );
const { window } = new JSDOM( "" );
const $ = require( "jquery" )( window );
