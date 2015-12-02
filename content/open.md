## Open Educational Resources

### Format

It is very hard work to generate good content.  In order to get the
most out of this work, it is necessary that the content that is
created be useable as widely as possible.  For example, universities
that use WebWork today have a large repository of homework problems
they can give their students.  But these problems are stored as Perl
programs using WebWork-specific libraries that cannot be easily
understood by any other system, so even if the source code of these
problems were published widely, they would only be easily usable at
schools using WebWork.

To this end, we must carefully consider the format in which we publish
any open resources, bearing in mind that different resources may
have different requiremenets regarding format.  

* Questions
* Static expository material
* Interactive expository material
* Open-source interactive widgets

We will discuss the nature of the problem and relevant considerations
for each of these in turn:

#### Questions

If we are to enable widespread sharing of questions among
institutions, then we have the following considerations:

* **The format must be convertible.** We do not propose to create the
  one great system for deploying and grading homework questions.
  Instead questions stored in the right format should be easily
  converted into the formats consumed by systems such as WebWork that
  are already deployed.  Because some systems are more capable than
  others, it is reasonable to expect that not all questions can be
  exported to all systems.

* **The format must be expressive.** Most basic kinds of logic that
  problem writers would wish to include in their problems should be
  supported out of the box.  For example, they may wish to provide
  specific responses to certain wrong answers.

* **The format must be extensible.** We do not expect to be able to
  enumerate the full list of features that all future problem writers
  will want.  There should be a way to add features that the format
  does not currently support (at the price of having to add
  conversions for the new features into the formats of whatever
  systems can support them).

* **The format must be perspicuous.** Many people will not write
  problems if the first step to doing so is "Learn Haskell".  It
  should at minimum be easy to find similar problems and copy them,
  changing the text and data as desired.  Ideally, it would not be
  difficult to read a short tutorial and be able to write most simple
  kinds of problems from scratch.

* **The format must be searchable.** The format should support tags to
  make it easy to mark and search out questions pertaining to "Law of
  Sines", for example.

Proposed formats:

* **LaTeX**: LaTeX is a well-understood format in the mathematical
    community.  It can be extended by adding new macros, and there is
    precedent in Ximera for converting LaTeX to a web-friendly format.
    The job of writing a convertor would be the work of re-creating or
    otherwise re-using the LaTeX parsing work that Ximera already
    does, and the job of writing an extension could be essentially
    that of adding a module to Ximera's LaTeX parsing code.  The main
    job in creating such a format would be in creating a modular
    system either like or out of Ximera and deciding on LaTeX macros
    for the main pieces of functionality that we would want to
    support.

* **Markdown**: Markdown is arguably the easiest format to learn.  It
    does not support mathematical expressions natively, nor tags,
    embedding of widgets, nor really any features beyond basic text
    formatting.  At a minimum, Markdown would have to be extended to
    support these.  This would create further difficuty in the work of
    creating export functionality.  The main work in creating a
    markdown-based format would be in agreeing upon a syntax for these
    extensions and creating an easy-to-use processor that supports
    them all.

* **XML**: There is a simple and widely-supported (every web browser
    can run it) declarative language called XSLT for converting XML
    into any other format you please.  The work of writing convertors
    from an XML format would be creating an XSLT document for each
    other format, and the work of extending the format would be adding
    a template for that extension to each XSLT convertor.  An XML
    format is relatively readable as plain text and can easily support
    metadata including tags.  XML is fundamentally a way of expressing
    data, so its ability to express logic would be limited.  The main
    wrk in specifying an XML format is in deciding on the document
    structure and tag definitions.  One proposal that does exactly
    this for a slightly different problem is Mathbok XML, so an option
    could be to extend that standard.

#### Static expository material

#### Interactive expository material

#### Open-source interactive widgets

### Repository

### Licensing