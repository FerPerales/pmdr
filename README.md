# pmdr

pmdr is an small wrapper for the awesome [pompom](https://github.com/knaveofdiamonds/pompom) command-line interface to use pomodoro
and make it work together with [rescue time](http://rescuetime.com) and their cool feature called FocusTime.

This script uses [IFTTT](http://ifttt.com) to trigger a custom action via [maker channel](https://ifttt.com/maker) which will be listening to two actions: `pomodoro_start` and `pomodoro_end`


## IFTTT Setup

* Get an [IFTTT account](https://ifttt.com/join) if you don't have one yet
* Activate the [maker channel](https://ifttt.com/maker)
* You will get a token. Take note and replace the `$IFTTT_KEY` in the `pmdr` file
* Add these two recipes to your IFTTT account:
  * [Start a FocusTime session]( https://ifttt.com/recipes/364500-start-a-15-minute-focustime-session). By default, a 15-minute session will be created, but can be customized.
  * [End current FocusTime session](https://ifttt.com/recipes/364499-end-current-focustime-session). Ends your current FocusTime session


## Script setup

* To make the script global, do the following:

```
chmod +x pmdr
sudo cp pmdr /usr/local/bin/pmdr
```

## Use

`pmdr start`

Starts a new 25-minute session in pompom and activate a 15-minute FocusTime session in RescueTime

`pmdr end`

Ends your current session in pompom and stops the current FocusTime session
