# Branode

A Branode é um serviço de hospedagem e suporte para sites WordPress. Criada para facilitar o processo de criação e manutenção de sites WP. Nós queremos ser aquela pessoa que diz “vá em frente”. Antes que algo dê errado, indicamos o melhor caminho. Mas se um problema aparecer, estaremos ao lado do cliente solucionando os problemas.

* Description: Combination of Automattic´s _s theme and Bootstrap 4. Made as a solid starting point for your next theme project and WordPress website. Use it as starter theme or as a parent theme. It is up to you. Including Font Awesome support, built-in widget slider and much more you need for basic websites. IMPORTANT: All developer dependencies are not bundled with this install file. Just download the .zip, extract it and run "npm install" and "gulp copy-assets" inside the extracted /understrap folder. That downloads everything and moves it in place so that you can recompile your CSS and JS files;
* Tested up to: 5.1
* License: UnderStrap WordPress Theme, Copyright 2013-2017 Holger Koenemann
* UnderStrap is distributed under the terms of the GNU GPL version 2
* License URI: http://www.gnu.org/licenses/gpl-2.0.html

## O tema UnderStrap é necessário para o funcionamento deste projeto
Este projeto é um tema filho, é necessário o código do tema pai para seu desempenho correto.

## How it works
Understrap Child Theme shares with the parent theme all PHP files and adds its own functions.php on top of the UnderStrap parent theme's functions.php.

**IT DOES NOT LOAD THE PARENT THEMES CSS FILE(S)!** Instead it uses the UnderStrap Parent Theme as a dependency via npm and compiles its own CSS file from it.

Understrap Child Theme uses the Enqueue method to load and sort the CSS file the right way instead of the old @import method.

## Installation
1. Install the parent theme UnderStrap first: `https://github.com/understrap/understrap`
   - IMPORTANT: If you download UnderStrap from GitHub make sure you rename the "understrap-master.zip" file to "understrap.zip" or you might have problems using this child theme!
1. Upload the understrap-child folder to your wp-content/themes directory
1. Go into your WP admin backend 
1. Go to "Appearance -> Themes"
1. Activate the UnderStrap Child theme

## Editing
Add your own CSS styles to `/sass/theme/_child_theme.scss`
or import you own files into `/sass/theme/understrap-child.scss`

To overwrite Bootstrap's or UnderStrap's base variables just add your own value to:
`/sass/theme/_child_theme_variables.scss`

For example, the "$brand-primary" variable is used by both Bootstrap and UnderStrap.

Add your own color like: `$brand-primary: #ff6600;` in `/sass/theme/_child_theme_variables.scss` to overwrite it. This change will automatically apply to all elements that use the $brand-primary variable.

It will be outputted into:
`/css/understrap-child.min.css` and `/css/understrap-child.css`

So you have one clean CSS file at the end and just one request.

## Developing With NPM, Gulp, SASS and Browser Sync

### Installing Dependencies
- Make sure you have installed Node.js, Gulp, and Browser-Sync [1] on your computer globally
- Open your terminal and browse to the location of your UnderStrap copy
- Run: `$ npm install` then: `$ gulp copy-assets`

### Running
To work and compile your Sass files on the fly start:

- `$ gulp watch`

Or, to run with Browser-Sync:

- First change the browser-sync options to reflect your environment in the file `/gulpconfig.json` in the beginning of the file:
```javascript
  "browserSyncOptions" : {
    "proxy": "localhost/wordpress/",
    "notify": false
  }
};
```
- then run: `$ gulp watch-bs`

[1] Visit [https://browsersync.io/](https://browsersync.io/) for more information on Browser Sync

## Plugins used in this project
* Divi Builder
* WooCommerce
* WooCommerce Iugu

## Credits
* Diego Rojas