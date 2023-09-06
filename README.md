# Preferences extension
Preferences extension is a library that simplifies the use and extends the capabilities of SharedPreferences.
With this library, using SharedPreferences has become much easier, saving and getting data is implemented using extensions.

# Basic usage

```kotlin
// Save data
val text = "text"
text.saveData("your-key", this, "your-preferences")
```
```kotlin
// Get data
val text = "text"
text.getData("your-key", this, "your-preferences")
```
# Using configurations
In this library, you can use configurations to customize the use of preferences.
In the configuration list, you must specify the following parameters

- Context
- Preferences name
- Context mode
- Async status

The configuration is created using a list:

```kotlin
// Create a configuration
val config: List<Any> = listOf(
            this,
            "your-preferences",
            Context.MODE_PRIVATE,
            true
        )
```
After that, you can save and get data.

```kotlin
// Save data
val text = "text"
text.saveDataWithConfig(config, "your-key")
```

```kotlin
// Get data
val text = "text"
text.getDataWithConfig(config, "your-key")
```
