# Apple Dictionary

[![zh](https://img.shields.io/badge/lang-%E4%B8%AD%E6%96%87-blue)](https://github.com/wayneclub/Apple-Dictionary/blob/main/README.zh-Hant.md)

**NON-COMMERCIAL USE ONLY**

## DESCRIPTION

This project provides online dictionaries for convenient offline use, expands Apple's dictionary, and facilitates simultaneous searches across multiple dictionaries. Support dark mode and offline pronunciation.

| Name                                   | Language        | Link |
| -------------------------------------- | --------------- | ------ |
| Cambridge Dictionary                   | English-Chinese | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |
| Oxford Advanced Learner's Dictionary   | English-Chinese | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |
| Oxford Advanced Learner's Dictionary   | English-English | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |
| Oxford Collocation Dictionary          | English-English | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |
| Merriam-Webster's Dictionary           | English-English | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |
| Merriam-Webster's Learner's Dictionary | English-English | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |
| Merriam-Webster's Thesaurus            | English-English | [Download](https://1drv.ms/f/s!AnPUuUreZmM0jwtbZhCZvp0wP2dY?e=sSQZTq) |

## Build

1. Download **Dictionary Development Kit** from [Additional Tools for Xcode](https://developer.apple.com/download/all/) or [Additional_Tools_for_Xcode.dmg](https://github.com/wayneclub/Apple-Dictionary/releases/download/v1.0.0/Additional_Tools_for_Xcode_15.dmg)

2. Open `Additional_Tools_for_Xcode.dmg`

3. Create `Extras` folder in `/Library/Developer/`

    ```bash
    sudo  mkdir /Library/Developer/Extras
    ```

4. Copy `Dictionary Development Kit` into `/Library/Developer/Extras`

    ```bash
    sudo cp -r /Volumes/Additional\ Tools/Utilities/Dictionary\ Development\ Kit /Library/Developer/Extras
    ```

5. Download OtherResources from [releases](https://github.com/wayneclub/Apple-Dictionary/releases) and put it in the corresponding folder

6. Open dictionary folder (Drag folder to terminal)

    ```bash
    cd /Users/xxx/Apple-Dictionary/Cambridge\ English-Chinese\ Dictionary
    ```

7. Build and install.

    ```bash
    make; make install; make clean;
    ```

## USAGE

1. Download the dictionary, and unzip the file.
2. Put it into the Dictionaries folder on Mac. (~/Library/Dictionaries)
3. Open `Dictionary.app`, add custom dictionary in `Preferences`.
