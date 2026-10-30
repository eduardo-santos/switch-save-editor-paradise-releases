# Shared "Find a value" fields

Fields that players found with **Find a value** and shared, so everyone else can edit them without searching. In the
app, open a game's **Find a value** screen and choose **Get shared fields for this game**.

## Share a field

Found a field that works? [Share it](https://github.com/eduardo-santos/switch-save-editor-paradise-releases/issues/new?template=share_field.yml).
The app shows each of your fields as *name · file · position · type*: copy that into the form, and say which game
version you tested it on.

## File format

One file per game, named after its title ID: `fields/<TITLE ID>.tsv`, for example `fields/010015100B514000.tsv`.
One field per line, with tabs between the columns. Lines starting with `#` are comments.

| Column | Example | Meaning |
| --- | --- | --- |
| Name | `Lives` | What players see in the app |
| File | `game_data.sav` | The file in the save, with its folder if it has one (`0/game_data.sav`) |
| Offset | `0x167C` | Where the value is in the file, in hexadecimal (`0x…`) or decimal |
| Type | `4` | `1` = 1-byte number, `2` = 2-byte number, `4` = 4-byte number, `5` = decimal number |
| Max | `99` | The highest value the app allows (`0` = the type's own limit) |

Fields only work for saves that aren't encrypted or checksummed, and offsets can move between game versions, so
every field should be tested on a real save first. Edited saves are always backed up by the app first.
