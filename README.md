EEG
===

Code to read EEG data via a soundcard or Arduino.

NOTE: This code is no longer being updated. Feel free to make whatever changes you want to it, but don't report back with errors.


A note from Marquis de Geek
===========================

I thought I'd spend a few moments making the READ_EEG code compile, and work. I've only tested with microphone input as (of yet) I've not had time to build the EEG module. But, it samples the input and displays it properly.

The configurable parts of interest are:

```
Line 54: final int timeLength = 240;
Size of the sampling buffer, when used.

Line 93 : int readDataFrom = INPUT_FROM_BUFFERED_AUDIO;
Determines whether to read directly from the audio input (default), a buffered version, or from the serial port (for when the Arduino passes the data across the serial)

Line 104: int serialIndex = 0;
Which of your serial ports is used

Line 152: int mixerID = 3;
Which of the audio input devices is to be used
```


