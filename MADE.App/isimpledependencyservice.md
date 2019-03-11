# ISimpleDependencyService interface

> Namespace: MADE.App.Dependency

Defines an interface for a simple dependency service.

```csharp
public interface ISimpleDependencyService
```

## Supported platforms

| Platform | Version |
| --- | --- |
| .NET Standard | 2.0 |
| Xamarin.Android | 8.1 |
| Xamarin.iOS  | 1.0 |
| UWP | 10.0.16299 | 

## Methods

### Register<TClass>()

Registers the given type.

```csharp
void Register<TClass>() where TClass : class;
```

### Register<TInterface, TClass>()

Registers the given interface and associated type.

```csharp
void Register<TInterface, TClass>()
            where TInterface : class 
            where TClass : class, TInterface;
```

### Register<TClass>(Func<TClass>)

Registers the given type with the given factory.

```csharp
void Register<TClass>(Func<TClass> factory);
```

#### Parameters
##### factory (Func<TClass>)
The factory for creating instances of the given type.

### Register<TClass>(string, Func<TClass>)

Registers the given type with the given factory and associates it with the given key.

```csharp
void Register<TClass>(string key, Func<TClass> factory);
```

#### Parameters
##### key
The key associated with the registration.

##### factory (Func<TClass>)
The factory for creating instances of the given type.

### GetInstance<TService>()

Gets an instance of the given service type that is registered.

```csharp
TService GetInstance<TService>();
```

#### Returns
A registered instance of the given service.

### GetInstance<TService>(string)

Gets an instance of the given service type that is registered.

```csharp
TService GetInstance<TService>(string key);
```

#### Parameters
##### key
The key of the instance to retrieve.

#### Returns
A registered instance of the given service.

### IsRegistered<T>()

Checks whether the given type is registered with the service.

```csharp
bool IsRegistered<T>();
```

#### Returns
True if the type is registered; otherwise, false.

### IsRegistered<T>(string)

```csharp
bool IsRegistered<T>(string key);
```

#### Parameters
##### key
The key of the instance to check is registered.

#### Returns
True if the type is registered; otherwise, false.
