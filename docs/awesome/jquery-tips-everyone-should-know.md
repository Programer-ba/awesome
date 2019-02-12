# jQuery Tips Everyone Should Know [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A collection of simple tips to help up your jQuery game.

> For other great lists check out [@sindresorhus](https://github.com/sindresorhus/)'s curated list of [awesome lists](https://github.com/sindresorhus/awesome/).



* [Contribution Guidelines](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/CONTRIBUTING.md)


## Tips

1. [Use `noConflict(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)`](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/#use-noconflict)
1. [Use `.on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` Binding Instead of `.click(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)`](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/#use-on-binding-instead-of-click)


### Use `noConflict()`

The `$` alias used by jQuery is also used by other JavaScript libraries. To ensure that jQuery doesn't conflict with the `$` object of different libraries, use the `noConflict()` method at the start of the document:

```javascript
jQuery.noConflict();
```

Now you'll reference the jQuery object using the `jQuery` variable name instead of `$` (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e.g., `jQuery(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'div p').hide(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)`). If you have multiple versions of jQuery on the same page (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/not recommended), you can use `noConflict(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` to set an alias to a specific version:

```javascript
let $x = jQuery.noConflict();
```



### Checking If jQuery Loaded

Before you can do anything with jQuery you first need to make certain it has loaded:

```javascript
if (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/typeof jQuery == 'undefined') {
  console.log(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'jQuery hasn\'t loaded');
} else {
  console.log(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'jQuery has loaded');
}
```

Now you're off...



### Use `.on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` Binding Instead of `.click(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)`

Using `.on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` gives you several advantages over using `.click(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)`, such as the ability to add multiple events...

```javascript
.on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click tap hover')
```

...a binding applies to dynamically created elements, as well (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/there's no need to manually bind every single element dynamically added to a DOM element)...

...and the possibility to set a namespace:

```javascript
.on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click.menuOpening')
```

Namespaces give you the power to unbind a specific event (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e.g., `.off(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click.menuOpening')`).



### Back to Top Button

By using the `animate` and `scrollTop` methods in jQuery you don't need a plugin to create a simple scroll-to-top animation:

```javascript
// Back to top
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.container').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', '.back-to-top', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
  e.preventDefault();
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'html, body').animate(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/{scrollTop: 0}, 800);
});
```

```html
<!-- Create an anchor tag -->
<div class="container">
  <a href="#" class="back-to-top">Back to top</a>
</div>
```

Changing the `scrollTop` value changes where you wants the scrollbar to land. All you're really doing is animating the body of the document throughout the course of 800 milliseconds until it scrolls to the top of the document.

**Note:** Watch for some [buggy behavior](https://github.com/jquery/api.jquery.com/issues/417) with `scrollTop`.



### Preload Images

If your web page uses a lot of images that aren't visible initially (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e.g., on hover) it makes sense to preload them:

```javascript
$.preloadImages = function () {
  for (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/var i = 0; i < arguments.length; i++) {
    $('<img>').attr('src', arguments[i]);
  }
};

$.preloadImages(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'img/hover-on.png', 'img/hover-off.png');
```



### Checking If Images Are Loaded

Sometimes you might need to check if your images have fully loaded in order to continue on with your scripts:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'img').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'load', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  console.log(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'image load successful');
});
```

You can also check if one particular image has loaded by replacing the `<img>` tag with an ID or class.



### Fix Broken Images Automatically

If you happen to find broken image links on your site replacing them one by one can be a pain. This simple piece of code can save a lot of headaches:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'img').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'error', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  if(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/!$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).hasClass(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'broken-image')) {
    $(this).prop('src', 'img/broken.png').addClass('broken-image');
  }
});
```

Alternatively, if you wish to hide broken images this snippet will take care of that for:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'img').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'error', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).hide(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
});
```



### Post a Form with AJAX

jQuery AJAX methods are a common way to request text, HTML, XML, or JSON. If you wanted to send a form via AJAX you could collect the user inputs via the `val()` method:

```javascript
$.post('sign_up.php', {
  user_name: $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'input[name=user_name]').val(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/),
  email:     $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'input[name=email]').val(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/),
  password:  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'input[name=password]').val(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/),
});
```

But all of those `val(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` calls are expensive and using `.val(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` on `<textarea>` elements will strip carriage return characters from the browser-reported value. A better way of collecting user inputs is using the `serialize(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)` function which collects them as a string:

```javascript
$.post(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'sign_up', $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#sign-up-form').serialize(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/));
```



### Toggle Classes on Hover

Let's say you want to change the visual of a clickable element on your page when a user hovers over it. You can add a class to your element when the user is hovering; when the user stops hovering removes the class:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.btn').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'hover', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).addClass(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'hover');
}, function () {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).removeClass(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'hover');
});
```

You need to add the necessary CSS. If you want an even _simpler_ way use the `toggleClass` method:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.btn').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'hover', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).toggleClass(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'hover');
});
```

**Note:** CSS may be a faster solution in this case but it's still worthwhile to know this.



### Disabling Input Fields

At times you may want the submit button of a form or one of its text inputs to be disabled until the user has performed a certain action (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e.g., checking the "I've read the terms" checkbox). Add the `disabled` attribute to your input so you can enable it when you want:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'input[type="submit"]').prop(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'disabled', true);
```

All you need to do is run the `prop` method again on the input, but set the value of `disabled` to `false`:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'input[type="submit"]').prop(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'disabled', false);
```



### Stop the Loading of Links

Sometimes you don't want links to go to a certain web page nor reload the page; you might want them to do something else like trigger another script. This will do the trick of preventing the default action:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'a.no-link').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
  e.preventDefault();
});
```



