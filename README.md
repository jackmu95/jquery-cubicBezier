# [jQuery cubicBezier][jquery-cubicbezier]

[![Build Status](https://travis-ci.org/jackmu95/jquery-cubicBezier.svg)](https://travis-ci.org/jackmu95/jquery-cubicBezier)
[![devDependency Status](https://david-dm.org/jackmu95/jquery-cubicBezier/dev-status.svg)](https://david-dm.org/jackmu95/jquery-cubicBezier#info=devDependencies)

This plugin allows you to create jQuery easing functions from cubic bezier coordinates. The code for the easing functions is a 1:1 conversion from the [WebKit Source][webkit-source] to JavaScript.

## Usage
Just include [jQuery][jquery] and the [jquery-cubicBezier](dist/jquery.cubicBezier.min.js) plugin in your HTML file. After that you can start using the plugin.

**The plugin takes two arguments:**
* `coordinates` - _Any array which should contain the four cubic bezier curve coordinates. The coordinates for a **linear** curve would be `[0, 0, 1, 1]`._
* `name` - _The name under which the jQuery easing function should be registered. By default the plugin converts the `coordinates` to a string and registers the easing function under this name._

```html
<body>
    ...
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
    <script src="jquery.cubicBezier.min.js"></script>
    <script>
        $(function() {
            $('#element').animate({ 'left': 100 }, 1000, $.cubicBezier([0.25, 0.1, 0.25, 1], 'ease'));
        });
    </script>
</body>
```

## Credits
* [WebKit][webkit-source] - For the original cubic bezier easing code
* [netzgesta.de][webkit-source] - For the 1:1 conversation of the WebKit code to JavaScript
* [Janne Aukia][janne-aukia] - For the idea how to use the code for jQuery easing functions


## License
The **jquery-cubicBezier** plugin is licensed under the [MIT License](LICENSE).

[jquery-cubicbezier]: https://github.com/jackmu95/jquery-cubicBezier
[webkit-source]: https://github.com/WebKit/webkit
[jquery]: https://jquery.com
[netzgesta]: http://www.netzgesta.de/dev/cubic-bezier-timing-function.html
[janne-aukia]: https://github.com/jaukia/easie
