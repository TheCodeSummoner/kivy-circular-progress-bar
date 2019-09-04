# Circular Progress Bar

This repository provides an implementation of a circular progress bar for the Python [kivy](https://kivy.org/#home)
GUI tool. Please refer to the in-code documentation or follow this *README* document to learn about the widget.

## Usage

The `CircularProgressBar` class extends kivy's `Widget` class, therefore it can be used in any scenarios as the
latter one. I have introduced a few new properties to simplify some of the common operations, however the standard
properties and methods available in the `kivy.uix.progressbar.ProgressBar` are still available. All the properties
can be specified using kivy markup language.

## Properties (copied from in-code docs)

    1. thickness - thickness of the progress bar line (positive integer)
    2. progress_colour - Colour value of the progress bar, check values accepted by kivy.graphics.Color
    3. progress_colour - Colour value of the background bar, check values accepted by kivy.graphics.Color
    4. cap_style - cap / edge of the bar, check the cap keyword argument in kivy.graphics.Line
    5. cap_precision - bar car sharpness, check the cap_precision keyword argument in kivy.graphics.Line
    6. max - maximum progress (value corresponding to 100%)
    7. min - minimum progress (value corresponding to 0%) - note that this sets the starting value to this value
    8. value - progress value, can you use it initialise the bar to some other progress different from the minimum
    9. widget_size - size of the widget, use this to avoid issues with size, width, height etc.
    10. label - kivy.graphics.Label textually representing the progress - pass a label with an empty text field to
    remove it, use "{}" as the progress value placeholder (it will be replaced via the format function)
    11. value_normalized - get the current progress but normalised, or set it using a normalised value

Please see the examples to understand how each property works.

## Examples

The `_Example` class showcases 3 different loading bars - simply run the module to see it in action. Here is a short gif
capturing how it looks like:

## Autorship

Kacper Florianski