# Vue Data Clock

Vue app to add strings of text ('skills') to an existing list. With each entry there is a delete button. Input validation is used to prevent empty strings or strings of less than 5 charaters from being added to the list.

**\* Note: to open web links in a new window use: _ctrl+click on link_**

## Table of contents

- [General info](#general-info)
- [Screenshots](#screenshots)
- [Technologies](#technologies)
- [Setup](#setup)
- [Features](#features)
- [Status](#status)
- [Inspiration](#inspiration)
- [Contact](#contact)

## General info

- This tutorial project used Vue Components, Templating, Input Verification, Styling, Forms, Animation, Routing.

## Screenshots

![Example screenshot](./img/skills-list.png).

## Technologies

- [Vue framework v2.6.10](https://vuejs.org/)

- [Vue Router v3.0.6](https://router.vuejs.org/) the official router for Vue.js

- [Vue CLI v3.6.0](https://cli.vuejs.org/)

- [Vue Vee-Validate](https://www.npmjs.com/package/vee-validate) a template-based validation framework that validates inputs and displays errors.

- [Vue DevTools extension for Chrome](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd) was used for debugging.

## Setup

Run `npm run serve` then navigate to `http://localhost:8080/`. The app will automatically reload if you change any of the source files.

## Code Examples

-addSkill() and remove() functions from `Skills.vue

```javascript

methods: {
  addSkill() {
    this.$validator.validateAll().then((result) => {
      if(result) {
        this.skills.push({skill: this.skill})
        this.skill = '';
      }
      console.log('not valid');
    })
  },
  remove(id) {
    this.skills.splice(id,1);
  }
}

```

## Features

- Add and delete skills from the Skills list supplied.

## Status & To-Do List

- Status: Tested and 100% working.

- To-Do: Add mode data inputs and add clock functionality.

## Inspiration

- [Gary Simon Youtube video: "The Vue Tutorial for 2018 - Learn Vue 2 in 65 Minutes"](https://www.youtube.com/watch?v=78tNYZUS-ps&t=2s)

## Contact

Created by [ABateman](https://www.andrewbateman.org) - feel free to contact me!
