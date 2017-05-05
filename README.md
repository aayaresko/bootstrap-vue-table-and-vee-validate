# adaptation

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

Execute:
```
npm run dev
```
and visit http://localhost:8080/#/home page - you will see the error:
```
[Vue warn]: The computed property "fields" is already defined in data.

found in

---> <Hello> at /srv/aayaresko/public_html/www/vuejs/adaptation/src/components/Hello.vue
       <App> at /srv/aayaresko/public_html/www/vuejs/adaptation/src/App.vue
         <Root> app.js line 721 > eval:432:1

[Vue warn]: Property or method "msg" is not defined on the instance but referenced during render. Make sure to declare reactive data properties in the data option.

found in

---> <Hello> at /srv/aayaresko/public_html/www/vuejs/adaptation/src/components/Hello.vue
       <App> at /srv/aayaresko/public_html/www/vuejs/adaptation/src/App.vue
         <Root> app.js line 721 > eval:432:1

[Vue warn]: The computed property "fields" is already defined as a prop.

found in

---> <BTable>
       <Hello> at /srv/aayaresko/public_html/www/vuejs/adaptation/src/components/Hello.vue
         <App> at /srv/aayaresko/public_html/www/vuejs/adaptation/src/App.vue
           <Root>
```
