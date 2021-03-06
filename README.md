Javascript Tips
===============

A collection of handy javascript tips and methods.

insertAdjacentHTML(location, content)
-------------------------------------

Inserts the `content` in the specified `location`.

The following example code is the template used throughout.

    <div id="box1">
      <p>Some example text</p>
    </div>
    <div id="box2">
      <p>Some example text</p>
    </div>

### Locations ###

The `location` parameter is a string value and may be one of the following:

* beforebegin - insert before the element
* afterbegin - prepend to the element (insert as first child)
* beforeend - append to the element (insert as last child)
* afterend - insert after the element

#### beforebegin ####

`'beforebegin'` will insert the value of `content` *before* the calling element.

##### Example #####

    <script>
      var box2 = document.getElementById("box2");
      box2.insertAdjacentHTML('beforebegin', "<div><p>Inserted text</p></div>");
    </script>

will lead to

    <div id="box1">
      <p>Some example text</p>
    </div>
    <div><p>Inserted text</p></div>
    <div id="box2">
      <p>Some example text</p>
    </div>

#### afterbegin ####

`'afterbegin'` will insert the value of `content` as the first child of the calling element.

##### Example #####

    <script>
      var box2 = document.getElementById("box2");
      box2.insertAdjacentHTML('afterbegin', '<p>Inserted text</p>');
    </script>

will lead to

    <div id="box1">
      <p>Some example text</p>
    </div>
    <div><p>Inserted text</p></div>
    <div id="box2">
      <p>Inserted text</p>
      <p>Some example text</p>
    </div>

#### beforeend ####

`'beforeend'` will insert the value of `content` as the last child of the calling element.

##### Example #####

    <script>
      var box2 = document.getElementById("box2");
      box2.insertAdjacentHTML('beforeend', "<div><p>Inserted text</p></div>");
    </script>

will lead to

    <div id="box1">
      <p>Some example text</p>
    </div>
    <div id="box2">
      <p>Some example text</p>
      <p>Inserted text</p>
    </div>

#### afterend ####

`'afterend'` will insert the value of `content` immediately following the calling element.

##### Example #####

    <script>
      var box2 = document.getElementById("box2");
      box2.insertAdjacentHTML('afterend', "<div><p>Inserted text</p></div>");
    </script>

will lead to

    <div id="box1">
      <p>Some example text</p>
    </div>
    <div id="box2">
      <p>Inserted text</p>
      <p>Some example text</p>
    </div>
    <div><p>Inserted text</p></div>
