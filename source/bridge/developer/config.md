# Extension Configuration

Creating configuration for extensions is simple. 
Just create a class that subclasses `ExtensionConfig`, and start adding settings.

```python
from core.config import ExtensionConfig, ConfigKey

class MyExtensionConfig(ExtensionConfig, base_key="my_extension"):
    my_setting = ConfigKey(str, "default_value")
    another_setting = ConfigKey(int, 123)
    required_setting = ConfigKey(str)
```

This will validate and add your configuration to the main config file automatically when created.

You can then access your settings like so:

```python
MyExtensionConfig.my_setting
MyExtensionConfig["my_setting"]
```

Updating a setting will automatically push it to the config file:

```python
MyExtensionConfig.my_setting = "new_value"
```

If you, for some reason, need to access the base settings, you can do so by importing the following from `core.config`:
- `ServerConfig`
- `AccountConfig`
- `DiscordConfig`
- `RedisConfig`
- `SettingsConfig`
