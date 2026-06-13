# Adapter Studio Migration

Active Adapter Studio development has moved to
[Foundation Models Framework Lab](https://github.com/rudrankriyam/Foundation-Models-Framework-Lab).
The standalone repository remains available as a historical snapshot and will
not receive further fixes or features.

## New Locations

| Standalone component | Foundation Lab location |
| --- | --- |
| macOS comparison app | [`Foundation Lab/AdapterStudio`](https://github.com/rudrankriyam/Foundation-Models-Framework-Lab/tree/main/Foundation%20Lab/AdapterStudio) |
| Training toolkit CLI | [`Tools/AdapterStudio`](https://github.com/rudrankriyam/Foundation-Models-Framework-Lab/tree/main/Tools/AdapterStudio) |
| CLI tests | [`Tools/AdapterStudio/tests`](https://github.com/rudrankriyam/Foundation-Models-Framework-Lab/tree/main/Tools/AdapterStudio/tests) |
| Integration workflow | [`.github/workflows/adapter-studio.yml`](https://github.com/rudrankriyam/Foundation-Models-Framework-Lab/blob/main/.github/workflows/adapter-studio.yml) |

## Continue With Foundation Lab

```bash
git clone https://github.com/rudrankriyam/Foundation-Models-Framework-Lab.git
cd Foundation-Models-Framework-Lab
open FoundationLab.xcodeproj
```

On macOS, open the Adapter Studio workspace inside Foundation Lab to import a
`.fmadapter` package and compare it with the base system model.

## CLI Rename

The former `adapter-studio` command is now `fmas`.

```bash
cd Foundation-Models-Framework-Lab
python3 -m pip install -e Tools/AdapterStudio
fmas --help
```

Existing toolkit configuration remains compatible. The consolidated CLI also
adds automated tests, stricter validation, and reliable nonzero exit statuses
for failed toolkit commands.

## History

The standalone Git history was imported into Foundation Lab before integration,
so prior authorship and commits remain traceable in the active repository.
