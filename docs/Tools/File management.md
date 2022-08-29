## How to name your files?
Created: 2022-07-12; Updated: 2022-08-08
Tags: #fundamental-skill; #data-managment 

Continue from https://uppsala.instructure.com/courses/58273/pages/data-organisation-practices-episodes-104-data-preservation-md?module_item_id=490224

It looks like a simple question, but I can't find a simple solution. Based on Git, my documentaries categories, I decide to name my files in such ways:

| File Category | Type | Format | Example | Note |
| Study Notes | markdown | descriptive name | File management | Organized by obsidian |
|  Grant proposal             |   word   |  [year]-[funding]-[PI's last name]-[Status]      |         |      |
### 1. Study notes
File types: Markdown for GitHub pages
Formats: Descriptive name with space, as the file name will be as title in GitHub pages
Example: File Management.md
Notes: Organized by obsidian

File types: PDF or other formats as resources
Formats: [Author] - [Year] - [Journal/Book]

### 2. Manuscript
File types: Words or others
Formats: [First author's last name] - [Project/Title Abbr.] - [Sections] - [Status] - [Version v1.2] - [Initial names] - [comments]

### 3. Grant proposals
File types: Words
Formats: [Numbers for sections/steps XX 01] - [PI's last name] - [funding] - [year] - [Project/Title Abbr.] - [Sections] - [Status] - [Version v1.2] - [Initial names] - [comments]

### 4. rmarkdown file
File types: rmarkdown [.Rmd]
Formats: [Date of creation] -  [Project/Title Abbr.]  - [Output type] - [Analysis]- [Initial names] - [status]
[Output type] -
reports-MOHUB-tidy-data-li-draft
220810-MOHUB-reports-tidy-data-li-draft
? date is not good in tracking

### 5. R codes
File types: r function script [.r]
Formats: [function name]


### Resources
#### Three principles for (file) names[^1]:
1.  Machine readable
2.  Human readable
3.  Plays well with default ordering
#### Elements to consider using in a naming convention are[^2]:

-   Date of creation (putting the date in the front will facilitate computer aided date sorting)
-   Short Description
-   Work
-   Location
-   Project name or number
-   Sample
-   Analysis
-   Version number

## A file name can consist of the following parts [^3]:

• A prefix that shows the type of document a file is  
• A title: this should be as informative as possible so that the document content can be understood from its title  
• The version number of the document  
• Date displayed when created: use YYMMDD format  
• Document status: draft or final  
• Author's initials: who last changed it

## Introduction to Data Management practices[^4]
Example of README.txt
![[Pasted image 20220808172515.png]]

A well suited file naming protocol should be:

1.  **Human readable** - A name describes the content of the file, connects to concept of a _slug_ from semantic URLs (e.g. www.scilifelab.se/_this-is-a-slug_). Makes it easy to understand what the file is and what it contains, from just reading the file name
2.  **Machine readable** – Avoid spaces, deliberate punctuation, accented or odd characters, inconsistent letter casing
3.  **Default ordered** – Put something numeric first, use the ISO 8601 standard for dates (YYYYMMDD, or YYYY-MM-DD), left pad single digits with zeros (01, 02, 03… 10)

In practise:

-   Balance the amount of elements: too many makes it difficult to understand vs. too few makes it generic (**Human readable**)
-   Order elements from general to specific (**Human readable**)
-   Use meaningful abbreviations (**Human readable**)
-   Replace whitespace with underscore (_), hyphen (-) or capitalized letters to separate elements in the name.
-   Avoid using special characters: ?!& , * % # ; * ( ) @$ ^ ~ ‘ { } [ ] < > (**Machine readable**)
-   Use date format ISO8601: YYYYMMDD, and time if needed HHMMSS, or in combination YYYYMMDD:HHMMSS (**Machine readable**)
-   Include a version number if appropriate (**Human readable**)
-   Write your file naming convention down and explain abbreviations in your data documentation (**Human readable**)

Examples of **good file names**:

-   Honeybee project, experiment 2 done in Helsinki, data file created on the second of December 2020
    -   _File name_: 20201202_HB_EXP2_HEL_DATA_V03.xls
    -   _Explanation_: Time_ProjectAbbreviation_ExperimentNumber_  
        Location_TypeOfData_VersionNumber
-   Cropped image of an ant head taken on the third of December 2020 by Meg Megson
    -   _File name_: 20201203_MM_HEAD_CROPPED_V1.psd
    -   _Explanation_: Time_CreatorData_TypeModification_Version

### Metadata  

A good and informative file name is a great start, but there is a limit to how much information you can pack into a file name before the length itself becomes a problem. This is where metadata comes in. For the purpose of findability we can associate the file name with metadata stored elsewhere, for example in a text file kept together with the files.

   **Pros**: Possible to enrich any file with unlimited amounts of metadata  
      **Cons**: Can be cumbersome to keep updated as number of files increase and file names are changed

> ### Example and Exercise
> 
> 20220115_GenAnn_AssemblyProj1_UME_Pipeline1_Firstrun.xml  
> 
> Writing an example of metadata information explaining the above file names and the file contents, describing the file and where and how to provide it could look like this:
> 
> 20220115_GenAnn_AssemblyProj1_UME_Pipeline1_Firstrun.xml
> 
> (Metadata.txt content)  
> `20220115_GenAnn_AssemblyProj1_UME_Pipeline1_Firstrun.xml   Genome annotation made 220115 in My first assembly project run in Umeå   using primary pipeline for the first time   `  
> Here the file Metadata.txt includes the file name on the first row, and associates it with non-abbreviated additional data not possible to fit into the file name itself. By adding it separately and associating it with the file name we increase findability a lot.
> 
> For the following filename, construct a metadata explanation similar to the one in the example above:
> 
> 20220310_GenAnn_AssemblyProj2_GOT_Dataiteration_2nd_try.xml

Keyword tagging

[^1]: [File Organization: Naming](https://datacarpentry.org/rr-organization1/01-file-naming/index.html)
[^2]: [Research Data Management at Princeton](https://libguides.princeton.edu/c.php?g=102546&p=930626#s-lg-box-2783109)
[^3]: [File organization, naming, versioning and formats from KI.se](https://staff.ki.se/file-organization-naming-versioning-and-formats)
[^4]: [Course from NBIS: Introduction to Data Management practices](https://uppsala.instructure.com/courses/58273)