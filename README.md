# Worm Gear Crankshaft

An interactive Unity and Vuforia project for exploring a worm-gear crankshaft assembly in augmented reality. The project combines a 3D mechanical model, animation, touch interaction, and image-target tracking so the mechanism can be inspected from different angles on a compatible Android device.

## Highlights

- Interactive 3D worm-gear crankshaft model.
- Vuforia image-target based AR experience.
- Touch gestures for rotating and inspecting the assembly.
- Animated mechanical components.
- Android build configuration included in the Unity project.

## Requirements

- Unity **2022.3.51f1** (LTS recommended).
- Android Build Support, including SDK/NDK and OpenJDK modules.
- A Vuforia Engine license key configured for your development environment.
- Android device with camera access for AR testing.

## Getting started

1. Clone this repository.
2. Open the repository root in Unity Hub using Unity `2022.3.51f1`.
3. If Unity reports a missing Vuforia package, obtain Vuforia Engine `11.4.4` from PTC and place the package archive at `Packages/com.ptc.vuforia.engine-11.4.4.tgz`.
4. Open `Assets/Scenes/WormGear.unity`.
5. Configure the Vuforia license key and Android Player settings for your device.
6. Press **Play** to test in the Editor, or build and run to an Android device.

## Repository layout

| Path | Description |
| --- | --- |
| `Assets/3D` | Worm-gear crankshaft models and animation assets |
| `Assets/Scenes/WormGear.unity` | Main interactive scene |
| `Assets/StreamingAssets/Vuforia` | Vuforia target databases and runtime data |
| `Assets/Plugins` | Lean Touch and supporting interaction components |
| `ProjectSettings` | Unity project and platform settings |
| `Build` | Local build output; ignored by Git |

## Android build

In Unity, select **File → Build Settings**, choose **Android**, add `Assets/Scenes/WormGear.unity` to the build scenes, then select **Build** or **Build And Run**. The generated APK is intentionally treated as a local build artifact; reproducible builds should be produced from the Unity project.

## Vuforia target setup

The project includes Vuforia target data under `Assets/StreamingAssets/Vuforia` and target image assets under `Assets/Editor/Vuforia`. Use the target image associated with the project when testing, and make sure the target database is enabled in the Vuforia configuration.

## Notes

- The Vuforia `.tgz` package is not committed because it is larger than GitHub's standard 100 MB per-file limit. Follow the setup step above to restore it locally.
- Generated folders such as `Library`, `Logs`, and `UserSettings` are excluded from version control because Unity recreates them.
- This repository contains project assets and third-party packages. Review their individual licenses before redistribution.

## License

No open-source license has been selected yet. Unless a license is added, copyright remains with the project owner and reuse should be requested from the owner.

