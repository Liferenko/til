## asdf as meta-alt-shift-ctrl

UPD 2025-07-24
#### Karabiner config for howerow
```json
{
    "description": "Hold j/f = Ctrl, a/; = Shift, d/k = Cmd, s/l = Option; tap = normal",
    "manipulators": [
        {
            "from": {
                "key_code": "j",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "j" }],
            "to_if_held_down": [{ "key_code": "left_control" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "f",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "f" }],
            "to_if_held_down": [{ "key_code": "left_control" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "a",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "a" }],
            "to_if_held_down": [{ "key_code": "left_shift" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "semicolon",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "semicolon" }],
            "to_if_held_down": [{ "key_code": "left_shift" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "d",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "d" }],
            "to_if_held_down": [{ "key_code": "left_command" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "k",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "k" }],
            "to_if_held_down": [{ "key_code": "left_command" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "s",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "s" }],
            "to_if_held_down": [{ "key_code": "left_option" }],
            "type": "basic"
        },
        {
            "from": {
                "key_code": "l",
                "modifiers": { "optional": ["any"] }
            },
            "to_if_alone": [{ "key_code": "l" }],
            "to_if_held_down": [{ "key_code": "left_option" }],
            "type": "basic"
        }
    ]
}
```

parameters:
to_if_alone_timeout_milliseconds: 140
to-if_held_down_threshold_milliseconds: 100
---



- Follow - https://github.com/rvaiya/keyd
- use example config from here (updated ctrl+hjkl)https://github.com/argenkiwi/kenkyo/blob/main/keyd/default.conf



located in `/etc/keyd/default.conf`

