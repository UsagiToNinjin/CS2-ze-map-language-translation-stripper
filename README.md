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

## Lyrics

For maps that contain music, the song title, artist, and lyrics have been added for display.

Both the original lyrics and their romanized version are displayed. This feature is implemented through the `env_hudhint` entity.

For information on this feature, please refer to the `// add lyric entity` comment in `default_ents.jsonc`.

## Lua Script

Lua script functionality has been converted to work without requiring any Lua script execution plugins.

This is achieved by replacing the `RunScriptCode` input with `KeyValue` operations.

This feature is applied to all Stripper configurations whose commit messages contain `convert lua script`.
