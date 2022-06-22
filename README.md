# Angular relative/absolute urls Test

#### Problem:

How to consistently use assets when building an angular app with base href?

For building and developing the site we have to specify assets in the angular config to provide them.
Assets are handled differently depending if the are used in styles or templates.


Assets in templates are not processed, they only get copied at build time.
Assets used in styles are processed depending on the url:

- if the url starts with [`/`](https://github.com/angular/angular-cli/blob/14.0.x/packages/angular_devkit/build_angular/src/webpack/plugins/postcss-cli-resources.ts#L73) or [`^`](https://github.com/angular/angular-cli/blob/14.0.x/packages/angular_devkit/build_angular/src/webpack/plugins/postcss-cli-resources.ts#L79) the assets are processed.
- For other urls assets get processed (copied and hashed depending on configuration)

relates to:

- https://github.com/angular/angular-cli/issues/12797
- https://github.com/angular/angular-cli/issues/17747
- https://github.com/angular/angular/pull/32921
- https://github.com/angular/angular-cli/blob/14.0.x/packages/angular_devkit/build_angular/src/webpack/plugins/postcss-cli-resources.ts#L79 


- https://github.com/angular/angular-cli/issues/3415#issuecomment-515203223

- https://angular.io/guide/deployment#the-base-tag


---

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.3.4.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.
