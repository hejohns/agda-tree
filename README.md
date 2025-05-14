# agda-tree

Converts `*.lagda.tree` to `*.tree`.

## Install

```sh
cargo install agda-tree
```

## Usage

Let's say you have a forest (evergreen notes system via [forester](https://www.jonmsterling.com/jms-005P.xml)), and the directory structure is

```
.
 |
 |-forest.toml      (config of forester)
 |-trees            (for forester)
 |-xxx
 | |-xxx.agda-lib
```

then you first run (with agda 2.8.0)

```sh
agda --html --html-highlight=code ex.lagda.tree
```

agda will produce a `html/ex.tree`, then do postprocessing

```sh
agda-tree build .
```

you will get

```
.
|-trees
| |- ex.tree
```

then you can view literate Agda in forster system.

## Example

![image](https://github.com/user-attachments/assets/ea6412f2-b53b-479a-9307-5934ac5804fd)
