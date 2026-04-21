---
id: aa76377f-2ec5-456b-ad7d-8473a7d6119a
title: Svelte + capcitor reddit post
created_at: 2026-03-18T02:35:20.315Z
datetime: 2026-04-01T21:47:00.861Z
tags: []
context: {"deviceName":"Emmanuels-MacBook-Pro.local","hostname":"Emmanuels-MacBook-Pro.local","activeApp":"Google Chrome","timeOfDay":"night","timestamp":"2026-03-18T02:35:20.334Z"}
---

https://www.reddit.com/r/sveltejs/comments/1mk05ym/mobile_app_made_with_svelte_5_capacitor/

Hey ya'll!

I've recently published my first mobile app, made entirely with Svelte & SvelteKit on the Apple App store.

The developer experience with Capacitor is quite good, there are easy to use plugins for almost everything including vibrations, rating dialogues, easily formatting app store assets and more.

For the UI I used Shadcn-Svelte with Tailwind 4 (love it!) and modified the components to be more suitable for mobile – larger touch targets, different user-select behaviors and active: state with an animation. I also created a custom color scheme and used ModeWatcher for automatically switching between light and dark.

For internationalization, I used ParaglideJS which works well for the most part, it's just a bit of a chore to handle formatted text (with bold, cursive parts) since you either need to split it into multiple parts or come up with your own formatting function afaik. Maybe there's a better way to do this :-)

I used some handy CSS like overscroll-behavior: none, the safe-area css env variables and some HTML viewport parameters like user-scalable: no to make it feel close to native.