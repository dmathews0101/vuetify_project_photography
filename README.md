# photography - responsive website using vuetify 
---
# Vuetify #1 : Create new app to create website
---
Vuetify is an UI library built with the help of vuejs and material design.

1. In home page, we have header, carasol, image gallery, latest post, and footer.
2. In about page, we have static image with title, some content, image gallery for teams and
3. In contact page, we have static image with title, contact form, and google map
---
node -v
vue -version
vue create photography
cd photography
vue add vuetify
npm run serve
---
4. here vue instance is created, and it is mounting towards appid, which is in index.html ...in public folder
new Vue({
  router,
  vuetify,
  render: h => h(App)
}).$mount('#app')

---
# Vuetify #2 : Working on Toolbar UI Component to create header
---
1. Create header using toolbar UI component
2. Vuetify -> UI Components -> Bars -> Toolbars
3. Dense Toolbars
4. v-toolbar-title is used for displaying a title and v-toolbar-items along with v-btn is used to add some items 
5. In our code, using text and flat props to remove black background and remove drop shadow

---
# Vuetify #3 : Adding and Importing SCSS in Vuetify
---
1. adding and importing scss in vuetify 
2. adding scss in src folder
3. the files and folder structure inside scss folder does not matter as long as we have imported every sass file in main.scss
4. importing main.scss in main.js
5. now our scss file should be ready to use and we should see some changes in the header
6. adding google fonts, copy link and add it to index.html

---
# Vuetify #4 : Working on Carousel Component
---
1. working on carousel UI component, create hero component
2. importing hero component, adding hero component inside v-content
3. vuetify -> get started -> ui components -> carousels -> custom transition
4. copying v-carousel to Hero component, after adding div with a class of hero block
5. we have use a class called hero block because in index.scss, we have added some style for hero block
6. it is adding height for hero block in mobile version, adding black overlay in images and adjusting title
7. copying script -> data, and pasting it in our hero component
8. removing container to get full width
9. to remove pagination we can add hide delimiters in v-carousel -> adding prop hide-delimiters to v-carousel
10. we can add cycle prop to make the image change automatically
11. adding custom images by adding images folder to src->assets folder,... for carousel, images used img-carousel1, img-carousel2, img-carousel3
12. src: require("../assets/images/img-carousel1.jpg")
13. according to our design, we have to add title in our carousel, .. so we can add title in items object
14. copying code for carousel with title,.. v-row, display-3,.. then in interpolation using item.title, because we have used title as the property,.. also add title as class name for v-row,.. removing class display-3

---
# Vuetify #5 : Working on Images Component to create Gallery
---
1. creating gallery using images component
2. creating new component called gallery
3. vuetify -> getting started -> UI Components -> Images -> grid -> v-row -> add div with a class of block and galleryBlock
4. using images in assets->images instead of sample images
5. adding items array with id and source properties,.. change for loop to item in items, .. and key as item.id,.. changing src to item.src
6. adding gallery title,.. by adding an h2 with a class of text-center

---
# Vuetify #6 : Working on Card Component to create Latest Post
---
1. creating latest post using card component,.. create new component called latestpost
2. adding latest post component to app.vue
3. vuetify -> get started -> UI Components -> Cards -> Media with text -> v-card 
3. adding v-container inside the latestPostBlock,.. same for gallery.vue as well to remove gap
4. removing max-width and add outline to remove box shadow and add border
5. we can use v-row and v-col if we want to use grid system
6. adding dynamic content by adding data in items object,.. we need id, title, subtitle, description and image src
7. once we get our data, we can use for loop in v-col ,.. using interpolation to show the data
8. for images we can bind the images to item.src

---
# Vuetify #7 : Working on Footer Component to create Footer
---
1. creating footer using footer component,.. creating new component called footer 
2. adding v-footer, footer component in app.vue
3. vuetify -> get started -> UI components -> footer -> indigo footer
4. copying v-footer to footer.vue,.. removing div with the class of block,.. copying everything in script starting with data to footer.vue
5. importing font-awesome using css cdn in index.html
6. removing indigo and lighten-1 class from v-card,.. removing dark theme by removing dark from v-footer
7. removing white--text, to make text and font color to black

---
# Vuetify #8 : Working on Vue Router and managing components
---
1. managing components using vue router,.. installing vue router using npm,.. npm install vue-router
2. importing and using VueRouter from vue-router
3. creating 4 components : home, about, contact and one for not found page, ... adding all of them in new folder views
4. importing home, about, contact and NotFound in main.js
5. creating router instance and passing route options,.. using path and component
6. adding router inside the vue instance
7. in app.vue,.. header and footer across all pages,.. adding router view in between them,.. so all components matched by the route will render inside router-view
8. adding router link in header.vue for home, about and contact button
9. moving hero, gallery and latest posts into this home component
10. moving hero, gallery and latestpost component from app.vue to home.vue component
11. removing the # tag in the url by adding mode history in main.js

