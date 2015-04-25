## My Code's a Little Rust-y

#### Dan Callahan &middot; dcallahan@mozilla.com · [@callahad](https://twitter.com/callahad)

<br>

[github.com/callahad/tccc18-rust](https://github.com/callahad/tccc18-rust)

---

## The Python/Ruby/Node.JS Lie

<br>

> "[Language] is fast enough, and <br>
> I can always write a C extension."

<br>

But it's not, and we never do.
<!-- .element: class="fragment" -->

---

## Why don't we write C?

### 1. Other people did it for us.

***

### Lines of C/C++ in Python Projects

|     Project     | # Lines |  %  |
| --------------- | -------:| ---:|
| CPython 3.5.0a2 | 399,387 | 43% |
| NumPy 1.9.2     | 166,034 | 62% |
| Pillow 2.7.0    |  22,669 | 52% |
| MarkupSafe 0.23 |     178 | 21% |

***

### We're standing on their shoulders

### And so are they.
<!-- .element: class="fragment" -->

![Pillow links to libjpeg](img/libjpeg.png)
<!-- .element: class="fragment" style="max-height: 65%; max-width: 65%;" -->

***

### 2. Writing C is **scary**.

***

### Memory management is **hard**.

<video data-autoplay class="stretch" src="img/ghostride.mp4"></video>

***

- Heartbleed
- Ghost <!-- .element: class="fragment" -->
- CVE-2015-0080 <!-- .element: class="fragment" -->

_I'm not smarter than the glibc or openssl devs._
<!-- .element: class="fragment" -->

---

## But what if you **need** to?

***

### The Dream

<br>

<span class="fragment">C's Performance</span><span class="fragment">, Portability</span><span class="fragment">, and Embeddability.</span>

<!-- .element: class="fragment" --> With *guaranteed* safety.

---

## Rust.

---

## Stack vs. Heap

***

|      Stack      |     Heap      |
| --------------- | ------------- |
| Fast but tiny   | Slow but huge |
| Function locals | Globals       |
| Managed by CPU  | Unmanaged     |

<br>

_Only small values of known, fixed size can go on the stack.
<br>
Growable things like vectors must go on the heap._

---

## Managed vs. Unmanaged

***

<!-- .slide: data-background-transition="none" data-background="img/ownership/01.jpg" -->

&nbsp;

***

## Managed vs. Unmanaged

_With Real Whiteboards!_

***

## Ownership

_With Real Whiteboards!_

***

<!-- .slide: data-background-transition="none" data-background="img/ownership/20.jpg" -->

&nbsp;

***

### Enforced Statically at Compile Time

<br>

- No dangling pointers
- No use after free vulnerabilities
- No pointer arithmetic
- No null pointer dereferencing

<br>

_This is a "Zero-Cost Abstraction."_

---

## Mutability Demos!

---

![](img/servo-github.png)
<!-- .element: style="margin-top: -5%;" -->

---

![](img/servo-reddit.png)
<!-- .element: style="margin-top: -5%;" -->

---

## Python FFI Demos!

---

## Learn More

_[rust-lang.org](https//rust-lang.org)_

___

[@callahad](https://twitter.com/callahad)

dcallahan@mozilla.com

___

[github.com/callahad/tccc18-rust](https://github.com/callahad/tccc18-rust)
