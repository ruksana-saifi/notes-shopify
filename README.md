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




----To create an app to shopify we need to install these things --------------
1. shopify cli - npm install -g @shopify/cli@latest
2. node.js
3. Git  install git 
4. shopify app init
5. After installation shopify app follow termial guide and then
6. go to the yourapp/app/
7. here you can add new pages and modify the design usign shopify polaris


------- when we need to connect shopify to github ---------------

cd path/to/your/project
shopify theme list
shopify theme pull

cd path/to/your/local/theme
git init
git remote add origin <repository-url>
git add .
git commit -m "Initial commit of Shopify theme"
git push -u origin master  # or git push -u origin main


