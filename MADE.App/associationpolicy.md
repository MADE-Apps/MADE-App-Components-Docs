# AssociationPolicy enum

> Namespace: MADE.App.Enums

Defines values to specify the behavior of an association.

```csharp
public enum AssociationPolicy
```

## Supported platforms

| Platform | Version |
| --- | --- |
| Xamarin.iOS  | 1.0 |

## Fields

| Enum Value | Int Value | Description |
| --- | --- | --- |
| Assign | 0 | Specifies a weak reference to the associated object. |
| RetainNonAtomic | 1 | Specifies a strong reference to the associated object, and that the association is not made atomically. |
| CopyNonAtomic | 3 | Specifies that the associated object is copied, and that the association is not made atomically. |
| Retain | 01401 | Specifies a strong reference to the associated object, and that the association is made atomically. |
| Copy | 01403 | Specifies that the associated object is copied, and that the association is made atomically. |