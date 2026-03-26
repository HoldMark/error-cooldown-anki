# Error Cooldown

An Anki addon that temporarily freezes the rating buttons when you type a **wrong answer** on a `{{type:FieldName}}` card. After the freeze expires you pick the rating yourself — so you can't accidentally click through without thinking.

## How it works

1. You see the answer on a typing card.
2. If your typed answer is wrong (and the rating is not *Again*), the ease buttons are disabled and dimmed for `1000 ms`.
3. After the timer fires, the buttons become active again and you choose the rating manually.
4. On the next card the state resets.

## Configuration

Edit the addon config via **Tools → Add-ons → error_cooldown → Config**.

| Key | Type | Default | Description |
|---|---|---|---|
| `decks` | `list[str]` | `[]` | Deck names the freeze applies to. Supports sub-decks (`Parent::Child`). Empty list means **all decks**. |
| `check_version` | `bool` | `true` | When `true`, the addon only runs if the current Anki version is in `required_versions`. Set to `false` to run on any version. |
| `required_versions` | `list[str]` | `["25.9.2"]` | Anki versions the addon is confirmed to work with. Ignored when `check_version` is `false`. |

### Example `config.json`

```json
{
    "decks": [
        "English::Typing",
        "Math::Multiplication"
    ],
    "check_version": true,
    "required_versions": ["25.09.2", "25.10.0"]
}
```

### License

This project is dual-licensed:

| Use case | License | Cost |
|---|---|---|
| Open-source project | [GPL v3](LICENSE) | Free |
| Personal / educational use | [GPL v3](LICENSE) | Free |
| Closed-source / commercial product | [Commercial](LICENSE-COMMERCIAL.md) | Contact author |

---

### Open Source

Free to use under the [GNU GPL v3](LICENSE) — but you must
open-source your own code too.

### Commercial

If you use this in a proprietary or closed-source product,
you need a commercial license.

Contact: **prodius.mark@gmail.com**
GitHub: [@HoldMark](https://github.com/HoldMark)

---

By contributing to this project, you agree to the [CLA](CLA.md).

---

Copyright (C) 2026 HoldMark (MarkelloFx2) <prodius.mark@gmail.com>

