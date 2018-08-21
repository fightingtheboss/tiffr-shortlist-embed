# TIFF + TIFFR

A small prototype showing off the TIFFR embed widget

https://tiffr-shortlist-widget.netlify.com/

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

1. Install some kind of web server for convenience, we recommend serve `yarn global add serve`.
2. run `serve` and navigate to /app.

### Setup

1. Clone this repository
2. Change into the project directory (`cd tiffr-shortlist-embed`)
3. Open /app in a browser or use a simple server (see above) to serve it.