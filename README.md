# Startpage

![screenshot](startpage-screenshot.png)

> Start your surfing right

A startpage for your browser to quickly access some links and using different search engines.

## Getting started

```shell
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev
```

## Features

* Choose a search engine, for example:
  - [DuckDuckGo](https://duckduckgo.com/)
  - [Google](https://www.google.com/)
  - [Dict](https://www.dict.cc/)
  - [Dees.cc](https://dees.dict.cc/)
* Quickly access links you often use
* Beautiful, random background images
* hidden scrollbar in Chrome and Firefox
* Customise links with a picture and title of your choice

## Configuration

### Add a searchbar
To add a searchbar go to `src\components\searchbar.vue` and add a object to the _search_engines_.

```js
search_engines: {
  google: {
    action: "http://www.google.com/search",
    name: "q"
  },
  duckduckgo: {
    action: "https://duckduckgo.com/",
    name: "q"
  },
}
```

### Customise links
To add or change a link go to `src\components\hyperlinks.vue` and change the desired values

```js
<template>
  <div class="links-container">
    <hyperlink title="Calendar" href="https://calendar.google.com/calendar/r" image="https://source.unsplash.com/zni0zgb3bkQ"></hyperlink>
    // ...
  </div>
</template>
}
```

## Built With

* [Vue.js](https://vuejs.org/) - The web framework used
* [Bulma](https://bulma.io/) - The css framework used
* [Unsplash](https://source.unsplash.com/) - For the beautiful background images

## Acknowledgement

* [ReadMe Guideline](https://github.com/jehna/readme-best-practices) - For making a decent ReadMe
* [ReadMe Template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2) - For making a decent ReadMe

## Licensing

The code in this project is licensed under MIT license.
