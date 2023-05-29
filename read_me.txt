npm init --yes
npm install express dotenv
npm install --save-dev nodemon ts-node typescript @types/express @types/node

    "dev": "nodemon ./src/main.ts",
        "start": "node ./dist/app.js",
        "build": "tsc",
        "lint-fix": "eslint --ignore-path .eslintignore . --fix",
        "format": "prettier --write .",
        "prepare": "husky install"

npx tsc --init
--rootDir
--moduleResolution
--outDir

==> tsconfig.json{compiler option muni}(
    "include":["./src"]
  }
)

run build after this for dist folder

//installing eslint and prettier
npm install --save-dev eslint eslint-config-prettier prettier 

after installing we get the file eslintrc.json
(some modifications at eslintrc.json)
-->"root":true (below parser)
-->   //modification of parser options
           "parserOptions": {
        "project" : true,
        "tsconfigRootDir" : "_dirname"
    },               



after that ,  build a file .prettierrc.json
-->{
    "trailingComma": "es5",
    "tabWidth": 4,
    "semi": false,
    "singleQuote": true
}

create an .eslintignore file and add the following (for now)
--> *.cjs
--> *.js
node_modules
dist

Set up the folder named .vscode and create a settings.json file inside it.
Add the following content
{
    "editor.codeAcrionsOnSave": {
        "source.fixAll.esling": true
    },
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.formatOnSave": true
}



npm install --save-dev lint-staged
npm install husky --save-dev
npm run prepare

npx husky add .husky/pre-commit "npm test"

git add .husky/pre-commit

husky vitra pre-commit xa, tya test lai hatayera lint-staged.

Package.json ko end ma add garne
(
  "lint-staged":{
    "*.ts":[
      "npm run format",
      "npm run lint-fix"
    ]
  }
)
git commit -m "Keep calm and commit"
# `npm test` will run

cros is used for integration


 --> install cros

 -->  npm i --save-dev @types/cors
