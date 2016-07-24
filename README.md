# Lazy-polymer

An experimental lazy loading pattern for polymer apps

##### Compoenents used:
  - Polymer
  - [generator-polymer](https://github.com/yeoman/generator-polymer)
  - [app-router](https://github.com/erikringsmuth/app-router)
  - Gulp - Vulcanize

##### Inspiration 
  - https://aerotwist.com/blog/polymer-for-the-performance-obsessed/
  - https://github.com/angular-ui/ui-router

##### Problem
Creating a huge polymer app, simple vulcanize concats all files into a single file. In an application with 7 - 8 submodules, loading all the modules at once isn't a great idea, especially when 2 or 3 modules has some fancy exclusive content that normally people won't use. In this experiment, we are trying to load submodules on the fly. The app structure was made with generator-polymer yeoman scaffold.

##### Solution
  - Divide project into modules
  - `elements.html` reffers all common elements
  - Create entry elemets for submodules and put them alongside commmon elements eg: `my-list-entry.html`
  - Make use of `aerotwist's lazyLoadPolymerAndElements()` function
  - Load entry elements in routes
  - Write gulp tasks to vulcanize each module induvidually

##### To Do:
  - Check if works with sub routes
