# TCP SimpleText

This repository contains the **SimpleText** files for the texts in the
**All TCP (2015) Corpus** from the Visualizing English Print (VEP project).

**Quickstart:** Warning: this is a HUGE collection (61315 files, 8.1GB of text).

If you are a GIT user, you can clone this repository. If you don't know what
that means, use the "Download ZIP" option from the "Code" button above.
If you just want to download the files, press the "Code" button
(upper right above the README) and select "Download ZIP". This way you can get
the files without using GIT. Be patient - it is a HUGE download.


This collection (61315 documents, about 8.1GB) is a bit big for a GIT
repository. The total (including the GIT compressed stash) is around 11GB. 

In theory, this sized repository is allowed on GitHub. While it is unweildy  (and is beyond what GitHub recommends), it is below the absolute limits. The "git-sizer" tool only gives it a level of concern of "8 asterisks". However, it seems that there are some limits on any individual push (see below).

If you clone this repository you will have over 11GB on your disk (8.1 GB of text files, and 3+GB of GIT stuff). 

GitHub allows us to serve individual TXT files, as well as to provide a way to deliver the ZIP archive. It also provides version tracking so we can monitor updates. If you want a link to an individual file, you can use the Metadata Builder [link], or guess at the link yourself (for example, a link to `A11954.txt`, it would be [this](https://raw.githubusercontent.com/uwgraphics/VEP2_TCP_SimpleText/main/A1/A11954.txt)). 

GitHub is not a great way to distribute such a large collection. It is not efficient for working with such a large number of large files. However, it is stable and convenient. 

## What is this?

The [Visualizing English Print (VEP)](http://vep.cs.wisc.edu/) project was an effort
to scalable, digital scolarship of Early Modern texts possible. The project ran
from 2011-2016. The project is now over, but we are trying to make the things we
created available.

[Text Creation Partnership (TCP)](https://textcreationpartnership.org/) had made 
61315 documents in 2016 (when the VEP project ended). These are mainly EEBO files,
but also the Evans collection and a sampling of ECCO documents. 

Note: the 61315 were released in two phases, phase 1 and phase 2. This collection
includes both phases. But it only includes the documents transcribed
(or at least available to us) before the VEP project ended.

**This Repository** contains the *SimpleText* versions of the 61315 documents.
That is, if you copy this repository, you will have 61315 `.txt` files
(in VEP SimpleText format). If you want something other than the SimpleText files,
you will need to look elsewhere. The source '.xml' files are available directly
from the TCP. 

There is (or should be) a `.txt` file for each of the 61315 files. The files have names based on their TCP IDs. They are divided into subdirectories based on their names (so the file `A11954.txt` is in the `A1` directory). This division was done by other collections. It does not lead to a good distribution (A few directories have vast majority of the content).

**SimpleText** is a simplified file format that was developed by the VEP project
in order to make certain kinds of analysis convenient. It is derived from the original
XML files available from the TCP. It purposefully throws away information
in the source files to make it convenient and consistent to perform analysis on the words.
Metadata is stored separately. It seeks to make consistent and transparent access to the
information in the TCP files. If there are errors, they are reproduced.
If we introduce errors, we do it consistently.

Briefly, SimpleText files are ASCII files (a limited character set) that include the
transcribed "words" without any metadata. Some limited standardization has been done to
improve consistency LINK.
But the format and its process were designed for simplicity, convenience, and traceability.
It was intended to help enable consistent, corpus scale inquiries (which necessarily means
computation analysis).
If you are looking for a format that is better for humans to read, or has extensive
metadata, or correctly captures letter forms and diacritical marks, look elsewhere.

These documents are **not split**, and they correspond 1-to-1 with TCP documents,
which should correspond 1-to-1 with physical documents that were transcribed.
So, for example, `A11954.txt` is Shakespeare's "First Folio" - all the plays in
one big file, since it was transcribed as one document.  

This **version** of the files was dated September 14, 2016. That is, we believe that
these files were processed (converted by a team member from the TCP XML sources on hand)
on (or before) that date. We are not actually sure which "version" of the TCP XML files were
used.

Internally, we called this collection `TCP_CharClean_ExtractedStandardizedDivided`
which basically describes the steps (pipeline) used to turn the TCP XML files
into SimpleText. We now just call it "SimpleText". We also use a simpler 
file naming convention: the file names are just "{TCP_ID}.txt".

We did not release these files in 2016 because there was an embargo on
public release of the Phase 2 EEBO documents. Now that that embargo is
over, we can release the whole thing. 

## What else can I get?

Again, this repository has only the SimpleText versions of the TCP2015 Corpus.

If you want the **metadata** ours is available using the [Metadata Builder](https://uwgraphics.github.io/MetadataBuilder/).

If you want an individual file, it can be inconvenient to use GitHub to get it.
You can get links to the individual files using the [Metadata Builder](https://uwgraphics.github.io/MetadataBuilder/).

If you want more extensive information about each TCP document, you may want to consult
the [EarlyPrint](https://earlyprint.org/) project. They have a very complete archive
of extensively annotated texts. Early Print has a very contrasting set of goals 
from SimpleText.

Similarly, if you want human readable versions of the texts, or "corrected"
versions of the texts, you probably want to look elsewhere. Again, [EarlyPrint](https://earlyprint.org/) may be a better resource.

If you want SimpleText (or MetaData) for the Drama documents in the corpus,
split by play (e.g., the first folio is many separate files),
you can look at the [Early Modern Drama Corpus](https://github.com/uwgraphics/EMDrama).

If you want the source XML files, you can get those from other sources, including the
TCP. If you want to see the page images, you will need to go elsewhere.
The [Metadata Builder](https://uwgraphics.github.io/MetadataBuilder/) can create links to the official ProQuest EEBO page images.

## What if I have Questions?

Unfortunately, the VEP project is over.
However, the PIs still care about it so you can write to us.
Email is best.

Note: if you find an "error", remember that our goal is to be consistent
and transparent. If there is an error in the original transcription, we
intentionally reproduce it. If we introduce an error in extracting and
converting the transcriptions, we do so consistently.

If you want a "corrected" set of texts, look to the
[EarlyPrint](https://earlyprint.org/) project.

This repository was posted in August of 2021, by Michael Gleicher.

## Some GIT Details

In order to get this to GitHub, which seems to limit the sizes of pushes, each individual subdirectory had its own initial commit.

To comply with git naming conventions, we renamed the default branch to `main` after the first commit.
