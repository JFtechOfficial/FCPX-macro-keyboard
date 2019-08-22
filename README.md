# FCPX Macro Keyboard
[![banner](https://dl.dropboxusercontent.com/s/kjas0ec2ibrgzes/banner-FCPX-macro-keyboard.png?dl=1 "banner with JFtech logo & social")](https://linktr.ee/jftechofficial)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) 

Convert any kind of USB keyboard into a fully programmable macro keyboard and add functions for FCPX. 

Integrate MIDI controls using your smartphone/tablet.

This repo will provide you with **instructions** on how to set it all up, along with **custom keycaps designs** for your macro keyboard and some **scripts** I personally use during videoediting. You can also read this in [Italiano🇮🇹](README-it-IT.md)


## 🚀 Getting started

<details>
 <summary><strong>Table of Contents</strong> (click to expand)</summary>

* [Getting started](#-getting-started)
* [Configuration](#️-configuration)
* [Resources](#-resources)
* [Contributing](#-contributing)
* [Support Me!](#-support-me)
* [Release History](#️-release-history)
* [License](#-license)
</details>

### Requirements

* [CommandPost](https://commandpost.io)

* [USB Overdrive](http://www.usboverdrive.com/USBOverdrive/News.html)

* [TouchOSC(paid) + TouchOSC Editor + TouchOSC Bridge](https://hexler.net/products/touchosc)


## ⚙️ Configuration
Make sure:
- you have a dedicated Settings in USB Overdrive for the keyboard you intend to use as macro keyboard 
- that Settings entry is selected in the dropdown menu.

### Macro Keyboard
if you want to assign a FCPX shortcut to a key:
* Open USB Overdrive Settings panel
* Select a key (add a new one if needed)
* Select "Press key" and assign the shortcut


if you want to assign CommandPost actions to a key:
* Open CommandPost Shortcuts preference panel
* Select a new action
* Select modifiers and key (make sure it does not collide with FCPX own sortcuts)
* Open USB Overdrive Settings panel
* Select a key (add a new one if needed)
* Select "Press key" and assign the same shortcut 


if you have more advanced needs (concatenating multiple CommandPost actions / FCPX shortcuts, calling CommandPost functions via Lua, you have no modifiers+key combinations left):
* Open USB Overdrive Settings panel
* Select a key (add a new one if needed)
* Select "Execute AppleScript" and write the script (see [Outro.scpt](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Outro.scpt) for an example)


### MIDI Controls
* Create a new user interface with TouchOSC Editor and send it to your device <strong>OR</strong> use one of the already made UI in the TouchOSC app
* Make sure you have both TouchOSC and TouchOSC Bridge up and running
* Open CommandPost MIDI preference panel
* Select a new action
* Click on learn and use the corresponding UI element on your TouchOSC app


## 📚 Resources

The [Keyboard-layout file](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Keyboard-layout.psd) contains custom made keycaps you can print on adhesive paper and stick on your orignial keycaps.

The keycap design is kept as simple and accessible as possible. It always contains text in the center portion of the key to describe the key function (with full words or abbreviations) and a symbol in the top left corner to represent what the key originally was, in case you want to use the keyboard as standard keyboard once again. The font is the one used by Apple in its own keyboards. The shapes are ment to create contrast with the text and add meaning (that matches with the keycap function). The background colors are chosen from [Apple Accessible + Vibrant macOS system color palette](https://developer.apple.com/design/human-interface-guidelines/macos/visual-design/color/). Color gradients are trendy these days, but printers don't get along with them, and, since the keycaps have to be printed, solid colors were a better choice.
Background colors were assigned as such:

| COLOR         | ASSIGNED TO   | NOTES |
| :-----------: |---------------| ------|
| Blue          | Video         | Video role is blue. Everything you can inspect in the Video inspector |
| Green         | Audio         | Music role is green. Everything you can inspect in the Audio inspector |
| Grey          | Transition    | Transitions are grey. Everything you can inspect in the Transition inspector |
| Orange        | FCPX layout   | Everything you can change about FCPX layout (es. workspaces) |
| Purple        | Title/Generator | Title role is purple. Everything you can inspect in the Generator inspector |
| Red           | Clips, media & other | Here is everything left |

The currently available keycap designs are:

| KEYCAP        | NOTES |
| :-----------: | ------|
| Add-Blend          | [Set Blend Mode to Add](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Blend%20mode.scpt) |
| Adjustment-Layer         | Add an Adjustment Layer title to the timeline |
| Audio-Denoiser          | [Apply Audio Denoiser effect to an audio clip and open Audio inspector](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Audio%20Denoiser.scpt) |
| Behind-Blend        | [Set Blend Mode to Behind](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Blend%20mode.scpt) |
| Brush        | Add Brush title to the timeline |
| Cam-Rig        | Add Cam Rig title to the timeline |
| Chroma-Key           | Apply Keyer effect to a video clip |
| Custom-Generator        | Add Custom generator to the timeline |
| Custom-Title          | Add Custom title to the timeline |
| Draw-Mask       | Apply Draw Mask effect to a video clip |
| Detach-Audio           | Detach audio from a clip |
| fit      | Set video player size to fit (not working yet) |
| Folder-BK        | Open Backup folder in Finder |
| Folder-YT        | Open YouTube folder in Finder |
| Font          | Apply a given font to a text |
| Grid          | Add Guides title to the timeline |
| Ink          | Add Ink title to the timeline |
| Line-Solid        | Add Line Solid title to the timeline |
| Lut           | Apply Lut effect to a video clip |
| MVMT1&2        | [Open a given submenu in the title and generator sidebar](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/MVMT.scpt) |
| Normal-Blend    | [Set Blend Mode to Normal](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Blend%20mode.scpt) |
| Outro        | [Add Outro generator at the end of the timeline and wrap it in a new compound clip called "Outro"](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Outro.scpt) |
| Point-Tracker           | Apply Point Tracker effect to a video clip |
| Slide-Right     | Apply Slide Right transition to a video clip|
| Slide-Left     | Apply Slide Left transition to a video clip|
| Speed       | Open retiming menu of a clip |
| Sync-Clips           | Syncronize selected clips |
| Vertical        | Add Vertical title to the timeline |
| Volume -∞        | Set a clip audio volume to -∞ dB |
| Volume 0.0        | Set a clip audio volume to 0.0 dB |
| Workspace-Color        | Set the workspace to your "color correction" workspace |
| Workspace-Cut        | Set the workspace to your "rough cut" workspace |
| Workspace-Effect        | Set the workspace to your "effects and refinements" workspace |
| 1x       | Set retiming of a clip back to 100% |
| 10%       | Set retiming of a clip to 10% |
| 150percent      | Set video player size to 150% (not working yet) |
| 2x       | Set retiming of a clip to 200% |
| 25%       | Set retiming of a clip to 25% |
| 4x       | Set retiming of a clip to 400% |
| 4pt-Blur           | Apply 4 Points Blur effect to a video clip |
| 50percent      | Set video player size to 50% (not working yet) |
| 50%       | Set retiming of a clip to 50% |
| 8x       | Set retiming of a clip to 800% |



Use the [Keyboard-layout file](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Keyboard-layout.psd) to preview and customize how you want to arrange your macro keys.
How to modify the layout:
1) modify keycap layer position
2) open keycap psd
3) change the character in the top left corner (should match the key it's covering)
4) save and close the keycap psd

If the keyboard layout you are using fits in an A4 paper sheet you are ready to print, otherwise you have to rearrange the keycap designs to make them fit.

Supported layouts (also A4-compatible):
* Apple en_US keyboard layout
* Apple en_International keyboard layout


## 🎁 Contributing
Do you want to help this project? You did some modification or created something new for this setup? Contribute!
Here you can find the contribution guidelines

### New Keyboard Layout
In order to add a new keyboard layout you must add to the [Keyboard-layout file](https://github.com/JFtechOfficial/FCPX-macro-keyboard/blob/master/Keyboard-layout.psd) the following layers:
* 1:1 scale keyboard layout 
* 1:1 scale keyboard layout mask that excludes any symbol on the "standard-sized" keys (keep "odd shaped" keys) 


### New/Modified Keycap Design
How to add a new keycap:
1) duplicate TEMPLATE layer
2) modify TEMPLATE copy layer position (should be covering a key)
3) open TEMPLATE copy psd
4) modify TEMPLATE copy psd
5) change the character in the top left corner (should match the key it's covering)
6) save and close the TEMPLATE copy psd
7) rename TEMPLATE copy and set it to visible

In order to keep the keycap designs consistent you should follow these guidelines:

***Design***

Do not obstruct top left corner (that's the spot for the keycap symbol!), keep the design centered, avoid adding design details near the canvas edges (when cutting the keycap from the paper, small errors could chip that detail away), align to guides. New design must be consistent with the current one.


***Colors***

Use one of the provided levels as background color for the keycap. Keep background colors consistent with their usage


***Text***

You must include text (in english). You can use full words or abbreviations. Use 30 pt San Francisco Heavy. Prefer capital letters, color black, white outline/background. It must be vertically centered and above any other layer.


***Shapes***

You must include simple shapes (fine details get lost during the printing phase). Prefer color white, use other colors only if it's necessary to convey meaning. Text and shapes should “merge” to be perceived as a single element that convey the meaning of the key.


### New Script
If you created a new script:
* test it
* be sure that the same function cannot be achieved via FCPX shortcuts
* be sure that the same function cannot be achieved via CP actions
* open a pull request


For other information please see [CONTRIBUTING.md](./CONTRIBUTING.md).


## 💵 Support Me!

 [![ko-fi](https://www.ko-fi.com/img/donate_sm.png)](https://ko-fi.com/Y8Y0FW3V)



## 🗓️ Release History

* 22/08/2019 - 1.0 - first release


## 🎓 License

[MIT](http://webpro.mit-license.org/)


