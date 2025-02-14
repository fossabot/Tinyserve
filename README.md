# Tinyserve

[![Build status](https://ci.appveyor.com/api/projects/status/dnv4xqnfx7v64re0?svg=true)](https://ci.appveyor.com/project/Babkock/tinyserve) [![dependency status](https://deps.rs/repo/github/Babkock/tinyserve/status.svg)](https://deps.rs/repo/github/Babkock/tinyserve) [![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FBabkock%2FTinyserve.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FBabkock%2FTinyserve?ref=badge_shield)
![](https://tokei.rs/b1/github/Babkock/tinyserve)

Tinyserve is a simple multi-threaded web server written in Rust. It serves the specified web root at the specified address.

```
USAGE:
    tinyserve [FLAGS] [OPTIONS]

FLAGS:
    -h, --help       Prints help information
    -v               Use -v for verbose output.
    -V, --version    Prints version information

OPTIONS:
    -a, --address <127.0.0.1>              Sets the IPv4 address to bind to. Default is 127.0.0.1 or localhost.
    -p, --port <8000>                      Sets the port on the specified address. Default is 8000.
    -r, --webroot <directory_with_html>    Sets the web root for the server. index.html is loaded from this directory.
                                           Default is ~/.config/tinyserve.
```

## How to use

Your web root directory must contain at the very least, a file called *404.html*. Tinyserve will crash if this file is not present. If there is no *index.html* to serve for a ```GET /``` request, Tinyserve will fall back to *404.html*.

There is an example HTML site included with this repo, copy it to your **```~/.config/tinyserve```**, the default web root, and give it a try. The default address is [localhost:8000](http://localhost:8000).

## License

This software is licensed under the terms of the [MIT License](https://github.com/Babkock/Tinyserve/blob/master/LICENSE.md). This software is distributed with absolutely no warranty.


[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FBabkock%2FTinyserve.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FBabkock%2FTinyserve?ref=badge_large)