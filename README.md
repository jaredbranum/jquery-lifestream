# jQuery Lifestream Plug-in

Show a stream of your online activity.  
Check out [the example][example]).

## Requirements
* [jQuery 1.3+](http://www.jquery.com)

## Supported feeds

Currently supports the following feeds natively:

* [Delicious](http://delicious.com)
* [Flickr](http://flickr.com)
* [Github](http://github.com)
* [Google Reader](http://google.com/reader)
* [Last.fm](http://last.fm)
* [Stackoverflow](http://stackoverflow.com)
* [Twitter](http://twitter.com)
* [Youtube](http://youtube.com)

Feel free to fork the project and add your own feeds in.  
Just send a pull request to christianv when you're finished.

## Usage

Add the following to the head or body tag of your HTML page.

``` html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.6.1/jquery.min.js"></script>
<script src="https://github.com/christianv/jquery-lifestream/raw/master/jquery.lifestream-compiled.js"></script>
<script>
  $("#lifestream").lifestream({
    "list":[
      {
        "service": "github",
        "user": "christianv"
      },
      {
        "service": "twitter",
        "user": "denbuzze"
      }
    ]
  });
</script>
```
The above code will always use the latest version of the script.  
If you want to use it in production, download the [compressed](https://github.com/christianv/jquery-lifestream/raw/master/jquery.lifestream-compiled.js)
or [uncompressed](https://github.com/christianv/jquery-lifestream/raw/master/jquery.lifestream.js) file locally.

## Configuration

The plug-in accepts one configuration JSON object:

``` javascript
$("#lifestream").lifestream({
  "limit": 30,
  "list":[
    {
      "service": "github",
      "user": "christianv"
    },
    {
      "service": "twitter",
      "user": "denbuzze"
    }
  ]
});
```

`limit` (_integer_): Specify how many elements you want in your lifestream (default = 10).

`list` (_array_): Array containing other JSON objects with information about each item.  
Each item should have a _service_ and a _user_.  
For more information about each _service_, check out the [source code][examplesource] of the [example page][example].

## Add your own feed

Adding in your own feed is pretty easy.  
Have a look at [this commit](https://github.com/christianv/jquery-lifestream/commit/529a06db159b4123ee3b2cc604f3a3ed698c6e9a) which adds support for the last.fm feed.

## Ideas
Stuff that isn"t implemented yet, but would be nice to have:

* Add support for [Twitter Web Intents](http://dev.twitter.com/pages/intents)

## Version log

* 0.0.5 Flickr support
* 0.0.4 Last.fm support
* 0.0.3 Delicious support + minor bug fix in the stackoverflow code
* 0.0.2 Youtube support
* 0.0.1 Initial version


[example]: http://christianv.github.com/jquery-lifestream/example.html 
"Example page"
[examplesource]: https://github.com/christianv/jquery-lifestream/blob/master/example.html "Source code of the example page"