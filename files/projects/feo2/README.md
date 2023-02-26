# FeO2 (alternatively: iron-oxide)
A statically typed interpreted programming language created entirely in Rust.

## Dependencies (as shown in `Cargo.toml`)
* `colored 2`
* `once_cell 1.17.1`

## File extensions
* `.feo2` - FeO2 source file
* `.iroxlib` - FeO2 libary source file
* `.iroxdf` - FeO2 data file (similar to `Cargo.toml` in Rust projects)

## Syntax example
FeO2 source file:
```js
using lib standard;
using lib string;

func loop(interations[int]) >[string] {
    for i[int] in range(1, interations) {
        print: to_str(1) + "\n"; // -> "1"
        println: 1; // -> "1"
        return 1;
    }
    return string.new("Success!");
}

func main() {
    println: loop(5);
}
```
FeO2 library source file:
```lua
OUT {
#func print,
#func println,
#number version = 001,
};
DEPEND {
#example="0.0.1",
};
INFO {
#version="0.0.1,
};
```
FeO2 data file:
```py
['throw_expections'] = true;
['information'] = [
    (name) = "example",
    (version) = "0.0.1",
    (ironox_version) = "0.0.1",
];
['dependencies'] = [
    ("example_external_repository") = "version",
];
```
