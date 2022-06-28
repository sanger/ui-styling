# ui-styling
Sharing UI styles based on Sanger brand guidlines across projects using tailwind 

## Description
This creates an npm module containing `tailwind.config` and `tailwind.css` file, which can be installed in any project having tailwind support. 


## How to create npm module 
1) While pushing any updates made to this package to the main branch will automatically publish the package in npm repository available at `https://www.npmjs.com/package/@sanger/ui-styling`

# #How to use npm module
Install the package `yarn add @sanger/ui-styling` or `npm install @sanger/ui-styling`

The module currently supports react files and html files by default. To override/customise the configuration write your own `tailwind.config` file, then import `tailwing.config` (from ui-styling npm module installed) and apply the required modifications
For e.g. To use this in a Vue project
 - Install the ui-styling package
 - Write a separate tailwing.config.js 
    1) Import tailwind.config.js from ui-styling module 
    2) Redefine `content` section of `module.exports` for .vue files

    ```
    const defaultOptions = require('../traction-ui/node_modules/@sanger/ui-styling/tailwind.config'
        module.exports = {
        ...defaultOptions,
        purge: {
            ...defaultOptions.purge,
            content: ['./src/**/*.{html,vue}'],
        },
        } 
    ```

## Notes:-
*Please update the 'version' tag in package.json prior to every release*