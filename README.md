# Frame

Program draws an animation of a frame pulsing with text in center of the screen.

Supposed to be ran on DOSBox

# Build program
```powershell
    tasm /la vram.asm
    tlink /t vram.obj
```

# Run program

## Format
```powershell
    vram.com <FrameStyle> <FrameWidth> <FrameHeight> <YourText>
```

## Frame styles
```text
0 - custom frame style
1 - normal frame with gray bg
2 - pink hearts
3 - red strange symbols
4 - blue stupid symbols
5 - funny yellow faces on red bg
5 or bigger - it will be set to 1
```
### Custom style
```powershell
    vram.com 0 <Nine symbols (check example)> <FrameWidth> <FrameHeight> <YourText>
```
Important: if used frame style 0 (custom) any 9 letters after will be recognized as symbols of a frame

## Example
Draw a frame with pink hearts, size=30*7 with text "Privet, Mir!"
```powershell
    vram.com 1 30 7 Privet, Mir!
```
![example](https://github.com/andredze/asm_vram/raw/master/example.png)

## Example of custom style
Draw a frame with symbols: "abcd!f123" and text "HelloJopa"
```powershell
    vram.com 0 abcd!f123 20 5 HelloJopa
```
![custom_style](https://github.com/andredze/asm_vram/raw/master/custom_style.png)
