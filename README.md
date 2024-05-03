#### An object is a collection of properties
#### and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method. Objects in JavaScript, just as in many other programming languages, can be compared to objects in real life
``` diff
-You can also give the destructured variables different names from the original properties. This is useful when the property names don't match your variable naming conventions.!
-Вы также можете дать деструктурированным переменным имена, отличные от исходных свойств. Это полезно, когда имена свойств не соответствуют правилам именования переменных.!
```
>[!TIP]
>An object is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method.
# Creating new objects
#### You can create an object using an object initializer. Alternatively, you can first create a constructor function and then instantiate an object by invoking that function with the new operator.
![object](./object)
>it's syntax is like this JSON only permits property definition using the `"property": value` syntax. The property name must be double-quoted, and the definition cannot be a shorthand. Computed property names are not allowed either.

creating object

``` js
let object = {

};
```


#### The following code creates an object with three `properties` and the keys are `"foo"`, `"age"` and `"baz"`. The values of these keys are a string `"bar"`, the number 42, and another object.

``` js
let object = {
  foo: "bar",
  age: 42,
  baz: { myProp: 12 },
};
```

#### Accessing properties
object-rangi masivai baroi ki xamai chi qabul mekna typyof-w objectai

bad neki masiva qati  object putat kadan darkor nest baroi ki `[masiv nabor raznotipnikh elemntov]`


# neki object property: qabul mekna

>[!TIP]
>key - klych



>[!TIP]
>entrie - znacheniya

![anisa](./anisa)

>[!NOTE]
>but here it will not show Anisa because we are calling method getFullName:()=>{} and here yyou can see example of what it should show
![fff](./getfullname)



#### How we can to extract (i mean gain property) in object
>![hello](./copy)



>[!CAUTION]
>We never can write to `same keys it will get second key not first`
![samekeys](./samekeys)



>[!TIP]
>This kind we can add new key into it klych dob kni
>![klychdobkni](./addingkey)



>[!TIP]
>This kind we can delete keys from object
>![deleting](./deleting)



# Object.entries
#### Object.entries(obj);

``` diff

-Parameters:
+obj: It is the object whose enumerable property [key, value] pairs are to be returned.

-Return Value:

+Object.entries() returns an array consisting of enumerable property [key, value] pairs of the object passed.

+Example 1: In this example, an object “obj” has been created with three property[key, value] pairs, and the Object.entries() method is used to return the first property [key, value] pair of the object.
```

``` js
// Creating an object constructor
// and assigning values to it
const obj = { 0: 'adam', 1: 'billy', 2: 'chris' };
	
// Displaying the enumerable property [key, value]
// pairs of the object using object.entries() method
console.log(Object.entries(obj)[1]);
```

``` js
const object1 = {
  a: 'somestring',
  b: 42,
};

for (const [key, value] of Object.entries(object1)) {
  console.log(`${key}: ${value}`);
}

// Expected output:
// "a: somestring"
// "b: 42"
```

# Object.keys()
 
>[!TIP]
>The Object.keys() static method returns an array of a given object's own enumerable string-keyed property names.


``` js
let object1 = {
  a: 'somestring',
  b: 42,
  c: false,
};

console.log(Object.keys(object1));
// Expected output: Array ["a", "b", "c"]
```

![objkey](./objkey)



# Object.values()

>[!TIP]
>The Object.values() static method returns an array of a given object's own enumerable string-keyed property values.
![objvallues](./objvalues)



# destructuring in js
``` js

let { identifier1, identifier2, ..., identifierN } = expression;
```



# spread in object

``` js
const obj = { ...true, ..."test", ...10 };
// { '0': 't', '1': 'e', '2': 's', '3': 't' }
```


``` js
const arr = [1, 2, 3];
const arr2 = [...arr]; // like arr.slice()

arr2.push(4);
// arr2 becomes [1, 2, 3, 4]
// arr remains unaffected

```