#### For ES6/ES2015, you can directly import json file:

    // example.json file
    {
        "name": "testing"
    }


    // ES6/ES2015
    import * as data from './example.json';
    
    //In node.js
    const data = require('./example.json');