### Cache jQuery Selectors

Think of how many times you write the same selector over and over again in any project. Every `$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.element')` selector has to search the entire DOM each time, regardless if that selector had previously run. Instead you can run the selector once and store the results in a variable:

```javascript
var blocks = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#blocks').find(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'li');
```

Now you can use the `blocks` variable wherever you want without having to search the DOM every time:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#hideBlocks').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  blocks.fadeOut();
});

$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#showBlocks').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  blocks.fadeIn();
});
```

Caching jQuery selectors is a good performance gain.



### Toggle Fade/Slide

Sliding and fading are common in animations with jQuery. You might want to show an element when a user clicks something, which makes the `fadeIn` and `slideDown` methods perfect, but if you want that element to appear on the first click and then disappear on the second, this will work fine:

```javascript
// Fade
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.btn').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.element').fadeToggle(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'slow');
});

// Toggle
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.btn').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.element').slideToggle(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'slow');
});
```



### Simple Accordion

This is a simple method for a quick accordion:

```javascript
// Close all panels

// Accordion
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#accordion').find(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.accordion-header').on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'click', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  var next = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).next(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
  next.slideToggle(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'fast');
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.content').not(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/next).slideUp(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'fast');
  return false;
});
```

By adding this script all you really need to do on your web page is the necessary HTML to get this working.



### Make Two Divs the Same Height

Sometimes you'll want two divs to have the same height no matter what content they have in them:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.div').css(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'min-height', $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.main-div').height(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/));
```

This example sets the `min-height` which means that it can be bigger than the main div but never smaller. However, a more flexible method would be to loop over a set of elements and set `height` to the height of the tallest element:

```javascript
var $columns = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.column');
var height = 0;
$columns.each(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  if (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).height(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) > height) {
    height = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).height(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
  }
});
$columns.height(height);
```

If you want _all_ columns to have the same height:

```javascript
var $rows = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.same-height-columns');
$rows.each(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).find(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'.column').height(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/this).height(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/));
});
```

