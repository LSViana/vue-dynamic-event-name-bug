# vue-dynamic-event-name-bug

This repository contains a bug demonstration related to [RIDER-83124](https://youtrack.jetbrains.com/issue/RIDER-83124/Vue-variables-used-as-dynamic-event-names-are-marked-as-unused). It's a bug in the Vue.js tooling of JetBrains Rider.

The bug happens when variables used as dynamic event names in `<template>` are marked as unused by the IDE.
There are two examples of this bug demonstrated through:

1. Composition API + `script setup`: `src/App.vue`
2. Options API: `src/components/HelloWorld.vue`

Both examples declare an `eventName` variable (or `computed` property) and use it via the syntax `@[eventName]="..."`
inside the `<template>` of their respective components. Even with that usage, the IDE marks both `eventName` identifiers
as unused in both scenarios.