
### Navigation

        <li class="right" style="margin-right: 10px">
          [index](https://pythonhosted.org/an_example_pypi_project/genindex.html)</li>
        <li class="right">
          [modules](https://pythonhosted.org/an_example_pypi_project/modindex.html) |</li>
        <li class="right">
          [next](https://pythonhosted.org/an_example_pypi_project/setuptools.html) |</li>
        <li class="right">
          [previous](https://pythonhosted.org/an_example_pypi_project/setuptools.html) |</li>
        - [an_example_pypi_project v0.0.5 documentation](https://pythonhosted.org/an_example_pypi_project/index.html) ╗ 
      
# Documenting Your Project Using Sphinx[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#documenting-your-project-using-sphinx)

This covers just a few of the many many commands available via sphinx.  For
more, visit [http://sphinx.pocoo.org/](http://sphinx.pocoo.org/).

Also, another great site with just an overview of more common commands is
[http://docs.geoserver.org/trunk/en/docguide/sphinx.html](http://docs.geoserver.org/trunk/en/docguide/sphinx.html).

## Installing Sphinx[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#installing-sphinx)

Try:

## Sphinx QuickStart[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#sphinx-quickstart)

To get started, <tt class="docutils literal">cd</tt> into the documentation directory and type:

Here is a list of the default used in this project:

<th class="head">Prompt</th><th class="head">Choice</th>
|------
|&gt; Root path for the documentation [.]:|&lt;ENTER&gt;
|&gt; Separate source and build directories (y/N) [n]:|y
|&gt; Name prefix for templates and static dir [_]:|&lt;ENTER&gt;
|&gt; Project name:|an_example_pypi_project
|&gt; Author name(s):|Andrew Carter
|&gt; Project version:|0.0.1
|&gt; Project release [0.0.1]:|&lt;ENTER&gt;
|&gt; Source file suffix [.rst]:|&lt;ENTER&gt;
|&gt; Name of your master document (without suffix) [index]:|&lt;ENTER&gt;
|&gt; autodoc: automatically insert docstrings from modules (y/N) [n]:|y
|&gt; doctest: automatically test code snippets in doctest blocks (y/N) [n]:|n
|&gt; intersphinx: link between Sphinx documentation of different projects (y/N) [n]:|y
|&gt; todo: write ôtodoö entries that can be shown or hidden on build (y/N) [n]:|n
|&gt; coverage: checks for documentation coverage (y/N) [n]:|n
|&gt; pngmath: include math, rendered as PNG images (y/N) [n]:|n
|&gt; jsmath: include math, rendered in the browser by JSMath (y/N) [n]:|n
|&gt; ifconfig: conditional inclusion of content based on config values (y/N) [n]:|y
|&gt; Create Makefile? (Y/n) [y]:|n
|&gt; Create Windows command file? (Y/n) [y]:|n

Then you should get:

## <tt class="docutils literal">conf.py</tt>[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#conf-py)

In your <tt class="docutils literal">doc/source</tt> directory is now a python file called <tt class="docutils literal">conf.py</tt>.

This is the file that controls the basics of how sphinx runs when you run a
build.  Here you can do this like:

> 
<ul class="simple">
<li>Change the version/release number by setting the <tt class="docutils literal">version</tt> and <tt class="docutils literal">release</tt>
variables.</li>
- Set the project name and author name.
- Setup a project logo.
<li>Set the default style to <tt class="docutils literal">sphinx</tt> or <tt class="docutils literal">default</tt>.  Default is what
the standard python docs use.</li>
</ul>


and much much more.  Browsing through this file will give you an understanding
of the basics.

## reStructured Text (reST) Resources[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#restructured-text-rest-resources)

Sphinx is built of reStructured text and, when using sphinx most of what you
type is reStructured text.  Some great resources are below (and most examples
are ripped out of these pages):

- [http://docutils.sourceforge.net/rst.html](http://docutils.sourceforge.net/rst.html)
- [http://docutils.sourceforge.net/docs/user/rst/quickref.html](http://docutils.sourceforge.net/docs/user/rst/quickref.html)
- [http://docutils.sourceforge.net/docs/user/rst/cheatsheet.txt](http://docutils.sourceforge.net/docs/user/rst/cheatsheet.txt)

## Bold/Italics[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#bold-italics)

Bold and italics are done like this:

which render like **bold** and **italics**.

## Lists[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#lists)

You can do:

which render as:

- A thing.
- Another thing.

or

1. Item 1.
1. Item 2.
1. Item 3.

or

- Some.
- Thing.
- Different.

## Headers[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#headers)

ItÆs up to you to pick a convention for headers and just stick with it û
Sphinx will pick up on your convention:

You can do whatever header stragetgy you want, but I think a good one is:

So:

Is rendered like this:

### A Subpoint[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#a-subpoint)

This is my idea.

#### A subsubpoint[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#a-subsubpoint)

This is a smaller idea.

## Tables[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#tables)

Basic tables are done like this:

Which render like this:

COMPLEX TABLE:

<th class="head">Header 1</th><th class="head">Header 2</th><th class="head">Header 3</th>
|------
|body row 1|column 2|column 3
|body row 2<td colspan="2">Cells may span columns.</td>
|body row 3<td rowspan="2">Cells mayspan rows.</td><td rowspan="2">- Cells- contain- blocks.</td>
|body row 4

SIMPLE TABLE:

<th class="head" colspan="2">Inputs</th><th class="head">Output</th>
<th class="head">A</th><th class="head">B</th><th class="head">A or B</th>
|------
|False|False|False
|True|False|True
|False|True|True
|True|True|True

## Links[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#links)

Urls are automatically linked, like [http://packages.python.org/an_example_pypi_project/](http://packages.python.org/an_example_pypi_project/)

For other links, you basically use the <tt class="docutils literal">_</tt> operator.

To add a text with a hyperlink, I like using this format:

which renders as [Docs for this project](http://packages.python.org/an_example_pypi_project/).

To create an anchor link that jumps to another section in the
same .rst file, use this syntax:

Which renders like this: [Table of Contents](https://pythonhosted.org/an_example_pypi_project/sphinx.html#table-of-contents)

## Images[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#images)

Images syntax is like this:

Which renders like this:

Proof that getting rich is mostly luck.

You can also add an anchor point for an image like this:

Which renders like this:

Proof that getting rich is mostly luck.

Now you can reference this anchor like this:

which renders like this:

This picture [is_sweaty](https://pythonhosted.org/an_example_pypi_project/sphinx.html#is-sweaty).

## Documents[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#documents)

To download documents you use the syntax:

which renders like **An Example Pypi Project**.

## Substitutions[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#substitutions)

Substitutions syntax is

Or if you want to do a literal text replacement use:

Which renders like this:

The <img alt="biohazard" src="./exemple_files/biohazard.png"> symbol must be used on containers used to dispose of medical waste.

I really like [<tt class="xref docutils literal">doctest</tt>](http://docs.python.org/library/doctest.html#module-doctest).

Note

Substitutions are really useful, especially when put into a <tt class="docutils literal">global.rst</tt>
and included at the top of every file.  See [Includes](https://pythonhosted.org/an_example_pypi_project/sphinx.html#includes) below for more.

## Includes[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#includes)

The syntax:

Will æinlineÆ the given file.  A common convention I use is create a global
.rst file called <tt class="docutils literal">global.rst</tt> and include that at the top of every page.
Very useful for links to common images or common files links, etc.

## Table of Contents[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#table-of-contents)

Using the syntax:

renders like this:

<li class="toctree-l1">[Getting Started With <tt class="docutils literal">setuptools</tt> and <tt class="docutils literal">setup.py</tt>](https://pythonhosted.org/an_example_pypi_project/setuptools.html)<ul>
- [Installing setuptools and easy install](https://pythonhosted.org/an_example_pypi_project/setuptools.html#installing-setuptools-and-easy-install)
- [Setting up <tt class="docutils literal">setup.py</tt>](https://pythonhosted.org/an_example_pypi_project/setuptools.html#setting-up-setup-py)
- [Using <tt class="docutils literal">setup.py</tt>](https://pythonhosted.org/an_example_pypi_project/setuptools.html#using-setup-py)
- [Intermezzo: .pypirc file and gpg](https://pythonhosted.org/an_example_pypi_project/setuptools.html#intermezzo-pypirc-file-and-gpg)
- [Registering Your Project](https://pythonhosted.org/an_example_pypi_project/setuptools.html#registering-your-project)
- [Uploading Your Project](https://pythonhosted.org/an_example_pypi_project/setuptools.html#uploading-your-project)
- [Putting It All Together With The Full Windows Script](https://pythonhosted.org/an_example_pypi_project/setuptools.html#putting-it-all-together-with-the-full-windows-script)

where <tt class="docutils literal">setuptools</tt>, <tt class="docutils literal">sphinx</tt>, etc. correspond to <tt class="docutils literal">setuptools.rst</tt> and
<tt class="docutils literal">sphinx.rst</tt> files in the local path.

## Paragraph Markup[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#paragraph-markup)

To bring attention to a section of text, use paragraphs level markups.

Important constructs include:

The way you would use this is as follows:

Which would render like this:

This is a statement.

Warning

Never, ever, use this code!


New in version 0.0.1.

Now it is okay to use this code.

For full Sphinx docs on paragraph markup, check out
[http://sphinx.pocoo.org/markup/para.html](http://sphinx.pocoo.org/markup/para.html).

## Code[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#code)

Python code in sphinx is easy.  Because we turned <tt class="xref docutils literal">pygments</tt> on, all we
need to do is use the <tt class="docutils literal">::</tt> operator at the end of a line.  So:

Renders like this:

Here is something I want to talk about:

Also you can use the <tt class="docutils literal">::</tt> operator to basically render any text exactly using
fixed width fonts and by passing the restructured text engine.
This is useful for ascii art:

Also, you can add ôinlineö code by using the fixed-font operator.

By using two <tt class="docutils literal">``</tt> marks like this:

you get:

This is inline <tt class="docutils literal">if __name__ == '__main__':</tt>

## Python Cross Referencing Syntax[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#python-cross-referencing-syntax)

Sphinx makes it easy to quickly link to other code definitions that
**are in the python path** or can be found by <tt class="xref docutils literal">intersphinx</tt>.

The major ones I use all the time are:

- <tt class="docutils literal">:mod:</tt>
- <tt class="docutils literal">:func:</tt>
- <tt class="docutils literal">:class:</tt>

Which is used like this:

which renders like this:

I really like the [<tt class="xref docutils literal">threading</tt>](http://docs.python.org/library/threading.html#module-threading) module which has the
[<tt class="xref docutils literal">threading.Thread</tt>](http://docs.python.org/library/threading.html#threading.Thread) class.

Here is a link [<tt class="xref docutils literal">time.time()</tt>](http://docs.python.org/library/time.html#time.time).

For more, visit [http://sphinx.pocoo.org/markup/inline.html](http://sphinx.pocoo.org/markup/inline.html).

## æAutoÆ Directives[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#auto-directives)

From the sphinx docs directly:

<tt class="xref docutils literal">sphinx.ext.autodoc</tt> û Include documentation from docstrings

This extension can import the modules you are documenting, and pull in
documentation from docstrings in a semi-automatic way.

Note

For Sphinx (actually, the Python interpreter that executes Sphinx) to find
your module, it must be importable.  That means that the module or the
package must be in one of the directories on [<tt class="xref docutils literal">sys.path</tt>](http://docs.python.org/library/sys.html#sys.path) û adapt your
[<tt class="xref docutils literal">sys.path</tt>](http://docs.python.org/library/sys.html#sys.path) in the configuration file accordingly.

For this to work, the docstrings must of course be written in correct
reStructuredText.  You can then use all of the usual Sphinx markup in the
docstrings, and it will end up correctly in the documentation.  Together with
hand-written documentation, this technique eases the pain of having to maintain
two locations for documentation, while at the same time avoiding
auto-generated-looking pure API documentation.

For more on autodoc see [http://sphinx.pocoo.org/ext/autodoc.html](http://sphinx.pocoo.org/ext/autodoc.html).

The main autodoc features I use are:

- <tt class="docutils literal">.. automodule:: &lt;module_name&gt;</tt>
- <tt class="docutils literal">.. autoclass:: &lt;class_name&gt;</tt> and
- <tt class="docutils literal">.. autofunction:: &lt;function_name&gt;</tt>

The key to using these features is the <tt class="docutils literal">:members:</tt> attribute.  If:

- You donÆt include it at all, only the docstring for the object is brought in:
<li>You just use <tt class="docutils literal">:members:</tt> with no arguments, then all public functions,
classes, and methods are brought it that have docstring.</li>
<li>If you explictly list the members like <tt class="docutils literal">:members: fn0, class0, _fn1</tt>
those explict members are brought.</li>

WeÆll examine these points in the full example [Full Code Example](https://pythonhosted.org/an_example_pypi_project/sphinx.html#full-code-example).

## Function Definitions[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#function-definitions)

Function doc strings deserve a mention.  The sphinx syntax (taken from
[http://sphinx.pocoo.org/markup/desc.html](http://sphinx.pocoo.org/markup/desc.html)) looks like this:

which renders like this:

Format the exception with a traceback.

- **etype** û exception type
- **value** û exception value
- **tb** û traceback object
- **limit** (integer or None) û maximum number of stack frames to show

list of strings

However, this can be a bit hard to read in the docstring itself (one line of
thinking is that the sphinx markup shouldnÆt kill the docstring that a user
might read through the <tt class="docutils literal">__doc__</tt> attribute).  In fact the
google style guide [http://google-styleguide.googlecode.com/svn/trunk/pyguide.html](http://google-styleguide.googlecode.com/svn/trunk/pyguide.html)
says doc string should look like this:

which I think is a lot cleaner when you just look at the docstring.  It wonÆt
have the pretty sphinx formatting however.  WeÆll see another example in
[Full Code Example](https://pythonhosted.org/an_example_pypi_project/sphinx.html#full-code-example) below.

## Full Code Example[Â](https://pythonhosted.org/an_example_pypi_project/sphinx.html#full-code-example)

The [<tt class="xref docutils literal">an_example_pypi_project</tt>](https://pythonhosted.org/an_example_pypi_project/pkgcode.html#module-an_example_pypi_project) contains

- An <tt class="docutils literal">__init__</tt> file for the module.
<li><tt class="docutils literal">useful_1.py</tt> and <tt class="docutils literal">useful_2.py</tt>.  These files are IDENTICAL so IÆll only
reprint one here.</li>
<li>The <tt class="docutils literal">code.rst</tt> file which pulls it all together. This file lives in the doc
directory.</li>

Note

The idea behind the <tt class="docutils literal">auto</tt> directives is to keep as much documentation in
the code docstrings as possible.  However, Sphinx still aims to give you
control not found when using real auto tools like doxygen or epydoc.

Therefore, that is why you need the small stub file <tt class="docutils literal">code.rst</tt> to bascially
act as a director for pulling the docstrings from the code.

Contents of <tt class="docutils literal">an_example_pypi_project.__init__</tt>:

Contents of <tt class="docutils literal">an_example_pypi_project.useful_1</tt>:

And finally, contents of <tt class="docutils literal">code.rst</tt> which pulls it all together:

When youÆre done, you get [**Documentation for the Code**](https://pythonhosted.org/an_example_pypi_project/pkgcode.html).

### [Table Of Contents](https://pythonhosted.org/an_example_pypi_project/index.html)

<li>[Documenting Your Project Using Sphinx](https://pythonhosted.org/an_example_pypi_project/sphinx.html)<ul>
- [Installing Sphinx](https://pythonhosted.org/an_example_pypi_project/sphinx.html#installing-sphinx)
- [Sphinx QuickStart](https://pythonhosted.org/an_example_pypi_project/sphinx.html#sphinx-quickstart)
- [<tt class="docutils literal">conf.py</tt>](https://pythonhosted.org/an_example_pypi_project/sphinx.html#conf-py)
- [reStructured Text (reST) Resources](https://pythonhosted.org/an_example_pypi_project/sphinx.html#restructured-text-rest-resources)
- [Bold/Italics](https://pythonhosted.org/an_example_pypi_project/sphinx.html#bold-italics)
- [Lists](https://pythonhosted.org/an_example_pypi_project/sphinx.html#lists)
<li>[Headers](https://pythonhosted.org/an_example_pypi_project/sphinx.html#headers)<ul>
<li>[A Subpoint](https://pythonhosted.org/an_example_pypi_project/sphinx.html#a-subpoint)<ul>
- [A subsubpoint](https://pythonhosted.org/an_example_pypi_project/sphinx.html#a-subsubpoint)


#### Previous topic

[Getting Started With <tt class="docutils literal docutils literal docutils literal docutils literal docutils literal">setuptools</tt> and <tt class="docutils literal docutils literal docutils literal docutils literal docutils literal">setup.py</tt>](https://pythonhosted.org/an_example_pypi_project/setuptools.html)

#### Next topic

[Getting Started With <tt class="docutils literal docutils literal docutils literal docutils literal">setuptools</tt> and <tt class="docutils literal docutils literal docutils literal docutils literal">setup.py</tt>](https://pythonhosted.org/an_example_pypi_project/setuptools.html)

### This Page

              - [Show Source](https://pythonhosted.org/an_example_pypi_project/_sources/sphinx.txt)
            
### Quick search


              Enter search terms or a module, class or function name.
              

### Navigation

        <li class="right" style="margin-right: 10px">
          [index](https://pythonhosted.org/an_example_pypi_project/genindex.html)</li>
        <li class="right">
          [modules](https://pythonhosted.org/an_example_pypi_project/modindex.html) |</li>
        <li class="right">
          [next](https://pythonhosted.org/an_example_pypi_project/setuptools.html) |</li>
        <li class="right">
          [previous](https://pythonhosted.org/an_example_pypi_project/setuptools.html) |</li>
        - [an_example_pypi_project v0.0.5 documentation](https://pythonhosted.org/an_example_pypi_project/index.html) ╗ 
      
