Cleaning data (part 2)
================

## Cleaning data (part 2)

Advanced cleaning with OpenRefine link for slides:
<http://bit.ly/bu-cleaning-data-p2>

## First steps:

Make sure you’ve downloaded and installed OpenRefine:
<http://openrefine.org/download.html>

1)  Go to the Downloads page
2)  Select the appropriate application for your computer

> See more information on downloading the OpenRefine software here:
> <https://github.com/OpenRefine/OpenRefine/wiki/Installation-Instructions>

## What we’ll cover

1.  First things first (software installation check)

2.  Web technologies and non-rectangular data types

3.  Wrectangling your data

4.  Make it reproducible

5.  Share your work\!

> *Many times, the data we encounter on the web (and other places) is in
> a format we can’t directly use, so we need to make some changes to the
> structure to make it more useful.* *The internet is full of all kinds
> of data types, and we want to be able to access, clean, format,
> restructure, visualize, and analyze all of it. OpenRefine is a tool
> that helps us take in a variety of data formats and clean it into
> something we can use.*

## Data file types

> *Today, we capture and store a massive amount of data electronically.
> But often, the format and structure for capturing and measuring data
> are not ideal for creating visualizations or performing analyses. This
> situation means we need to clean data (prepare them) for analysis.*

## What is/where are data?

Data are everywhere we look, and they’re being used to measure nearly
anything we can imagine

Numbers, text, pictures, audio, videos–there’s no limit to what we can
capture.

> *Data get collected from apps, devices, sensors, scanned documents,
> the internet, and relational databases. Storage like this usually
> results in a variety of file formats. Before a software algorithm can
> go looking for answers, the data must be cleaned up and converted into
> a unified form that the algorithm can understand.*

## But cleaning data isn’t sexy

<https://www.nytimes.com/2014/08/18/technology/for-big-data-scientists-hurdle-to-insights-is-janitor-work.html>

## Fundamentals – File Types and Structure

> *As we’ve noted, the information we find on the web (and other places)
> is in a format we can’t directly use. In the next few slides, we’re
> going to present what these formats are, why people use them, and how
> we can convert them into something we can analyze.*

## Data come in a variety of file formats

Someone sends you data in a downloadable file You log into an
interactive front-end and retrieve the data from a storage system (i.e.,
an MS SQL server database system) The data are available via a
continuous stream that’s capturing web traffic (i.e., social media) You
access the data through an Application Programming Interface (API)

> *Each of these methods might create a different file type, so it’s
> essential to know the strength and weaknesses of each. A single file
> that gets emailed to you is handy because you can always return to the
> original email to retrieve it. However, more extensive data sources
> require you to interact with them via a virtual machine or desktop
> (VMware or VirtualBox). Sometimes there is a constant stream of data
> coming in from users, like on a social media application or online
> business. Finally, sometimes, companies or organizations have a portal
> for accessing data called an Application Programming Interface (API).*

## Types of files: text files

Computer files generally belong to two broad groups, commonly called
text files and binary files: Files like web pages, computer source code,
and open-source programming languages are all text files These files can
be opened in a text editor (Notepad, Text Edit, etc.) or via the command
line Humans and computers can read these files

> *These files consist of only text characters (UTF-8 and UTF-16)*

> *Editing them can be difficult without an understanding of the
> particular format, language, or structure of the text itself.*

> *Text files are our friends for lots of reasons, but the most
> important being that they are more accessible to our collaborators
> (and future selves\!).*

## Types of files: binary files

Binary files require software to open them and are typically not
human-readable

Files like MS Word, Excel, and other proprietary software files

Executable files like application installation files (.dmgs or .exe)

Media files like .png, .jpg .mp4 or .mov files

Encryption or compression files (.zip or .rar)

Humans can’t read these files

> *These files need software to open and edit, and usually can’t be
> viewed via the command line. Most media files, database files,
> executables, and zipped files are binary files.*  
> *You can view plain text files, but you probably need to know the
> language if you’re going to edit or create these files.*

## Rectangular files (spreadsheets)

These are files stored in columns and rows (or variables and
observations)

Rectangular files usually require spreadsheet software (Excel or
OpenOffice) or relational database software.

> *Understanding how to access, manipulate, and extract the information
> in rectangular files (i.e., spreadsheets) is an essential part of data
> work because of how ubiquitous tabular data are. An absolute must-read
> for data in spreadsheets is [“Data Organization in
> Spreadsheets”](https://www.tandfonline.com/doi/full/10.1080/00031305.2017.1375989)
> by Karl Broman and Kara Woo.*

## Non-rectangular files (JSON & XML)

Non-rectangular data files (like JSON and XML) are commonly used on the
web for storing data.

JSON was (JavaScript Object Notation) created in 2002, and used for data
storage and transfer

XML (extensible markup language) is slightly older technology (created
in 1996), but still widely used for the same purpose

> *Internet technologies commonly use non-rectangular data files (like
> JSON and XML). [JSON](https://www.json.org/) (pronounced Jay-SON) is
> the JavaScript Object Notation format, and it looks a little like a
> list (if you’ve seen these before).
> [XML](https://en.wikipedia.org/wiki/XML) (or extensible markup
> language) is a data description language that’s useful for sharing
> information between different software systems.*

## JSON objects

JSON is an object notation language and stores data in objects and
arrays

Why would anyone store data this way? JSON can store data and the
attributes of the data within the same object.

> *[JSON](https://www.json.org/) data is a general-purpose, lightweight
> format, widely accessible, and relatively simple. You’ll find JSON
> used directly in JavaScript code for Web pages, and it’s the file
> format of choice for many APIs.*  
> *JSON Data Types: null, true, false, number, string*  
> *JSON Data Containers: square brackets \[ \], curly brackets { }*  
> *JSON objects (in contrast to rectangular database models) can store
> the set of attributes for an object within the object. JSON objects
> have a flexible representation because they don’t confine your data to
> columns and rows (now you can include text, images, etc.).*  
> *However, these objects typically need to be coerced into a
> rectangular object before analyzing.*

## XML objects

XML (eXtensible Markup Language) is a language used to encode web
documents and data structures. XML is also useful for transmitting
information between different software systems and through APIs.

[XML](https://en.wikipedia.org/wiki/XML) was designed to be
“self-descriptive” and carry data in a readable format (by humans and
machines)

> *the difference between XML and HTML is that XML is used to transport
> information, while HTML is used to display information.*