**Note:** This can be done several ways [in CSS](http://codepen.io/AllThingsSmitty/pen/KMPqoO) but depending on what your needs are, knowing how to do this in jQuery is handy.



### Open External Links in New Tab/Window

Open external links in a new browser tab or window and ensure links on the same origin open in the same tab or window:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'a[href^="http"]').attr(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'target', '_blank');
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'a[href^="//"]').attr(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'target', '_blank');
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'a[href^="' + window.location.origin + '"]').attr(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'target', '_self');
```

**Note:** `window.location.origin` doesn't work in IE10. [This fix](http://tosbourn.com/a-fix-for-window-location-origin-in-internet-explorer/) takes care of the issue.



### Find Element By Text

By using the `contains()` selector in jQuery you can find text in content of an element. If text doesn't exists, that element will be hidden:

```javascript
var search = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#search').val(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'div:not(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/:contains(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/"' + search + '"))').hide(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
```



### Trigger on Visibility Change

Trigger JavaScript when the user is no longer focusing on a tab or refocuses on a tab:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/document).on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'visibilitychange', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
  if (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e.target.visibilityState === 'visible') {
    console.log(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'Tab is now in view!');
  } else if (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e.target.visibilityState === 'hidden') {
    console.log(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'Tab is now hidden!');
  }
});
```



### AJAX Call Error Handling

When an AJAX call returns a 404 or 500 error, the error handler will be executed. If the handler isn't defined, other jQuery code might not work as intended. To define a global AJAX error handler:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/document).on(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'ajaxError', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e, xhr, settings, error) {
  console.log(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/error);
});
```



### Chain Plugin Calls

jQuery allows for the "chaining" of plugin method calls to mitigate the process of repeatedly querying the DOM and creating multiple jQuery objects. Let's say the following snippet represents your plugin method calls:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#elem').show(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#elem').html(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'bla');
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#elem').otherStuff(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);
```

This could be vastly improved by using chaining:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#elem')
  .show()
  .html(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'bla')
  .otherStuff();
```

An alternative is to cache the element in a variable (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/prefixed with `$`):

```javascript
var $elem = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#elem');
$elem.hide();
$elem.html(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'bla');
$elem.otherStuff();
```




### Sort List Items Alphabetically

Let's say you end up with too many items in a list. Maybe the content is produced by a CMS and you want to order them alphabetically:

```javascript
var ul = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#list'),
lis = $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'li', ul).get(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/);

lis.sort(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/a, b) {
  return (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/a).text(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/).toUpperCase(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) < $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/b).text(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/).toUpperCase(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/)) ? -1 : 1;
});

ul.append(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/lis);
```

There you go!



### Disable Right-Click

If you want to disable right-click, you can do it for an entire page...

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/document).ready(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/document).bind(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'contextmenu', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
    return false;
  })
})
```

...and you can also do the same for a specific element:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/document).ready(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#submit').bind(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'contextmenu', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
    return false;
  })
})
```



## Support

Current versions of Chrome, Firefox, Safari, Opera, Edge, and IE11.



## Translations

* [Español](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/es-ES)
* [Français](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/fr-FR)
* [Magyar](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/hu-HU)
* [Português do Europe](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/pt-PT)
* [Pусский](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/ru-RU)
* [简体中文](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/zh-CN)
* [繁體中文](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/zh-TW)
hub.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
    return false;
  })
})
```

...and you can also do the same for a specific element:

```javascript
$(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/document).ready(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/) {
  $(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'#submit').bind(https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/'contextmenu', function (https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/blob/master/e) {
    return false;
  })
})
```



## Support

Current versions of Chrome, Firefox, Safari, Opera, Edge, and IE11.



## Translations

* [Español](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/es-ES)
* [Français](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/fr-FR)
* [Magyar](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/hu-HU)
* [Português do Europe](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/pt-PT)
* [Pусский](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/ru-RU)
* [简体中文](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/zh-CN)
* [繁體中文](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/zh-TW)
ortuguês do Europe](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/pt-PT)
* [Pусский](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/ru-RU)
* [简体中文](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/zh-CN)
* [繁體中文](https://github.com/AllThingsSmitty/jquery-tips-everyone-should-know/tree/master/translations/zh-TW)