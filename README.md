
# love-qrcode

love-qrcode is a QR Code rendering library for [LÖVE](https://love2d.org/), utilizing [Luaqrcode](https://github.com/speedata/luaqrcode) under the hood. This library allows you to generate and render QR codes in your LÖVE projects.

## Features

- Generate QR codes from text
- Render QR codes on the screen
- Easy to integrate and use in LÖVE projects

## Installation

1. Clone the repository or download the zip file:
    ```sh
    git clone https://github.com/Nawias/love-qrcode.git
    ```
2. Place the `love-qrcode` folder in your LÖVE project directory.

## Usage
```lua
-- require the library in your `main.lua`:
local QRCode = require("love-qrcode")
-- Create a QR code instance:
local qr = QRCode("Hello, World!")
-- Draw the QR code in the `love.draw` callback:
function love.draw()
    qr:draw(100, 100)
end
```

## API

### QRCode Constructor

```lua
QRCode(text)
```
- `text` (string): The text to be encoded into the QR code.

### Methods

#### `QRCode:draw(...)`

Draws the QR code on the screen. The parameters passed are the standard `love.graphics.draw` parameters.

#### `QRCode:getText()`
Returns the current text value.

- Returns: (string) The text encoded in the QR code.

#### `QRCode:setText(text)`
Changes the text value and updates the QR code.

- `text` (string): The new text to be encoded.

#### `QRCode:getSize()`
Gets the size of the QR code in pixels.

- Returns: (number) The size of the QR code.

## Acknowledgements

This library is based on [Luaqrcode](https://github.com/speedata/luaqrcode). Many thanks to the original authors for their work.

## License

```text
love-qrcode - QR Code rendering library for LÖVE

Copyright 2024 Michał Wójcik

Permission is hereby granted, free of charge, to any person obtaining a
copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be included
in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENTs SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

