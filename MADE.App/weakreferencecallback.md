# WeakReferenceCallback class

> Namespace: MADE.App

Defines a model for providing a weak referenced callback.

```csharp
public sealed class WeakReferenceCallback
```

## Supported platforms

| Platform | Version |
| --- | --- |
| .NET Standard | 2.0 |
| Xamarin.Android | 8.1 |
| Xamarin.iOS  | 1.0 |
| UWP | 10.0.16299 | 

## Constructors

### WeakReferenceCallback(Delegate, Type)

#### Parameters
##### action (Delegate)
The callback action.

##### callbackType (Type)
The expected type for the callback.

## Properties

### IsAlive

Gets a value indicating whether the callback is alive.

```csharp
public bool IsAlive { get; }
```

### Type

Gets the expected type for the callback.

```csharp
public Type Type { get; }
```

## Methods

### Invoke(object)

Invokes the callback with the specified parameter.

```csharp
public void Invoke(object param);
```

#### Remarks
InvalidOperationException thrown if the weak reference is no longer alive.

#### Parameters
##### param (object)
The parameter to pass to the callback.