---
# Vuetify #9 : Working on about page using image and card component
---
1. using image and card component to create about page
2. creating hero block with image and text at bottom
3. vuetify -> get started -> UI components -> images -> fixed ratio
4. copying v-img -> div with a class of staticHero, changing image src, and removing aspect ratio, email address, changing classname from subheading to headline,... centering text
5. adding paragraph,... our teams using cards component
6. grid using v-row, v-col, cols=4 -> width becomes 33 %
7. vuetify -> cards -> media with text
8. copying v-card to v-col,.. removing v-card-title, v-card-subtitle and v-card-action,.. adding some data with id, src, name and title
9. adding forloop in v-col,.. using interpolation to get the dynamic data,.. adding class text-center to bring text to center

---
# Vuetify #10 : Working on contact page using images and form component
---
1. creating contact page using images and forms component,.. adding google map using iframe
2. adding same hero block as about page,.. changing image and title block
3. vuetify -> get started -> UI components -> form input and controls -> forms -> validation with submit and clear
4. copying v-form to contact.vue, .. copying script tag
5. changing checkbox to textarea
6. vuetify -> UI components -> form input and controls -> textareas -> usage -> default style,... copying v-textarea,.. removing select and items
7. adding validation for textarea message
8. adding google map in site,... google.com/maps,.. searching for london, .. share -> embed a map -> iframe link -> adding iframe inside a div with a class of googlemap,.. removing attributes frameborder, style, allowfullscreen,.. width = 100%

---
# Vuetify #11 : Working on Not Found Page
---
1. creating not found page
2. adding heading, paragraph, icon <i class="fas fa-exclamation-triangle red--text"></i>,.. increasing font size and adding margin to icon by creating and selecting class notfound fas in common.scss

---
# Vuetify #12 : Working on responsive using grid component
---
1. making the site fully responsive,.. opening grid component to find out the breakpoint we need to know
2. vuetify -> get started -> UI components -> grids -> 5 different breakpoints -> xs, sm, md, lg, xl
3. opening developer tool(f12) -> clicking on toggle device toolbar -> responsive -> 1264 (desktop), 960 (large tablet and laptops), 600 (small to medium tablets)
4. making latest posts in home page to 100% width, rather than 33% width,.. v-col md="4", cols="12",.. 4 means using 33% width(here in large tablet to laptop, and also in higher devices) and 12 means using 100% width
5. 320 -> small to large handset -> removing text from hero block -> hero.vue -> v-row class="fill-height title hidden-xs-only",.. hiding the title when device is 600px or less
6. in gallery show 2 columns instead of 3,.. gallery.vue,.. v-col,.. cols="6"(for small handset to medium tablet,.. <600px to 960px) md="4" (for large tablet to laptop,.. 960px-1264px )
7. fixing our teams in about page,.. v-col, cols = "12",.. sm = "4",.. apply 100% width only in mobile version
8. adding burger menu,.. hiding current navigation in mobile version,.. header.vue.., v-toolbar-items class="hidden-xs-only" (hidden for mobile versions),.. adding drop down menu in mobile version
9. vuetify -> menus -> usage,.. copying v-menu to header.vue,.. class = "hidden-sm-and-up",.. this class will let us hide this dropdown from breakpoint small and up
10. remove interpolation, add static content, new class responsiveMenu, adding router link
11. instead of the dropdown button, using the burger icon,.. can find icon in UI Components -> bars -> Toolbars,.. adding <v-app-bar-icon> , adding v-on, removing v-btn

---
# Vuetify #13 : Deployment and making it live
---
1. deploying and making site live,..opening link
cli.vuejs.org/guide/deploymeny.html ,.. documentation on   deployment using vue cli
2. copying publicPath to vue.config.js, change project folder name
3. npm run build
4. building dist folder, .. adding to hosting account to make it live,.. 
5. copying dist folder to desktop, renaming to vuetifyproject, creating zip folder using winrar, logging in to cpanel hosting details
6. opening cpanel -> file manger -> public_html -> upload -> selecting zip file -> closing, refreshing tab,... -> public html -> vuetifyproject -> extracting project
7. adding the url of project : domain/vuetifyproject/

---

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn run serve
```

### Compiles and minifies for production
```
yarn run build
```

### Run your tests
```
yarn run test
```

### Lints and fixes files
```
yarn run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
# vuetify_project_photography
