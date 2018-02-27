# random_color
:gear: :art: Rust crate for generating random attractive colors. Checck it out on [crates.io](https://crates.io/crates/random_color).

Inspired by [RandomColor](https://github.com/davidmerfield/randomColor).

![crate badge](https://img.shields.io/crates/v/random_color.svg)
## Usage 

### Example

```rust
use random_color::{Color, Luminosity, RandomColor};

let color = RandomColor::new()
  .hue(Color::Blue) // Optional
  .luminosity(Luminosity::Light) // Optional
  .seed(42) // Optional
  .alpha(1.0) // Optional
  .to_hsl_string(); // 

// color => "hsl(179, 99%, 10%)"
```

### Possible hue values: 
  + `Color::Monochrome`
  + `Color::Red`
  + `Color::Orange`
  + `Color::Yellow`
  + `Color::Green`
  + `Color::Blue`
  + `Color::Purple`
  + `Color::Pink`

### Possible luminosity values: 
  + `Luminosity::Random`
  + `Luminosity::Bright`
  + `Luminosity::Light`
  + `Luminosity::Dark`

### Possible alpha values:
  + You can specify a value between 0 and 1 with `.alpha()`
  + You can specify a random value with `.random_alpha()`
  
### Avaible outputs:
```rust
  // As HSV Array
  let color = RandomColor::new().to_hsv_array(); // color => [179, 20, 100]

  // As RGB String
  let color = RandomColor::new().to_rgb_string(); // color => "rgb(204, 255, 254)"

  // As RGBA String
  let color = RandomColor::new().to_rgba_string(); // color => "rgba(204, 255, 254, 1)"

  // As RGB Array
  let color = RandomColor::new().to_rgb_array(); // color => [204, 255, 254]

  // As HSL String
  let color = RandomColor::new().to_hsl_string(); // color => "hsl(179, 99%, 10%)"

  // As HSLA String
  let color = RandomColor::new().to_hsla_string(); // color => "hsl(179, 99%, 10%, 1)"

  // As HSL Array
  let color = RandomColor::new().to_hsl_array(); // color => [179, 99, 10]
  
  // As Hex String
  let color = RandomColor::new().to_hex(); // color => "#b31464"
```
## Roadmap

+ Seed from string
+ Iteartor
+ Documentation

## License

The MIT License (MIT)

Copyright (c) 2017 <a href="http://lucasmarino.me">Lucas Maximiliano Marino</a>

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
