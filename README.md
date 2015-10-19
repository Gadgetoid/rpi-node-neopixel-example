# rpi-node-neopixel-example

This is a code example written in Node.js for a blog post on  [blog.hypriot.com](http://blog.hypriot.com/post/drive-neopixels-in-docker/).

## Building the image

On your Raspberry Pi you can clone this example with

```bash
$ git clone https://github.com/hypriot/rpi-node-neopixel-example.git
$ cd rpi-node-neopixel-example
```

Then build the Docker image with

```bash
$ docker build -t node-neopixel .
```

## Running the example

Now run the NeoPixel example app on a Raspberry Pi B/B+ with this command

```bash
$ docker run --cap-add SYS_RAWIO --device /dev/mem -d node-neopixel
```

On the Raspberry Pi 2 you have to use this command

```bash
$ docker run --privileged -d node-neopixel
```

## Acknowlegements

Thanks to

* @usefulthink to create the Node.js module - https://github.com/raspberry-node/node-rpi-ws281x-native
* @richardghirst to port the WS281x library to Raspberry Pi 2 - https://github.com/richardghirst/rpi_ws281x

## License

The MIT License (MIT)

Copyright (c) 2015 Hypriot

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
