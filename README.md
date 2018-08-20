# TIFF + TIFFR

A small prototype showing off the TIFFR embed widget

http://fightingtheboss.github.io/tiffr-shortlist-embed/

## Implementation

Implementation of the widget involves two steps:

### Add the widget script tag to your app

The script tag only needs to be loaded once with the rest of your assets, per page where films can be favourited. You'll need to identify the year of the festival as a data attribute, as seen in the example below:

```javascript
<script src="https://tiffr.com/assets/widget.js" data-tiffr-festival="2017"></script>
```

### Add a link to each film

Add a `<a>` tag to each film module where you want the shortlist heart to appear. The tag should have a class of `tiffr-shortlist` and a data-attribute identifying the id of the film.

```javascript
<a href="#" class="tiffr-shortlist" data-show-id="W000096151"></a>
```

The above example would add a shortlist heart for *Faces Places*.

#### Styling

Base styling for both the button and the notification is provided but you can easily override them, particularly useful for changing colours and positioning to integrate better into your site.

The main classes you'll need are:

1. `.tiffr-shortlist`: class applied to the heart button
2. `.tiffr-notification`: class applied to the notification

## Running this demo app locally

### Pre-requisites
- [NodeJS](https://nodejs.org)
- [Grunt](http://gruntjs.com)
- [Bower](http://bower.io)
- [Yeoman](http://yeoman.io)

1. Install NodeJS via the installer at the above link or via [homebrew](http://brew.sh/) or [nvm](https://github.com/creationix/nvm) if on Mac OS
2. Run `npm install -g grunt-cli bower yo`

### Setup

1. Clone this repository
2. Change into the project directory (`cd tiffr-shortlist-embed`)
3. Run `npm install && bower install`
4. Run `grunt`
