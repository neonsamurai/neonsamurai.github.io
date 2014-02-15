---
layout: post
title: "indexOf Object in Array"
---

Every now and then I need to know the position of an object in an array.
I usually identify the object by one of its keys. The function I wrote
to return me the index of a given object in an array looks like this:

```javascript
/**
* Finds an object in an array using a key => value pair
* @param   {Array}   list   The array which is to be searched.
* @param   {String}  key    The key by which the object should be
*                           identified.
* @param   {varies}  value  Value of the key.
* @return  {Number}         The index of the object.
**/
function indexOfObject(list, key, val){
  return _.chain(list).pluck(key).indexOf(val).value();
  }
```

The implementation uses Underscore.js
