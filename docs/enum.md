<a name="Enum"></a>

## Enum
This is the common base class for all enumeration types. Enum constants are

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| name | <code>string</code> | The name of the enum constant, exactly as declared           in the enum declaration. |
| ordinal | <code>number</code> | An integer indicating the ordinal of this           enumeration constant (its position in its enum declaration, where           the initial constant is assigned a value of zero). |
| type | <code>string</code> | A string representing the type of this constant           (actually, the name of the class that this constant extends from). |
| _ | <code>string</code> | An alias to [Enum.toString](Enum.toString). This property offers           a short and convenient way of obtaining the string representation           of this constant. |


* [Enum](#Enum)
    * [new Enum()](#new_Enum_new)
    * _instance_
        * [.isConstantOf(anEnum)](#Enum+isConstantOf) ⇒ <code>boolean</code>
        * [.isSameTypeAs(that)](#Enum+isSameTypeAs) ⇒ <code>boolean</code>
        * [.compareTo(that)](#Enum+compareTo) ⇒ <code>number</code>
        * [.toString()](#Enum+toString) ⇒ <code>string</code>
    * _static_
        * [.values(...constants)](#Enum.values)
        * [.valueOf()](#Enum.valueOf) ⇒ <code>[Enum](#Enum)</code>
        * [.all()](#Enum.all) ⇒ <code>array</code>

<a name="new_Enum_new"></a>

### new Enum()
Enum types may not be instantiated through the new operator. The

**Throws**:

- <code>AssertionError</code> Whenever that one uses the new operator with an enum type.

<a name="Enum+isConstantOf"></a>

### enum.isConstantOf(anEnum) ⇒ <code>boolean</code>
Returns true whether this enum constant bellongs to the specified enum

**Kind**: instance method of <code>[Enum](#Enum)</code>  
**Returns**: <code>boolean</code> - True or false indicating waht is explained above.  

| Param | Type | Description |
| --- | --- | --- |
| anEnum | <code>[Enum](#Enum)</code> | Any enum class. |

<a name="Enum+isSameTypeAs"></a>

### enum.isSameTypeAs(that) ⇒ <code>boolean</code>
Returns true whether this constant bellongs to the same enum class of the

**Kind**: instance method of <code>[Enum](#Enum)</code>  
**Returns**: <code>boolean</code> - True or false indicating what is explained above.  

| Param | Type | Description |
| --- | --- | --- |
| that | <code>[Enum](#Enum)</code> | Any enum constant. |

<a name="Enum+compareTo"></a>

### enum.compareTo(that) ⇒ <code>number</code>
Compares this enum constant with the specified object for order (by using

**Kind**: instance method of <code>[Enum](#Enum)</code>  
**Returns**: <code>number</code> - A negative integer, zero or a positive integer following
**Throws**:

- <code>Error</code> If the preconditions mentioned above aren't satisfied.


| Param | Type | Description |
| --- | --- | --- |
| that | <code>[Enum](#Enum)</code> | An enum constant of the same type of this enum constant. |

<a name="Enum+toString"></a>

### enum.toString() ⇒ <code>string</code>
Returns a string representing this enum constant. By default, this method

**Kind**: instance method of <code>[Enum](#Enum)</code>  
**Returns**: <code>string</code> - String representation of this constant.  
<a name="Enum.values"></a>

### Enum.values(...constants)
Initializes this enum type, by creating the specified constant values. Each

**Kind**: static method of <code>[Enum](#Enum)</code>  
**Throws**:

- <code>AssertionError</code> If the invariants mentioned previously aren't respected.


| Param | Type | Description |
| --- | --- | --- |
| ...constants | <code>string</code> &#124; <code>object</code> | Rest parameters representing the enum declarations. If a          string is specified it will be the name of the constant. If the          enum declaration is an object, it must respect the following form:          ```js {name: {property1: value1, property2: value2, propertyN:          valueN}} ``` In other words, each enum declaration must be a plain          object with one and only one property (that will be the enum          constant's name) and a set of members (attributes and/or methods)          assigned to this property. Any violation to these invariants will          cause an AssertionError. |

<a name="Enum.valueOf"></a>

### Enum.valueOf() ⇒ <code>[Enum](#Enum)</code>
Returns the enum constant whose the result of an invokation of the method

**Kind**: static method of <code>[Enum](#Enum)</code>  
**Returns**: <code>[Enum](#Enum)</code> - The enum constant whose #toString() matches the specified
**Throws**:

- <code>AssertionError</code> If the provided name is not a string or if there is no an enum

<a name="Enum.all"></a>

### Enum.all() ⇒ <code>array</code>
Returns an array containing all declared constants of this enum type.

**Kind**: static method of <code>[Enum](#Enum)</code>  
**Returns**: <code>array</code> - Array with all constants that bellong to this enum.  