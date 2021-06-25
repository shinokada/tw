<p align="center">
<img width="400" src="https://raw.githubusercontent.com/shinokada/typelet/main/images/typewriter3.gif" />
</p>
<p align="center">
Photo by <a href="https://unsplash.com/@lucaonniboni?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Luca Onnibonil</a> on <a href="https://unsplash.com/">Unsplash</a>. GIF image by Author.
</p>
<h1  align="center">Typelet</h1>

## Overview

Create and add large words print it with a typewriter effect.

![image](https://raw.githubusercontent.com/shinokada/tw/main/images/400-tw.gif)

## Requirement

- [Figlet](http://www.figlet.org/)
- [GitHub CLI gh](https://github.com/cli/cli#installation)

## Usage

### Colors

When you print `-p`, use following number with the `--color` option.

| Number | Color           |
| ------ | --------------- |
| 0      | black           |
| 1      | red             |
| 2      | green (default) |
| 3      | yellow          |
| 4      | blue            |
| 5      | magenta         |
| 6      | cyan            |
| 7      | white           |

### Interval

When you print `-p`, interval determines the interval time. Use with `-i` or `--interval`.
Default: 2

| Number | time              | Speed                  |
| ------ | ----------------- | ---------------------- |
| 1      | 0.01-0.09 sec     | Slowest                |
| 2      | 0.001-0.009 sec   | Midium speed (Default) |
| 3      | 0.0001-0.0009 sec | Fastest                |

### Space

Use `-s`  to add spaces in front of all lines.
Default: 0

### Empty line

You can add a empty line using the `-e` option.

## Examples

### Create a new

Create a new Typelet file. The default font is standard.

```sh
typelet -c Typewriter
# or
typelet --create Typewriter
```

### Add a line

After creating a new Typelet file, you can add a new line using the `-a` option. Change a font using the `-f` option with a font name.

```sh
typelet -a Print -f banner
# or
typelet --add Print -f banner
```

### Add a empty line

```sh
typelet -e
```

### Spaces

Use the `-s` option to add spaces in front of all lines. The `-s` option takes a number.

```sh
typelet -s 30
```

This will add 30 spaces in front of all lines.

If you want to add spaces in front of a word/line, use quotes:

```sh
typelet -c "     Typelet" -f standard
```

<p align="center">
<img width="500" src="https://raw.githubusercontent.com/shinokada/typelet/main/images/space.png" /> 
</p>


### Read the Typelet file

The `-r` or `--read` option prints what's in the Typelet file.

```sh
typelet -r
# or
typelet --read
```

### Print

Print using the default settings.

```sh
typelet -p
```

Print it with the fastest mode 3 and red color.

```sh
typelet -p --color 1 -i 3
# or
typelet --print --color 1 -i 3
```

### Manually edit Typelet file

Sometimes you want to edit the Typelet file ma

Use `-o` or `--open` to open the Typelet file in a editor.

```sh
typelet -o
# or
typelet --open
```

This will open the terminal default editor. If it's not set, vim will open.

You can open it with VS Code using `-o v` or `--open v`.

```sh
typelet -o v
```

### Save it to Gist

You can save what you created to a Gist using `-g` or `--gist`.

```sh
typelet -g
# or
typelet --gist
```

### Save to the local from a Gist

You can save a Gist to your Typelet file using `-u` or `--url`.

```sh
typelet -u https://gist.github.com/shinokada/f7996e53914bc55854d2a800ec20ef82
# or
typelet -url https://gist.github.com/shinokada/f7996e53914bc55854d2a800ec20ef82
```

### Other functions

```sh
# print version
typelet -v

# print help
typelet -h
```

See [figlet](http://www.figlet.org/examples.html), for font examples.

### Save to Gist

```sh
typelet -g
# or
typelet --gist
```

### Save from Gist to local

```sh
typelet -u <gist-url>
# or
typelet --url <gist-url>
# then print it
typelet -p --color 1 -i 3
```

## Limitations

Ceratin Figlet fonts may create multiple lines for a word.

You can check it using `typelet read`.


## Reference

- [Figlet font examples](http://www.figlet.org/examples.html)


## Author

Shinichi Okada

## License

MIT License

Copyright (c) 2021 Shinichi Okada

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
