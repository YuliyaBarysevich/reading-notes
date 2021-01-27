# Local Storage

## HTML5 Storage 

 -is a specification named Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification. Certain browser vendors also refer to it as **“Local Storage”** or **“DOM Storage.”**

**What is HTML5 Storage?**  

-it’s a way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. Unlike cookies, this data is never transmitted to the remote web server.  

**How to access HTML5 Storage?**  

-from JavaScript code, access HTML5 Storage through the localStorage object on the global window object.

```javascript
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}

//OR use Modernizr to detect support for HTML5 Storage
//before include <script> in HTML file => <script src="modernizr.min.js"></script>

if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
``` 

### Using HTML5 Storage 

1. HTML5 Storage is based on named key/value pairs
2. Stores data based on a named key (that data can be retrieved with the same key)
    - _named key is a string_
    - _data can be any type supported by JavaScript, including strings, Booleans, integers, or floats_ (stored as a string)

```javascript
interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};
``` 

- Calling `setItem()` with a named key that already exists will silently overwrite the previous value. Calling `getItem()` with a non-existent key will return null rather than throw an exception.  

>Instead of using the getItem() and setItem() methods, you can simply use square brackets.

```javascript
var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);

==== >

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
``` 

3. Methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

```javascript
interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};
``` 

4. Property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).
```javascript 
interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
``` 

5. Tracking changes to the HTML5 Storage area

To keep track programmatically of when the storage area changes, we can trap the **storage event**. The storage event is fired on the window object whenever `setItem()`, `removeItem()`, or `clear()` is called and actually changes something. For example, if we set an item to its existing value or call `clear()` when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.  

```javascript
if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};

//The handle_storage callback function will be called with a StorageEvent object

function handle_storage(e) {
  if (!e) { e = window.event; }
}
```   


[<== Back to ReadMe](../README.md)