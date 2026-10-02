# Wallpaper Engine Setup Guide

This project has been set up to work as a web-based wallpaper in [Wallpaper Engine](https://store.steampowered.com/app/431960/Wallpaper_Engine/). By importing this repository, you can display the procedurally generated Shan Shui landscape directly on your desktop!

## Prerequisites

1.  **Wallpaper Engine** installed from Steam.
2.  A local copy of this repository on your computer.

## How to Test and Use in Wallpaper Engine

1.  Open the **Wallpaper Engine** application.
2.  In the main interface, click on the **"Wallpaper Editor"** button located at the bottom (or access it by right-clicking the tray icon and selecting "Create Wallpaper").
3.  In the welcome screen of the Wallpaper Editor, select **"Open existing project"** (or click the folder icon).
4.  Browse to the folder where you have cloned or downloaded this repository.
5.  Select the `project.json` file inside the root folder.
6.  The wallpaper will now load in the editor. You can use the settings panel on the right side to test out the custom user properties:
    *   **Auto-scroll**: Toggles the automatic scrolling on or off.
    *   **Scroll Speed**: Adjusts how fast or far it scrolls each tick.
    *   **Show UI Elements**: Hides or shows the original web UI buttons.

## Applying the Wallpaper

1.  While in the Wallpaper Editor, go to the top menu and click **File -> Apply Wallpaper**.
2.  This will immediately apply the wallpaper to your desktop so you can see how it looks and performs outside of the editor.

## Publishing to the Steam Workshop (Optional)

1.  If you would like to share this wallpaper with others on the Steam Workshop, go to the top menu in the Wallpaper Editor and click **Steam -> Prepare for Publishing**.
2.  Fill in any missing details, such as a Title, Description, and tags.
3.  Click **Publish** (or "Update" if you are updating an existing submission).
4.  Once the upload finishes, the wallpaper will be available on your Steam Workshop page.

## Notes on the Structure

*   `project.json`: Contains the configuration settings required by Wallpaper Engine to recognize this folder as a wallpaper project. It also defines the custom properties exposed to the user.
*   `index.html`: The main file of the wallpaper. It has been slightly modified to include a `window.wallpaperPropertyListener`, which receives updates from the Wallpaper Engine interface and alters the wallpaper's behavior on the fly.
