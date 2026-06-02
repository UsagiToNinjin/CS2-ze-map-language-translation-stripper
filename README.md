# CS2 Zombie Escape Stripper

This Stripper configuration was created to improve gameplay convenience.

## Translation

Maps that display in-game messages in languages other than English have been modified to support multiple languages(including English)

Supported entities:

* `point_servercommand (say)`
* `point_worldtext`
* `env_hudhint`

This feature is only available for Stripper configurations whose commit messages contain keywords such as `language`>`other languages/...` or similar.

You can change the language by referring to the comments at the top of the `default_ents.jsonc` file.
Please enter the desired language serial number in the `overrideparam` value of `language_counter`.

```jsonc
{
    "outputname": "OnMapSpawn",
    "targetname": "language_counter",
    "inputname": "SetValue",
    "overrideparam": "1", // please enter the language serial number here
    "delay": 0.0,
    "timestofire": -1
}
```
