---
id: install
title: How to install js_of_ocaml
sidebar_label: How to install js_of_ocaml
---


##  Requirements

* dune
* Cmdliner, ppx_tools_versioned, ocaml-migrate-parsetree

See opam files at the root of the repository for version constraints.

Optional dependencies:
  * tyxml(see https://github.com/ocsigen/tyxml)
  * reactiveData(see https://github.com/ocsigen/reactiveData)
  * yojson(see https://github.com/mjambon/yojson)

## Install from opam

```
opam install js_of_ocaml js_of_ocaml-ppx js_of_ocaml-lwt
```

## Build and install from source

```
make
opam-installer js_of_ocaml-compiler
opam-installer js_of_ocaml
opam-installer js_of_ocaml-ppx
opam-installer js_of_ocaml-lwt
```