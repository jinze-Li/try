# Chicken Feather vs White

An iOS mobile game prototype with a multi-mode shell and a playable FPS mode. The project uses SwiftUI for menus and app structure, then SpriteKit for the real-time combat scene.

> Working title in Chinese: Xiao Ji Mao vs Xiao Bai.

## Features

- Mode menu for a larger multi-mode game
- Playable FPS mode
- Two fighters: Xiaojimao and Xiaobai
- Left virtual joystick for forward, backward, left, and right movement
- Right fire button
- Drag on the screen to turn the reticle
- Hit zones with different damage values
- Both fighters start with 100 health
- A fighter loses when health reaches 0
- Simple enemy chase and shooting behavior
- Original procedural placeholder character art
- Restart flow after victory or defeat

## Modes

| Mode | Status |
| --- | --- |
| FPS Mode | Playable prototype |
| Survival | Placeholder for a future mode |
| Duel | Placeholder for a future mode |

## Hit Damage

| Zone | Damage |
| --- | ---: |
| Head | 35 |
| Torso | 20 |
| Legs | 12 |

## Run

1. Open `ChickenFeatherVsWhite.xcodeproj` in Xcode.
2. Choose an iPhone simulator or a real iPhone.
3. Press Run.

Recommended environment:

- macOS with Xcode 16 or newer
- iOS 17 target or newer

## Project Layout

```text
ChickenFeatherVsWhite.xcodeproj/
ChickenFeatherVsWhite/
  ChickenFeatherVsWhiteApp.swift
  GameView.swift
  GameScene.swift
  Assets.xcassets/
```

`GameView.swift` owns the mode menu and restart flow. `GameScene.swift` owns the FPS gameplay, combat rules, joystick input, aiming, shooting, hit detection, and procedural placeholder characters.

## Character Reference Note

I searched the web for the character names, the game title, and related image-reference keywords. Text search did not return a clear official source for this exact title. Image search returned general yellow/white chick references, including chick photos, chick toys, and illustrated chicken pages, but not a safely reusable official Xiaojimao/Xiaobai character sheet. The prototype therefore uses original placeholder art:

- Xiaojimao: yellow chick, three top feathers, orange beak
- Xiaobai: white round character with blue accents

If you have official or licensed art, add it to `ChickenFeatherVsWhite/Assets.xcassets` and replace the procedural drawing in `CharacterNode` with texture sprites.

More detail: `docs/character-research.md`.

## Continuous Integration

The repository includes a GitHub Actions workflow at `.github/workflows/ios.yml`. After pushing to GitHub, it builds the app on a macOS runner with `xcodebuild` and the shared Xcode scheme.

## Acceptance Checklist

See `docs/acceptance.md` for a requirement-by-requirement checklist that maps the original request to files in this repository.

## GitHub Setup

This folder is ready to become a GitHub repository. From the project folder:

```bash
git init
git add .
git commit -m "Create iOS FPS prototype"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```
