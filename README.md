# Awesome Lisp Languages with stars

A list of lisp-flavored programming languages implemented on top of existing programming languages.

### Why should I care as a lisp programmer?

If you already love s-expressions then lisp-flavored languages will make it nicer when you need to build on existing platforms. In case the target language does not support advanced features like macros and REPL-driven development, these can often be easily added by using the s-expressions layer.

The second point is about helping to spread lisp and its powerful ideas more. The example of Clojure and its relative popularity shows that being hosted on existing mainstream language and leveraging ecosystems of existing libraries is a key to broader adoption. It also lowers the barrier for people to try lisp and learn about the ideas behind it. Traditionally to learn lisp one needs to learn and get used to very unfamiliar syntax while at the same time being exposed to a completely new environment and ecosystem. Taking the environment out of the equation can make the experience of trying out lisp more approachable.

### Why should I care as a programmer in other language?

Learning about Lisp will make you a [better programmer](http://www.paulgraham.com/avg.html). You can pick any language below based on the language you are familiar with to get you started with the [lisp syntax](https://en.m.wikipedia.org/wiki/S-expression) more easily. It is also worth to read a post to get [intuition for lisp syntax](https://stopa.io/post/265).

In general when one learns any new programming language it opens new horizons and improves programming insight. Modern programming languages are converging and sometimes are being very similar to each other. The similarities can be missed because they are hidden behind a specific syntax.

If we translate the languages to a common syntax the similarities are more apparent and the different concepts stand out more. That way we can focus on the new innovative concepts and ideas to broaden our horizons.

## Classification

* **Type-A**: Simple syntax mapping\
  *These languages usually just provide s-expressions (parentheses) syntax and are translated to the target language without extra features/semantics. Also sometimes being called transpilers.*

* **Type-B**: Syntax and additional semantics\
  *In addition to translating the syntax some additional features/semantics that are not present in the target language are added. Usually if a language does not fit in other category, it can be considered being a Type-B.*

* **Type-C**: [Clojure](https://clojure.org/)-like\
  *Distinctive syntax that besides parentheses also uses brackets and curly braces. Distinctive features are persistent data structures, namespaces and vars, protocols.*

* **Type-L**: [Common Lisp](https://en.wikipedia.org/wiki/Common_Lisp)\
  *Implementing ANSI Common Lisp standard or being inspired by it.*

* **Type-S**: [Scheme](https://en.wikipedia.org/wiki/Scheme_%28programming_language%29)\
  *Implementing some of RxRS standards or being inspired by Scheme.*

## Languages

Listed primarily by the language which can be used for interoperability / [FFI](https://en.wikipedia.org/wiki/Foreign_function_interface).

*Language section does not necessarily mean the language of the implementation. For example `Ferret` compiles into `C++` but the compiler is written in `Clojure`. Or `Carp` interops with `C` but it is mostly written in `Haskell`. In case of `SBCL` it contains only small amounts of `C`, but it is implemented almost entirely in `Common Lisp`.*

<!-- TOC depthFrom:3 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

* [Multi Lang](#multi-lang)
* [Common Lisp](#common-lisp)
* [Scheme](#scheme)
* [C/C++](#cc)
* [C#](#c)
* [Dart](#dart)
* [Erlang](#erlang)
* [Fortran](#fortran)
* [Go](#go)
* [Java](#java)
* [JavaScript](#javascript)
* [Julia](#julia)
* [Lua](#lua)
* [Objective-C](#objective-c)
* [OCaml](#ocaml)
* [PHP](#php)
* [Python](#python)
* [R](#r)
* [Rust](#rust)
* [Shell](#shell)
* [VHDL](#vhdl)
* [WASM](#wasm)

<!-- /TOC -->

### Multi Lang

* [Mal](https://github.com/kanaka/mal) ⭐ 10,721 | 🐛 47 | 🌐 Assembly | 📅 2025-10-22 is an educational lisp with implementations in dozens of languages. It is a great resource for learning about lisp implementation.
* [Lux](https://github.com/LuxLang/lux) ⭐ 1,741 | 🐛 0 | 🌐 Emacs Lisp | 📅 2026-08-20 \[Type-B] functional, statically-typed Lisp that will run on several platforms
* [Wax](https://github.com/LingDong-/wax) ⭐ 855 | 🐛 15 | 🌐 C | 📅 2025-03-03 \[Type-A] tiny programming language, strongly statically typed, manual memory management, transpiles to C, C++, Java, TypeScript, Python, C#, Swift, Lua and WebAssembly
* [Ribbit](https://github.com/udem-dlteam/ribbit) ⭐ 562 | 🐛 20 | 🌐 Scheme | 📅 2026-08-16 \[Type-S] small and portable Scheme implementation (R4RS, 4 KB footprint), AOT and incremental compilers, targets C, JavaScript, Python and Scheme
* [Zick Standard Lisp](https://github.com/zick/ZickStandardLisp) ⭐ 56 | 🐛 2 | 🌐 Common Lisp | 📅 2021-03-14 minimal lisp with 42 implementations
* [Bigloo](https://www-sop.inria.fr/mimosa/fp/Bigloo/) \[Type-S] compiles into native binaries, interop with C, JVM, .NET
* [STELLA](https://www.isi.edu/isd/LOOM/Stella/index.html) - strongly typed, object-oriented, compiles down to Common Lisp, C++, or Java
* [Shen](https://shen-language.github.io/) \[Type-B] implementations in many programming languages, builtin pattern-matching and logic programming, optional static typing and lazy evaluation

### Common Lisp

* [Clasp](https://github.com/clasp-developers/clasp) ⭐ 2,782 | 🐛 175 | 🌐 Common Lisp | 📅 2026-08-24 \[Type-L] compiled using LLVM, seamless integration with existing libraries
* [Coalton](https://github.com/coalton-lang/coalton) ⭐ 1,751 | 🐛 194 | 🌐 Common Lisp | 📅 2026-08-15 \[Type-L] efficient, statically typed functional programming language that supercharges Common Lisp
* [SBCL](http://www.sbcl.org) \[Type-L] high performance native code compiler, native threading support, type inference engine
* [CLISP](https://clisp.sourceforge.io/) \[Type-L] uses bytecode compiler, easily portable
* [Clozure CL](https://ccl.clozure.com/) \[Type-L] fast compilation speed, native threads, precise generational compacting garbage collector, convenient foreign-function interface
* [ECL](https://common-lisp.net/project/ecl/) \[Type-L] embeddable and portable, can build standalone executables
* See list of [additional implementations](https://www.cliki.net/Common+Lisp+implementation).

### Scheme

* [Chez Scheme](https://www.scheme.com/) \[Type-S] compiles to native binaries, among the fastest available Scheme implementations, R6RS
* [Chicken Scheme](https://www.call-cc.org/) \[Type-S] produces portable and efficient C, supports R5RS and R7RS (work in progress)
* [Guile](https://www.gnu.org/software/guile/) \[Type-S] embedable, useful for extending programs with scripting
* [Racket](https://racket-lang.org/) \[Type-S] large standard library, powerful macro system, includes DrRacket IDE
* [Cyclone](https://justinethier.github.io/cyclone/) \[Type-S] Scheme-to-C compiler, R7RS, native threading support, generates fast native binaries
* [Microscheme](https://ryansuchocki.github.io/microscheme/) \[Type-S] Scheme subset for microcontrollers (like Arduino boards)
* [Loko Scheme](https://gitlab.com/weinholt/loko) \[Type-S] runs on bare hardware
* See list of [additional implementations](http://community.schemewiki.org/?scheme-faq-standards#implementations) and [benchmarks](https://ecraven.github.io/r7rs-benchmarks/).

### C/C++

* [Carp](https://github.com/carp-lang/Carp) ⭐ 6,014 | 🐛 138 | 🌐 Haskell | 📅 2026-08-24 \[Type-B] statically typed, no GC (Rust-like borrow checking)
* [FemtoLisp](https://github.com/JeffBezanson/femtolisp) ⭐ 1,720 | 🐛 21 | 🌐 Scheme | 📅 2020-02-26 \[Type-S] scheme-like lisp, powers the compiler of the Julia language
* [Extempore](https://github.com/digego/extempore) ⭐ 1,462 | 🐛 18 | 🌐 C | 📅 2026-07-22 \[Type-S] designed for live coding and music performances, temporal scheduling based on audio card sample rate
* [Dale](https://github.com/tomhrr/dale) ⭐ 1,045 | 🐛 28 | 🌐 C++ | 📅 2025-04-20 \[Type-B] Lisp-flavoured C with additional features, no GC, LLVM backend
* [C-Mera](https://github.com/kiselgra/c-mera) ⭐ 453 | 🐛 26 | 🌐 Common Lisp | 📅 2026-03-07 \[Type-A] also includes extensions to generate code to run on CUDA, GLSL
* [Liz](https://github.com/dundalek/liz) ⭐ 291 | 🐛 0 | 🌐 Clojure | 📅 2021-10-02 \[Type-A] written as EDN, compiles to Zig, customizable memory allocators, native binaries for many architectures
* [jo\_clojure](https://github.com/Zelex/jo_clojure) ⭐ 153 | 🐛 1 | 🌐 C++ | 📅 2025-04-26 \[Type-C] Fast Embeddable Clojure in C/C++, including persistent datastructures and STM
* [Lcc](https://github.com/saman-pasha/lcc) ⚠️ Archived \[Type-A] Lisp-like syntax for writing C
* [Toccata](https://github.com/Toccata-Lang/toccata) ⭐ 8 | 🐛 0 | 🌐 C | 📅 2026-08-25 \[Type-C] Clojure-inspired, gradually typed, no nil values, reference counting, compiles into native binaries
* [Cakelisp](https://github.com/makuto/cakelisp) \[Type-A] performance-oriented, good for game development, compiles down to C/C++, macros and compile-time code modification
* [Ferret](https://ferret-lang.org/) \[Type-C] aimed towards embedded systems
* [Janet](https://janet-lang.org/) \[Type-B] embedable, large standard library, GC
* [Jank](https://jank-lang.org/) \[Type-C] LLVM-hosted, Clojure-compatible, type-analysis, JIT
* [Maru](https://www.piumarta.com/software/maru/) \[Type-B] minimal self-hosting lisp, multimethods, user-defined types and structures, GC
* [PicoLisp](https://picolisp.com) \[Type-B] compiled to bytecode and interpreted, C and Java interop, built-in  database and GUI
* [Pre-Scheme](https://codeberg.org/prescheme/prescheme) \[Type-S] statically typed Scheme dialect, compiles to C, type inference, no GC, designed for systems programming
* [Owl Lisp](https://gitlab.com/owl-lisp/owl) \[Type-S] dialect of the Scheme, code can be interpreted or compiled into C files

### C\#

* [Clojure CLR](https://github.com/clojure/clojure-clr) ⭐ 1,653 | 🐛 0 | 🌐 C# | 📅 2026-07-20 \[Type-C] great for game development with arcadia and unity
* [RainLisp](https://github.com/chr1st0scli/RainLisp) ⭐ 44 | 🐛 1 | 🌐 C# | 📅 2026-08-01 \[Type-B] inspired by Scheme, interpreted, can be used as DSL integrating with .NET

### Dart

* [ClojureDart](https://github.com/Tensegritics/ClojureDart) ⭐ 1,635 | 🐛 123 | 🌐 Clojure | 📅 2026-08-24 \[Type-C] clojure dialect for Flutter and Dart

### Erlang

* [Clojerl](https://github.com/clojerl/clojerl) ⭐ 1,715 | 🐛 11 | 🌐 Erlang | 📅 2025-01-07 \[Type-C]
* [Lisp Flavored Erlang](http://lfe.io/) \[Type-A]

### Fortran

* [fscheme](https://genepi.qimr.edu.au/Staff/davidD/Scheme/SIOM.html) \[Type-S] small scheme interpreter written in Fortran 95
* [Schemetran](https://gitlab.com/codetk/schemetran) \[Type-A] Expressing Fortran computations in Scheme, compiles to readable Fortran code

### Go

* [Zygo](https://github.com/glycerine/zygomys) ⭐ 1,787 | 🐛 8 | 🌐 Go | 📅 2026-06-30 \[Type-B] embedable, call into native Go using reflection, optional infix syntax
* [let-go](https://github.com/nooga/let-go) ⭐ 553 | 🐛 150 | 🌐 Go | 📅 2026-08-24 \[Type-C] compiler, bytecode VM, Go interop, small footprint, fast booting
* [ZYLISP](https://github.com/zylisp/zylisp) ⚠️ Archived \[Type-A] simple Lisp that compiles to Go (source or bytecode)
* [Joker](https://joker-lang.org/) \[Type-C] interpreter, linter, great for scripting, Go interop is very limited
* [Slick](https://github.com/pcostanza/slick) \[Type-L]  Lisp/Scheme-style s-expression surface syntax for the Go programming language

### Java

* [Armed Bear Clojure](https://github.com/lsevero/abclj) ⭐ 94 | 🐛 4 | 🌐 Clojure | 📅 2021-04-27 \[Type-C+L] Common Lisp embedded in Clojure via ABCL
* [Venice](https://github.com/jlangch/venice) ⭐ 46 | 🐛 0 | 🌐 Java | 📅 2026-08-16 \[Type-C] Clojure-inspired, sandboxed, Java interop, 800+ builtin functions
* [ABCL](https://common-lisp.net/project/armedbear/) \[Type-L] CL interpreter and compiler, embedable using Java scripting API (JSR-223)
* [Clojure](https://clojure.org/) \[Type-C]
* [Kawa](https://www.gnu.org/software/kawa/) \[Type-S] scheme implementation (R7RS)
* [PicoLisp](https://picolisp.com) \[Type-B] compiled to bytecode and interpreted, C and Java interop, built-in  database and GUI

### JavaScript

* [Wisp](https://github.com/Gozala/wisp) ⭐ 986 | 🐛 59 | 🌐 wisp | 📅 2021-02-07 \[Type-C] Clojure-like, has protocols, no persistent data structures
* [Squint](https://github.com/squint-cljs/squint) ⭐ 898 | 🐛 22 | 🌐 Clojure | 📅 2026-08-12 \[Type-C] Squint is a light-weight dialect of ClojureScript with a compiler and standard library
* [RacketScript](https://github.com/racketscript/racketscript) ⭐ 736 | 🐛 81 | 🌐 Racket | 📅 2026-02-18 \[Type-S] Racket to JavaScript compiler, interop with both Racket and JS ecosystem
* [Lumen](https://github.com/sctb/lumen) ⭐ 570 | 🐛 31 | 🌐 JavaScript | 📅 2024-10-18 \[Type-A] self-hosted Lisp for Lua and JavaScript, uses arrays as first-class datastructures
* [eslisp](https://github.com/anko/eslisp) ⭐ 538 | 🐛 21 | 🌐 LiveScript | 📅 2026-05-28 \[Type-A] S-expression syntax for ECMAScript/JavaScript, Lisp-like macros
* [Valtan](https://github.com/cxxxr/valtan) ⭐ 271 | 🐛 4 | 🌐 Common Lisp | 📅 2025-12-19 \[Type-L] Common Lisp to JavaScript compiler
* [JSLisp](https://www.jslisp.org) ([source](https://github.com/6502/JSLisp) ⭐ 43 | 🐛 0 | 🌐 Common Lisp | 📅 2024-08-17) \[Type-L] Lisp-2, similar to Common Lisp, includes GUI library and IDE
* [BiwaScheme](https://www.biwascheme.org/) \[Type-S] compact Scheme written in JavaScript, integrates well with web browsers and Node
* [ClojureScript](https://clojurescript.org/) \[Type-C]
* [JACL](https://tailrecursion.com/JACL/) \[Type-L]  extended subset of Common Lisp, async reader and REPL development workflow
* [LIPS](https://lips.js.org) \[Type-S] similar to BiwaScheme, has better notation to call JS functions
* [Parenscript](https://common-lisp.net/project/parenscript/) \[Type-L] Common Lisp to JavaScript translator, native JS types, native calling convention
* [Whalesong](https://www.hashcollision.org/whalesong/) \[Type-S] Racket to JavaScript compiler

### Julia

* [LispSyntax.jl](https://github.com/swadey/LispSyntax.jl) ⭐ 236 | 🐛 8 | 🌐 Julia | 📅 2024-02-28 \[Type-A] Clojure-like lisp syntax to Julia translator with convenience macros, uses Julia's compiler and JIT

### Lua

* [Lumen](https://github.com/sctb/lumen) ⭐ 570 | 🐛 31 | 🌐 JavaScript | 📅 2024-10-18 \[Type-A] self-hosted Lisp for Lua and JavaScript, uses arrays as first-class datastructures
* [Fennel](https://fennel-lang.org/) \[Type-A] full Lua compatibility, embedable, compiled code with no runtime dependency
* [LCL](https://codeberg.org/gsou/LCL) \[Type-L] Lua Common Lisp is an implementation of Common Lisp targeting the Lua language
* [Urn](https://urn-lang.com/) \[?] focus on minimalism, should work with LuaJIT, influenced by Common Lisp and Clojure

### Objective-C

* [nu](https://github.com/programming-nu/nu) ⭐ 2,188 | 🐛 19 | 🌐 Objective-C | 📅 2023-07-11 \[?] interpreted
* [DreamLisp](https://github.com/jsloop42/dreamlisp) ⭐ 8 | 🐛 0 | 🌐 Objective-C | 📅 2026-08-24 \[Type-B] Clojure-inspired, originally based on MAL, added modules, lazy collections

### OCaml

* [Reason-Lisp](https://github.com/jaredly/myntax) ⭐ 52 | 🐛 2 | 🌐 OCaml | 📅 2019-01-26 \[Type-A] very incomplete

### PHP

* [Phel](https://phel-lang.org/) \[Type-C] Phel is a functional programming language that compiles to PHP.

### Python

* [Hy](https://github.com/hylang/hy) ⭐ 5,434 | 🐛 9 | 🌐 Python | 📅 2026-07-31 \[Type-A] compiles to Python AST, use Python ML libraries, runs on PyPy
* [Pixie](https://github.com/pixie-lang/pixie) ⭐ 2,358 | 🐛 55 | 🌐 Python | 📅 2020-10-28 \[Type-B] Clojure inspired, written in RPython, custom GC and JIT
* [Basilisp](https://github.com/basilisp-lang/basilisp) ⭐ 478 | 🐛 46 | 🌐 Python | 📅 2026-08-02 \[Type-C] Clojure-compatible, targeting Python3.6+
* [Hissp](https://github.com/gilch/hissp) ⭐ 450 | 🐛 30 | 🌐 Python | 📅 2026-08-06 \[Type-A] compiles to a functional subset of Python, macro metaprogramming with Python ecosystem

### R

* [llr](https://github.com/dirkschumacher/llr) ⭐ 205 | 🐛 17 | 🌐 R | 📅 2021-12-03 \[Type-C] Clojure inspired, in R compiles and interops with R

### Rust

* [Steel](https://github.com/mattwparas/steel) ⭐ 2,544 | 🐛 77 | 🌐 Rust | 📅 2026-08-25 \[Type-S] embedded scheme interpreter in Rust, inspired by Racket
* [Ketos](https://github.com/murarth/ketos) ⭐ 767 | 🐛 17 | 🌐 Rust | 📅 2021-05-18 \[Type-B] scripting and extension language for Rust programs, compiled to bytecode
* [Rustly](https://github.com/timothypratley/rustly) ⭐ 167 | 🐛 0 | 🌐 Clojure | 📅 2020-03-22 \[Type-C] transpiler, only small subset of Clojure supported
* [BLisp](https://ytakano.github.io/blisp/) \[Type-B] statically typed scripting language, type inference, algebraic data types, generics
* [GameLisp](https://gamelisp.rs) \[Type-B] scripting language for Rust game development, interpreted, pattern‑matching, coroutines, macros

### Shell

* [Gherkin](https://github.com/alandipert/gherkin) ⚠️ Archived \[Type-B] (dormant) implemented in Bash, shell interop
* [Fleck](https://github.com/chr15m/flk/) ⭐ 507 | 🐛 1 | 🌐 Shell | 📅 2021-12-18 \[Type-A] Clojure-like, based on [Mal](https://github.com/kanaka/mal/) ⭐ 10,721 | 🐛 47 | 🌐 Assembly | 📅 2025-10-22, packaged as single-file Bash script

### VHDL

* [Vhdl Lisp](https://github.com/domus123/vhdlisp) ⭐ 44 | 🐛 0 | 🌐 Common Lisp | 📅 2019-07-27 - alternative s-expression based notation to describe programmable integrated circuits (FPGAs)

### WASM

* [Liz](https://github.com/dundalek/liz) ⭐ 291 | 🐛 0 | 🌐 Clojure | 📅 2021-10-02 \[Type-A] general purpose programming language, supports WASM compilation target
* [Schism](https://github.com/schism-lang/schism) ⭐ 220 | 🐛 2 | 📅 2020-06-02 \[Type-S] self-hosting compiler from a subset of R6RS Scheme to WebAssembly
* [WebAssembly Scheme](https://github.com/PollRobots/scheme) ⭐ 182 | 🐛 109 | 🌐 WebAssembly | 📅 2023-05-02 \[Type-S] partial implementation of R7RS scheme, written using WebAssembly Text format
* [clj-wasm](https://github.com/roman01la/clj-wasm) ⭐ 160 | 🐛 0 | 🌐 Clojure | 📅 2019-11-24 \[Type-A] Clojure-flavored WASM's text format
* [Arboreta WASM](https://github.com/Arboreta/arboreta-wasm) ⭐ 60 | 🐛 1 | 🌐 Common Lisp | 📅 2016-12-14 \[?] Common Lisp tooling for WebAssembly
* [Hoot](https://gitlab.com/spritely/guile-hoot/) \[Type-S] ahead-of-time compiler for R7RS-small Scheme, aiming to support all of Guuile

## Misc

* A list of more [Clojure-like languages](https://github.com/chr15m/awesome-clojure-likes) ⭐ 266 | 🐛 2 | 🌐 Shell | 📅 2026-08-12.
* [Bel](http://paulgraham.com/bel.html) - self-hosted lisp dialect, see also markdown formatted [mirror](https://github.com/alephyud/bel) ⭐ 52 | 🐛 1 | 🌐 Common Lisp | 📅 2022-09-25
  * [Bel Clojure](https://github.com/stopachka/bel-clojure) ⭐ 48 | 🐛 1 | 🌐 Clojure | 📅 2022-09-04 - implementation in Clojure, includes continuations, Java numbers and strings, read [blog post](https://stopa.io/post/290)
  * [Language::Bel](https://github.com/masak/bel) ⭐ 27 | 🐛 80 | 🌐 Perl | 📅 2026-01-16 - implementation of Bel in Perl 5, includes extensive test suite
  * [Chime](https://github.com/jeremyschlatter/chime/) ⭐ 19 | 🐛 12 | 🌐 Haskell | 📅 2020-08-24 - implementation of Bel written in Haskell
  * [Babybel](https://github.com/cookrn/babybel) ⭐ 8 | 🐛 3 | 🌐 Common Lisp | 📅 2020-03-12 - Ruby implementation of Bel
  * [Bel-sml](https://github.com/niyarin/bel-sml) ⭐ 8 | 🐛 0 | 🌐 Standard ML | 📅 2021-09-11 - implementation written in Standard ML
* [CLJSL](https://github.com/IGJoshua/cljsl) ⭐ 24 | 🐛 0 | 🌐 Clojure | 📅 2022-05-08 - subset of Clojure compiled to GLSL for GPU programming
* See also list of languages  [implemented in Lisp](https://github.com/vindarel/list-of-languages-implemented-in-lisp) ⭐ 18 | 🐛 2 | 📅 2020-01-29.
* Lisps for Microcontrollers
  * [LispBM](https://github.com/svenssonjoel/lispBM) ⭐ 132 | 🐛 3 | 🌐 C | 📅 2026-08-23 (LBM) - concurrency and message passing influenced by Erlang, threads with mailbox, pattern-matching
  * [uLisp](http://www.ulisp.com/) - fits into 2 Kbytes of RAM, embedded syntax for assembly
* Additional "write C in Lisp" [projects](https://www.reddit.com/r/lisp/comments/e10spm/a_list_of_various_lispflavored_programming/f8n6qxa/) (most of them not ready for a prime time).
* [Build your own lisp](http://www.buildyourownlisp.com/) - a book describing building a Lisp dialect
* [Map of Common Lisp implementations](https://twitter.com/dk_jackdaniel/status/698157022483771392/photo/1)
* [Benchmarks of Scheme implementations](https://ecraven.github.io/r7rs-benchmarks/)

## Contribute

Anything incorrect? Is there an interested project that is missing? Open an issue or PR to request adding a project to the list.

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-25._
