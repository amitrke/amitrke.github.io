---
layout: post
title:  "Learning Angular"
date:   2017-12-01 21:14:30 -0500
categories: Technology
---

# Framework and libraries

# AngularJS vs Angular

# Typescript

# Building Blocks

## Angular CLI

### Generate

```
$ ng g component {componentname}
```

```
ng g service services/user
```

## Modules

## Components

## Directives

Directives allow you to attach a custom behavior to an HTML element.

# Module Loaders

## System JS

## Webpack

## FAQ

### What are Angular component life cycle functions

### What is the difference between constructor and ngInit function

Constructor is predefined default method of the typescript class. There is no relation between Angular and constructor. Normally we use constructor to define/initialize some variables, Inject services, but when we have tasks related to Angular's bindings we move to Angular's ngOnInit life cycle hook. ngOnInit is called just after the constructor call. We can also do the same work in the constructor but its preferable to use ngOnInit to start Angular's binding.

in order to use ngOnInit we have to import this hook from the core library:
```
import {Component, OnInit} from '@angular/core'
```

### How do you do data binding in Angular
Data binding is a core concept in Angular and allows to define communication between a component and the DOM
#### Component to DOM
Interpolation: {{ value }}
This adds the value of a property from the component:
```
<li>Name: {{ user.name }}</li>
```
Property binding: [property]=”value”
The value is passed from the component to the specified property.
```
<input type="email" [value]="user.email">
```
#### DOM to Component
Event binding: (event)=”function”

On DOM event (eg.: click, change), call the specified specified method in the component.
```
<button (click)="submit()"></button>
```
#### Two-way
Two-way data binding: [(ngModel)]=”value”

```
<input type="email" [(ngModel)]="user.email">
```

### How do you use promises in Angular

https://codecraft.tv/courses/angular/es6-typescript/promises/

### How do you use Observables in Angular
Angular 2 onwards it is included as default async type.
https://medium.com/@mpodlasin/promises-vs-observables-4c123c51fe13

### What are the main differences between promises and Observables

### What is AOT and how is it better than just in time compilation

### Which boiler plate code did you use to create your Angular app

I generally use Angular CLI

### How did you uglify and minify the JS files If you used webpack, how many bundle files did you had for your production build.

### What are the main differences between Angular 2, 4

### How do templates work in Angular 2
