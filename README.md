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
 | |- ex.lagda.tree
```

`cd xxx`, you first run agda (>= 2.8.0) with flags

```sh
agda --html --html-highlight=code ex.lagda.tree
```

agda will produce a `./html/ex.tree`, then do postprocessing

```sh
agda-tree build
```

you will get a directory `xxx/trees`, I will put this directory into configuration `forest.toml`, then you can view literate Agda in forster system.

![image](https://github.com/dannypsnl/agda-tree/blob/main/workflow.svg)

## Example

![image](https://github.com/user-attachments/assets/ea6412f2-b53b-479a-9307-5934ac5804fd)
