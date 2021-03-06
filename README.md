Dart: Up and Running
=============

This is the book "Dart: Up and Running" by Kathy Walrath and Seth Ladd.
More info: http://shop.oreilly.com/product/0636920025719.do

An HTML version of this book is online at
http://www.dartlang.org/docs/dart-up-and-running/.

The most up-to-date copy of the book is in an O'Reilly Subversion repo,
but we plan to keep this version (more or less) in sync with that.
If we change http://www.dartlang.org/docs/dart-up-and-running/,
then we also need to update the Subversion repo (and eventually this one).

The files in the Subversion repo have production changes that we should
apply to these ones. Ugh.

Project Structure
-----------------

**Makefile:**
	Use this to run doc-code-merge and to test the code.

**README.md:**
	This file.

**book.xml:**
	This is the entry point for the book, from an XML point of view.

**code/:**
	Code should be pulled out of the XML files and put here.

**figs/:**
	Figures and images.

**merged/:**
	doc-code-merge merges the documentation in xml/ and the code in code/
	to create this directory. It is autogenerated, so do not modify it!

**xml/:**
	The DocBook source for the book.


Using the Makefile
------------------

Install the Dart Editor (or Dart SDK).

Define DART_SDK, perhaps in your ~/.bashrc. Be sure to fill in the "..." with
the actual place you put it:

	export DART_SDK=.../dart-sdk
	export PATH=$PATH:$DART_SDK/bin

Checkout a copy of doc-code-merge:

	git clone git@github.com:dart-lang/doc-code-merge.git
	cd doc-code-merge
	pub install

Make sure you put that in your PATH as well, perhaps in your ~/.bashrc. Be
sure to fill in the "..." with the actual place you downloaded doc-code-merge:

	export PATH=$PATH:.../doc-code-merge

Install packages:

  cd .../doc-code-merge
  pub install

Now, just run make from your SVN directory:

	make

Watch the output carefully for errors. Unfortunately, there are cases where it
will print an error but not stop processing.
