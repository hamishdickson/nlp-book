# 2.0 Haskell

This book will use Haskell for it's code examples.

## 2.1 What's a Haskell?

Haskell is a static, pure, lazy, functional language. Gee, that sounds an awful lot like buzzword lingo! That may well be, but these properties make Haskell a very effective language, and sometimes a bit odd. These properties are also opposite to most mainstream languages. For instance, Java is static, impure, eager and not functional, Ruby is dynamic, impure, eager, and only functional at times. While it is hard to give an accurate definition of every characteristic, we will try anyway.

Functional: Haskell puts an emphasis on functions and treats computation as the evaluation of functions. This in contrast to so-called imperative languages, that specify an order of instructions. As such, Haskell functions very often resemble mathematical functions closely. Being functional also has practical implications. For instance, iteration is accomplished by means of recursion, and functions are also values and can be passed to other functions.

Pure: Haskell is a pure language, in that functions do not have side-effects. This means that existing values cannot be changed, since changing data would be a side-effect of a function. It also guarantees that the evaluation of a function will always result in the same value given the same function arguments.

Lazy: As a lazy language, Haskell only evaluates expressions when needed. Say you just implemented a function that gives a list of all prime numbers. In a strict language, the function that makes the list will never terminate (since there are always more prime numbers). Haskell, on the contrary, will only evaluate this function when and as much as necessary. As long as you take a finite number of primes from the list, the program will happily terminate.

Static: Haskell programs are compiled before they can run. This means that the Haskell compiler will catch many errors for you at compile-time, rather than finding them when your program is used in production. Additionally, Haskell does type-inference. This means that the Haskell compiler can find out the types of values most of the times, and you do not need to type-annotate every value.

If you have prior programming experience in an imperative or eager language, Haskell can feel a bit odd in the beginning. Don't worry, you will feel warm and fuzzy eventually!

You may ask why we chose Haskell as the main programming language for this book, rather than a more mainstream language. During our own experiences developing natural language processing tools, we noticed that very many natural language processing tasks are relatively straightforward data transformations. Haskell is a language that is exceptionally good at data transformations. First of all, because it has higher order functions (functions that take functions as an argument) that traverse lists, sets, mappings, etc. Second, Haskell makes it easy to construct more complex transformations out of simple transformations.

Although this book does not provide a full introduction to the Haskell programming language, we try to cover Haskell concepts extensively when required. If you require more background on certain concepts, we recommend you to consult the free book <a href="http://learnyouahaskell.com/">Learn Haskell for Great Good!

## 2.1 Haskell isn't your typical language

If you've come from java, python or any other imperative language then you may have heard about some of Haskell's features.. or you may not have, so let's talk a bit about them.

*More detail here.*

## 2.2 Getting up and running

To work with this book, you need the Haskell Platform and a text editor. The Haskell Platform is available for Mac OS X, Windows, and Linux at: [http://hackage.haskell.org/platform/](http://hackage.haskell.org/platform/) Download the package for your platform, and install it.

If you do not use one of these platforms, not all is lost. First of all, you should download the GHC Haskell compiler. If you operating system provides a ports system or package manager, use it to locate and install a GHC package. If your operating system does not provide a port or package for GHC, you can still try to download a binary distribution from the GHC website. Once you have installed and set up GHC, install the packages of the Haskell Platform.

For the text editor, pick any editor you find comfortable, as long as it saves files as plain text. Programming Haskell becomes more comfortable if you have an editor with syntax highlighting and interpreter integration. Your authors prefer the Emacs editor with haskell-mode. haskell-mode provides good support for highlighting, and Haskell code formatting. Besides that, Emacs allows you to run the GHCi Haskell interpreter within the editor.

### 2.2.1 Editors

If you don't like emacs (weirdo) and have no idea what [https://en.wikipedia.org/wiki/Editor_war](the editor wars) are, then you probably want to use something like [https://atom.io/](atom) [http://www.sublimetext.com/](sublime text). Both are excellent.

## 2.3 Baby's first Haskell

You will probably want to get acquainted with the ghci Haskell interpreter. It allows you to try Haskell expressions and get immediate feedback.

On OS X or Linux systems, type `ghci -XNoMonomorphismRestriction` in a terminal to launch the interpreter. You will be greeted with a prompt that resembles the following:

            <script src="https://gist.github.com/hamishdickson/e357d715f911d6da3da6.js"></script>

On Windows, choose Start -> All Programs -> Haskell Platform -> WinGHCi. The first time, you should set the NoMonomorphismRestriction option that is required for some examples. Do this by going to the following item: File > Options > GHCi Startup. Then append -XNoMonomorphismRestriction in the field (make sure that there is a space before this addition). Click OK, and restart WinGHCi.
