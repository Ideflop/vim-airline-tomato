# vim-airline-tomato

  
vim-airline-tomato is a Vim extension that allows users to easily apply the [Pomodoro Technique](http://en.wikipedia.org/wiki/Pomodoro_Technique) in their editor. It is a fork of [Zuckonit](https://github.com/Zuckonit/vim-airline-tomato) and is based on [vim-airline](https://github.com/vim-airline/vim-airline) plugin.

With vim-airline-tomato, users can start and stop a Pomodoro timer and see the current time and remaining time displayed in the Vim status line. The extension also supports customizing the working and rest times, as well as the text displayed for each phase.

## Features

- Easy application of the Pomodoro Technique in Vim
- Customizable working and rest times
- Clock and countdown display options
- Automatic reset of the Pomodoro count after a specified number of Pomodoros
  
## Installation

To install vim-airline-tomato, use one of the following methods:

Using Vim's native package manager
```
git clone https://github.com/Ideflop/vim-airline-tomato.git ~/.vim/pack/plugins/start/vim-airline-tomato/
```

Using a plugin manager (e.g. Vundle, Pathogen)

Refer to the documentation of your chosen plugin manager for instructions on how to install vim-airline-tomato.
   
## Configuration

If you want to change the working time:
```
let g:tomato#interval = 60 * 60
```
  
If you wat to change rest time:
```
let g:tomato#rest_time = 20 * 60
```
  
If you want to change working text:
```
let g:tomato#remind = "🍅"
```
  
If you want to change rest text:
```
let g:tomato#restinfo = "⏳"
```

If you want to enable clock:
```
let g:tomato#show_clock = 1
```

If you want to show a count down:
```
let g:tomato#show_clock = 1  
let g:tomato#show_count_down = 1 
```

## Usage

To start the Pomodoro timer and display it in the status line, run the following command in Vim:

``` 
:call tomato#start()
```

Note that the timer will continue to run even when Vim is not open, so the next time you open Vim the timer will still be running and displayed in the status line.

To stop the Pomodoro timer and remove it from the status line, run the following command in Vim:

```
:call tomato#stop()
```

To reset the Pomodoro count to 1, run the following command in Vim:

```
:call tomato#reset()
```
  
Set auto reset when number over a value
```
let g:tomato#auto_reset_num = 24 (here put the number you wanna set)  
```
if the ``` g:tomato#auto_reset_num = -1 ``` , then the auto reset will be forbidden  
if there is no ``` g:tomato#auto_reset_num``` in your config, the default ``` auto_reset_num is 24 * 60 / g:tomato#interval ```, the total tomato numbers of one day.


## troubleshooting

If you encounter issues while using vim-airline-tomato, it may be necessary to install certain fonts:

[Airline](https://github.com/bling/vim-airline): The extension is based on vim-airline (like powerline, but faster and with a deeper KISS flavor)
[powerline-font](https://github.com/Lokaltog/powerline-fonts): if you use wild char's, you may need install powerline font.

[pomicons](https://github.com/gabrielelana/pomicons): This is a font with 8 symbols to talk about the "Pomodoro Technique"® (You can use these special symbols to change the configuration). You can use one of the [awesome-terminal-fonts](https://github.com/gabrielelana/awesome-terminal-fonts) that contains both powerline and pomicons symbols.

## Screenshot

![pomicons](/screenshot/screenshot.png)
