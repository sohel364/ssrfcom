Step by Step Process to write OWN NPM Module

Configure NPM :

npm set init.author.name "Mahmudul Hasan"
npm set init.author.email "ma.hasan@samsung.com"
npm set init.author.url "samsung.net"
npm adduser
Create/Clone git Repository 
1. Create a git repository
2. Clone it in your desired location 
as follows :
	git clone git@github.com:gitusername/project.git
	cd project
Then Execute :
 	npm init
(This command will guide you through the process of generating the “package.json” file by QA[question and answer]
Let's do the coding :
1. Create index.js file as it's my starting point file for the module.
	Example File :
		exports.WhatAreyou=function(){
			return "Hello i am your module";	
		};

2.  Now to test the module from javascript file. Let's write a test.js file. I did this for example
		var req = require("./index.js");
		console.log(req.WhatAreyou());

3. Run the test file from node as
		node test.js
	It should show "Hello i am your module"

Now the module is ready . Let's commit it to git . Add tag for version and commit 
		git tag 0.1.0
		git push origin master –tags
4. Now we can install from git as :

npm install git://github.com/you/your_project.git
npm install git://github.com/you/your_project.git#0.1.0

Check in the list of modules. It's Done !
