# Circular Progress Bar

This repository provides an implementation of a circular progress bar for the Python [kivy](https://kivy.org/#home)
GUI tool. Please refer to the in-code documentation or follow this *README* document to learn about the widget.

## Usage

The `CircularProgressBar` class extends kivy's `Widget` class, therefore it can be used in any scenarios as the
latter one. I have introduced a few new properties to simplify some of the common operations, however the standard
properties and methods available in the `kivy.uix.progressbar.ProgressBar` are still available. All the properties
can be specified using kivy markup language.

## Properties (copied from in-code docs)

1. `thickness` - thickness of the progress bar line (positive integer)
2. `cap_style` - cap / edge of the bar, check the cap keyword argument in kivy.graphics.Line
3. `cap_precision` - bar car sharpness, check the cap_precision keyword argument in kivy.graphics.Line
4. `progress_colour` - Colour value of the progress bar, check values accepted by kivy.graphics.Color
5. `background_colour` - Colour value of the background bar, check values accepted by kivy.graphics.Color
6. `max` - maximum progress (value corresponding to 100%)
7. `min` - minimum progress (value corresponding to 0%) - note that this sets the starting value to this value
8. `value` - progress value, can you use it initialise the bar to some other progress different from the minimum
9. `widget_size` - size of the widget, use this to avoid issues with size, width, height etc.
10. `label` - kivy.graphics.Label textually representing the progress - pass a label with an empty text field to remove it, use "{}" as the progress value placeholder (it will be replaced via the format function)
11. `value_normalized` - get the current progress but normalised, or set it using a normalised value

Please see the examples to understand how each property works.

## Examples

The `_Example` class showcases 3 different loading bars - simply run the module to see it in action. Here is a short gif
capturing how it looks like:

![Amazing progress bars spinning right round](https://github.com/TheCodeSummoner/kivy-circular-progress-bar/blob/master/animated.gif "Circular Progress Bar example")

The code styling the progress bars is available, but I will additionally include it here for convenience:

```
#:import Label kivy.core.text.Label           
#:set _label Label(text="\\nI am a label\\ninjected in kivy\\nmarkup string :)\\nEnjoy! --={}=--")
#:set _another_label Label(text="Loading...\\n{}%", font_size=10, color=(1,1,0.5,1), halign="center")
FloatLayout:
    CircularProgressBar:
        pos: 50, 100
        thickness: 15
        cap_style: "RouND"
        progress_colour: "010"
        background_colour: "001"
        cap_precision: 3
        max: 150
        min: 100
        widget_size: 300
        label: _label
    CircularProgressBar
        pos: 400, 100
    CircularProgressBar
        pos: 650, 100
        cap_style: "SqUArE"
        thickness: 5
        progress_colour: 0.8, 0.8, 0.5, 1
        cap_precision:100
        max: 10
        widget_size: 100
        label: _another_label
```

## Autorship

Kacper Florianski
