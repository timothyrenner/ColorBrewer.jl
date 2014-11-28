# ColorBrewerJl

A small library for generating color brewer color palettes.
For more information on color brewer, see http://colorbrewer2.org/. 

## About

The color brewer palette collection was originally designed for maps, but is also useful for quickly generating nice colors for any kind of plot.

## Usage

The module contains one function, `palette`, which takes a scheme name and an integer for the number of colors in the palette.
It returns an array of `RGB` values, which are defined in the [Color.jl](https://github.com/JuliaLang/Color.jl) package.

The schemes are broken up into three categories based on the type of data you want to show: sequential, diverging, and qualitative.

All sequential color schemes can have between 3 and 9 colors (inclusive).
The available sequential color schemes are:

* Blues
* Oranges
* Greens
* Reds
* Purples
* Greys
* OrRd
* GnBu
* PuBu
* PuRd
* BuPu
* BuGn
* YlGn
* RdPu
* YlOrBr
* YlGnBu
* YlOrRd
* PuBuGn

All diverging color schemes can have between 3 and 11 colors (inclusive).
The available diverging color schemes are:

* Spectral
* RdYlGn
* RdBu
* PiYG
* PRGn
* RdYlBu
* BrBG
* RdGy 
* PuOr

The number of colors a qualitative color scheme can have depends on the scheme.
The available qualitative color schemes are:

* Set1
* Set2
* Set3
* Accent
* Dark2
* Paired
* Pastel1
* Pastel2

The `Paired` and `Set3` schemes can have between 3 and 12 colors (inclusive).
The `Pastel1` and `Set1` schemes can have between 3 and 9 colors (inclusive).
The `Set2`, `Accent`, `Dark2`, and `Pastel2` schemes can have between 3 and 8 colors (inclusive).

For example, to obtain a five color sequential green scheme, call

```julia
    greens = palette("Greens", 5);
```
Pretty simple stuff.

If the `palette` function is passed an invalid scheme or number of colors, it throws an `ArgumentError`.
