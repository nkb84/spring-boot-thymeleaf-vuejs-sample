# spring-boot-thymeleaf-vues-sample

This is an sample of how to combined:
- Server: spring boot + thymeleaf
- Client: vuejs + multiple pages

In this sample, we use source code from [string guides](https://github.com/spring-guides/gs-serving-web-content/) and generate a new vue project from [vue-multiple-pages](https://github.com/nkb84/webpack-multiple-pages) template.

## How to use

### Server side

- Static resources are put at `src/main/webapp`
- Thymeleaf templates are put at `src/main/resources/templates`

### Client side

- Install dependencies

``` bash
npm install
```

- Create a new page
    - Create a new folder (can have multiple level) in src/pages folder
    - New folder includes: `app.html`, `app.js` and `App.vue`
    - Add a new route file for new page, and change the required router in `app.js` 
    - `app.html` can contains `thymeleaf` tags

- Build for production with minification, the output is `dist` folder
```bash
npm run build
```

- With the page use `thymeleaf`, copy that html file to server at `src/main/resources/templates/`
- With the normal pages, copy all remaining files to server at `src/main/webapp/`
