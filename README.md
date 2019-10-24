Cleaning data (part 2)
=====================

*Advanced cleaning with OpenRefine*

link for slides: http://bit.ly/bu-cleaning-data-p2 

Be sure to check out these installation instructions before starting this workshop.  

***

## First steps:

Make sure you've downloaded and installed OpenRefine:

http://openrefine.org/download.html

1) Go to the Downloads page

2) Select the appropriate application for your computer
See more information on downloading the OpenRefine software here: https://github.com/OpenRefine/OpenRefine/wiki/Installation-Instructions 

***

## What we'll cover

- First things first (software installation check)  
- Web technologies and non-rectangular data types  
- Wrectangling your data  
- Make it reproducible    
- Share your work!  

The Internet is full of all kinds of data types, and we want to be able to access, clean, format, restructure, visualize, and analyze all of it. OpenRefine is a tool that helps us take in a variety of data formats and clean it into something we can use.

![](figs/01-openrefine.png)


***

## Data file types

Today we capture and store a massive amount of data electronically. But often times, the format and structure for capturing and measuring data are not ideal for creating visualizations or performing analyses. This means cleaning...

## What is/where are data?

Data are everywhere we look, and they're being used to measure nearly anything we can imagine

Numbers, text, pictures, audio, videos--there's no limit to what we can capture 

Data get collected from apps, devices, sensors, scanned documents, the Internet and relational databases. This usually results in a variety of file formats, and before a software algorithm can go looking for answers, the data must be cleaned up and converted into a unified form that the algorithm can understand.

***

## But cleaning isn't sexy...

https://www.nytimes.com/2014/08/18/technology/for-big-data-scientists-hurdle-to-insights-is-janitor-work.html

***

## Fundamentals – Formats, Types, and Encodings

Many times the data we encounter on the web (and other places) is in a format we can't directly use, so we need to make some changes to the structure in order to make it more useful.

***

## Data come from a variety of sources:

1. Someone send you data in a downloadable file

2. You log into an interactive front-end and retrieve the data from a storage system (i.e. a SQL database system with a query interface)

3. The data are available vis a continuous stream that's capturing web traffic (i.e. social media)

4. The data are accessible through an Application Programming Interface (API)

Each of these methods might create a different file type, so its important to know the strength and weaknesses of each. 

***

## Text and binary files

Computer files generally belong to two broad groups, commonly called **text files** and **binary files**.

Files like web pages, computer source code, and open-source programming languages are written in plain text. These files consist of only text characters (UTF-8 and UTF-16). 

These files can opened in a text editor, but editing them is difficult without understanding the particular format, language, or structure of the text itself.

***

## Types of files (2)

Binary files require software to open them, and are typically not human readable.

- Files like Microsoft Word and other proprietary software files  
- Executable files like application installation files (.dmgs or .exe)  
- Media files like .png, .jpg .mp4 or .mov files  
- Encryption or compression files (.zip or .rar)  

These files need software to open and edit, and usually can't be viewed via the command line.

***

## Rectangular files

These are files stored in columns and rows (or variables and observations)

Rectangular files can be opened in spreadsheet software (Excel or OpenOffice) or relational database software

Understanding how to access, manipulate, and extract the information in rectangular files (i.e. spreadsheets) is an essential part of data work because of how ubiquitous tabular data are. An absolute must read for data in spread sheets is, ["Data Organization in Spreadsheets"](https://www.tandfonline.com/doi/full/10.1080/00031305.2017.1375989) by Karl Broman and Kara Woo. 

## Non-rectangular files (JSON & XML)

Non-rectangular data files (like JSON and XML) are commonly used on the web for storing data. 

JSON were created in 2002, and used for data storage and transfer.

XML is slightly older technology (created in 1996), but still widely used for the same purpose.

Non-rectangular data files (like JSON and XML) are commonly used on the web. [JSON](https://www.json.org/) (pronounced Jay-SON) is the JavaScript Object Notation format, and it looks a little like a list (if you've seen these before). [XML](https://en.wikipedia.org/wiki/XML) (or extensible markup language) is a data description language that can be used for storing data. It is particularly useful as a format for sharing information between different software systems.







