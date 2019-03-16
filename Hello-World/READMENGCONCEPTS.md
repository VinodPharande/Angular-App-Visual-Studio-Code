# ngConcepts



## angular.json
An Angular Application Environment is JSON configuration information that tells the build system which files to change when you use ng build and ng serve . Let's say you have a back end REST API deployed on a server that provides services to your Angular application.

Introducing Configurations
By default the Angular CLI creates a src/environments folder with two environment files in it: environment.ts and environment.prod.ts.

These files are referenced in our angular.json file.

We need to tell angular.json about our new environment file. In the build element there is a configurations object.

Refer: https://blog.angularindepth.com/becoming-an-angular-environmentalist-45a48f7c20d8



## tsconfig.json
A tsconfig.json file can inherit configurations from another file using the extends property. The extends is a top-level property in tsconfig.json (alongside compilerOptions , files , include , and exclude ). extends ' value is a string containing a path to another configuration file to inherit from.

Overview
The presence of a tsconfig.json file in a directory indicates that the directory is the root of a TypeScript project. The tsconfig.json file specifies the root files and the compiler options required to compile the project. A project is compiled in one of the following ways:

Using tsconfig.json
By invoking tsc with no input files, in which case the compiler searches for the tsconfig.json file starting in the current directory and continuing up the parent directory chain.
By invoking tsc with no input files and a --project (or just -p) command line option that specifies the path of a directory containing a tsconfig.json file, or a path to a valid .json file containing the configurations.

Refer: https://www.typescriptlang.org/docs/handbook/tsconfig-json.html



## tslint.json
TSLint Configuration. When using the CLI or many third-party tools, a file named tslint.json or tslint.yaml is used to configure which rules get run and each of their options.

Installation
Local (in your project’s working directory):

npm install tslint typescript --save-dev
# or
yarn add tslint typescript --dev
Global:

npm install tslint typescript -g
# or
yarn global add tslint typescript
Peer dependencies
The typescript package is a peer dependency of TSLint. This allows you to update the compiler independently from the linter. This also means that tslint will have to use the same version of tsc which is used to actually compile your sources.

Although the peer dependency allows installing the latest nightly releases of typescript@next, be aware that these might include breaking changes that cause the linter to malfunction.

Refer: https://palantir.github.io/tslint/usage/cli/



## package.json
All npm packages contain a file, usually in the project root, called package.json - this file holds various metadata relevant to the project. This file is used to give information to npm that allows it to identify the project as well as handle the project's dependencies. It can also contain other metadata such as a project description, the version of the project in a particular distribution, license information, even configuration data - all of which can be vital to both npm and to the end users of the package. The package.json file is normally located at the root directory of a Node.js project.

Refer: https://docs.nodejitsu.com/articles/getting-started/npm/what-is-the-file-package-json/



## BrowserModule from '@angular/platform-browser'
BrowserModule provides services that are essential to launch and run a browser app. BrowserModule also re-exports CommonModule from @angular/common , which means that components in the AppModule module also have access to the Angular directives every app needs, such as NgIf and NgFor .

Refer: https://angular.io/guide/ngmodule-faq



## bootstrap in @NgModule
The root component that Angular creates and inserts into the index.html host web page.

Refer: https://angular.io/guide/bootstrapping



## AppRoutingModule from '@angular/router'
In Angular, the best practice is to load and configure the router in a separate, top-level module that is dedicated to routing and imported by the root AppModule . By convention, the module class name is AppRoutingModule and it belongs in the app-routing.module.ts in the src/app folder. The Angular Router enables navigation from one view to the next as users perform application tasks.

Refer: https://angular.io/guide/router



