# ME.Macros
Unity 3D Macros System

## Features

1. Source macros in script files
2. Source macros in text files

## Using
In any file (text or script) declare macros:

### Simple:

```C#
#region source macros MACROSNAME
var anyCode = 0;
++anyCode;
#endregion
```

### Advanced:

```C#
#region source macros MACROSNAME
var anyCode = 0;
++anyCode;
{someCode1}
{someCode2}
#endregion
```

In any file (where you want to use it):

### Simple:

```C#
#region macros MACROSNAME
#endregion
```

### Advanced:

```C#
#region macros MACROSNAME (someCode1: var a = "test";, someCode2: Debug.Log(a);)
#endregion
```

## Result:

### Simple:

```C#
#region macros MACROSNAME
/* This code is auto-generated
 * Do not change it
 */
var anyCode = 0;
++anyCode;
#endregion
```

### Advanced:

```C#
#region macros MACROSNAME (someCode1: var a = "test";, someCode2: Debug.Log(a);)
/* This code is auto-generated
 * Do not change it
 */
var anyCode = 0;
++anyCode;
var a = "test";
Debug.Log(a);
#endregion
```
