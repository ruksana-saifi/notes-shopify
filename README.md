# notes-shopify

api
https://apikey:apitoken@storename/admin/api/version/orders.json


to use Admin api in node js ======
1. install node.js
2. intall npm package trough command:  npm install -g package-name
3. inatall request package trough command: npm i request
4. create page and paste this code: 

let request = require('request');

let apikey = '0e4972554e756862b111428815775569';
let pass = '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';
// let endpoint = '';

let options = {
 'method': 'GET',
 'url': `https://${apikey}:${pass}@studyheart.myshopify.com/admin/api/2024-07/collections/470484517181.json`,
 'headers': {
   'Content-Type': 'application/json'
 }
};

request(options, function(error, response){
 if(error) throw new Error(error);
 console.log(response.body);
});
