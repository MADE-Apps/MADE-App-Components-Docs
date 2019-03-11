# NSObjectExtensions class

> Namespace: MADE.App.Extensions

Defines a collection of extensions for iOS NSObject values.

```csharp
public static class NSObjectExtensions
```

## Supported platforms

| Platform | Version |
| --- | --- |
| Xamarin.iOS  | 1.0 |

## Static Methods

### SetAssociatedObject(this NSObject, NSString, NSObject)

Associates the given value with the given NSObject by the given key.

```csharp
public static void SetAssociatedObject(this NSObject nsObject, NSString key, NSObject value);
```

#### Example

This example shows how you might associated a value, such as adding a tag to a view.

```csharp
NSNumber myProperty = new NSNumber(1);

view.SetAssociatedObject("MyCustomProperty", myProperty);
```

#### Parameters
##### nsObject (NSObject)
The object to associated the value with.

##### key (NSString)
The key for the associated value.

##### value (NSObject)
The value to associate.

### GetAssociatedObject(this NSObject, NSString)

Gets the associated value from the given NSObject by the given key.

```csharp
public static object GetAssociatedObject(this NSObject nsObject, NSString key);
```

#### Example

This example shows how you might retrieve an associated value, such as a custom tag on a view.

```csharp
NSNumber myProperty = new NSNumber(1);
object associatedObject = view.GetAssociatedObject("MyCustomProperty");
if (associatedObject != null)
{
    myProperty = (NSNumber)associatedObject;
}
```

#### Parameters
##### nsObject (NSObject)
The object to retrieve the associated value from.

##### key (NSString)
The key to retrieve a value for.

#### Returns
The associated value.