## Instructions for Mozilla reviewers

I have the source code in the vue and js files. With the command `npm run build` you create a build on pure js which is located in the dist folder. The `npm run build:prod` command will create the same build in the same folder, only the files will be minimized. The `npm run build-zip` command will create 2 zip archives in the `dist-zip` folder. The file and with the name `simple-tab-groups@drive4ik-v3.3-dev.zip` has the source code - I upload it with each release.
The file `simple-tab-groups@drive4ik-v3.3-prod.zip` has minimized code from the command `npm run build:prod`, which actually gets into the resulting XPI file.
All these commands and their execution are described in the `package.json` file.
How the build is going and with what settings you can also see in the file `webpack.config.js`
There is also a `remove-evals.js` script that removes the eval code from vue when creating a build.

```bash
$ npm install
$ npm run build-zip
```

If you need the build without minimization code you need to run the command
```bash
$ npm install
$ npm run build
```
This code will be located in the `dist` folder.