---
id: 56592a60ddddeae28f7aa8e1
title: الوصول إلى القائمات المتعددة الأبعاد باستخدام الترتيب (Access Multi-Dimensional Arrays With Indexes)
challengeType: 1
videoUrl: 'https://scrimba.com/c/ckND4Cq'
forumTopicId: 16159
dashedName: access-multi-dimensional-arrays-with-indexes
---

# --description--

إحدى الطرق للتفكير في قائمة <dfn>عديده الأبعاد(multi-dimensional)</dfn> هي تكون *قائمة من قائمات (array of arrays)*. When you use brackets to access your array, the first set of brackets refers to the entries in the outermost (the first level) array, and each additional pair of brackets refers to the next level of entries inside.

**مثال**

```js
const arr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14]
];

const subarray = arr[3];
const nestedSubarray = arr[3][0];
const element = arr[3][0][1];
```

في هذا المثال، لدي `subarray` قيمة `[[10, 11, 12], 13, 14]`, ولدي `nestedSubarray` قيمة `[10, 11, 12]`, ولدي `element` قيمة `11`.

**ملاحظة:** لا ينبغي أن تكون هناك أي مسافات بين اسم القائمة (array) والأقواس المربعة، مثل `array [0][0]` و حتي ذلك `array [0] [0]` ممنوع أيضاً. مع أنّ JavaScript قادر على معالجة هذا الأمر بشكل صحيح، إلا أن هذا قد يحير المبرمجين الآخرين الذين يقرؤون التعليمات البرمجية الخاص بك.

# --instructions--

باستخدام bracket notation، اختر عنصرا من `myArray` بحيث أن `myData` يساوي `8`.

# --hints--

يجب أن يساوي `myData` قيمة `8`.

```js
assert(myData === 8);
```

يجب أن تستخدم bracket notation لقراءة القيمة الصحيحة من `myArray`.

```js
assert(/myData=myArray\[2\]\[1\]/.test(__helpers.removeWhiteSpace(code)));
```

# --seed--

## --after-user-code--

```js
if(typeof myArray !== "undefined"){(function(){return "myData: " + myData + " myArray: " + JSON.stringify(myArray);})();}
```

## --seed-contents--

```js
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[0][0];
```

# --solutions--

```js
const myArray = [[1, 2, 3], [4, 5, 6], [7, 8, 9], [[10, 11, 12], 13, 14]];
const myData = myArray[2][1];
```
