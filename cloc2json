#!/usr/bin/env node

var csv         = require("csv-parser"),
    fs          = require("fs");
    
var files = [];

fs.createReadStream(process.argv[2])
  .pipe(csv())
  .on('data', function(data) {
    files.push(data);
  })
  .on('end', function() {
      console.log(JSON.stringify(createJson(files)));
  })
  
function createJson(contents) {
  var output = [];
  files.forEach(function(file) {
      output.push({lines: parseInt(file.code, 10), language: file.language, name: file.filename});
  });
  
  return output;
}