# LaTeX Assignment Template — Lean Overleaf Version
 
A lean LaTeX template for STEM assignments, optimised for fast compilation on Overleaf. This is the collaboration version of the full template — use it to write and collaborate on Overleaf, then transfer your content to the full template for final local compilation.
 
> **Full template:** https://github.com/TylerBignell/LaTeX-AssignmentTemplate
 
---
 
## Purpose
 
This template is intentionally stripped down. Several packages that improve the final appearance of the document — such as `tikz`, `pgfplots`, `microtype`, and heading formatters — are commented out or removed to keep Overleaf compile times short. The trade-off is that the document will not look as polished as the full template, but it will compile quickly and reliably during collaboration.
 
When your content is finished, transfer your `content.tex` file to the full template and compile locally for the final submission-ready PDF.
 
---
 
## Recommended Workflow
 
1. Write and collaborate using this template on Overleaf
2. Keep all your work in `content.tex`
3. When ready for final submission, copy `content.tex` into the full template and compile locally
Both templates use identical metadata fields, environments, and commands. Your content file transfers with no changes needed.
 
---
 
## Quick Start
 
1. Fill in the metadata block at the top of `main.tex`
2. Write your content in `content.tex`
3. Compile on Overleaf — bibliography is handled automatically
---
 
## File Structure
 
```
├── assets/
│   ├── stemtemplate-overleaf.sty     ← Lean template (don't edit)
│   ├── example.tex                   ← Example showing available features
│   └── example.pdf                   ← Compiled example from the full template
├── figures/                          ← Place your images here
├── main.tex                          ← Edit metadata here, compile this file
├── content.tex (create this)         ← Write your content here and transfer to the full template
└── references.bib (create this)      ← Your bibliography entries
```
 
The `example.pdf` is compiled from the full template so you can see what the finished document looks like locally. Read it alongside `example.tex` to understand how each feature is used.
 
---
 
## Metadata
 
The metadata block in `main.tex` controls document settings such as your name, course, and bibliography style. Most of these settings affect the title page and header, which matter more in the full template where the final formatting is applied. On Overleaf, the metadata still needs to be filled in correctly so the document compiles, but the visual output will be plainer than the final version.
 
For a full explanation of every metadata field and what it does, see the full template documentation.
 
```latex
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% METADATA (EDIT FOR EACH SUBMISSION)
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\newcommand{\metaAssignmentTitle}{Assignment Title}
\newcommand{\metaStudentName}{Your Name}
\newcommand{\metaStudentNumber}{123456789}
\newcommand{\metaStudentEmail}{email@my.yorku.ca}
\newcommand{\metaPartners}{}   % "Jane Doe & 123456789\\John Doe & 123456789"
\newcommand{\metaUniversity}{York University}
\newcommand{\metaFaculty}{Lassonde School of Engineering}
\newcommand{\metaDepartment}{Department Name}  % Leave empty to omit
\newcommand{\metaCourseCode}{Course Code}
\newcommand{\metaCourseName}{Course Name}
\newcommand{\metaInstructor}{Dr. Professor}
\newcommand{\metaDate}{Due date}
\newcommand{\metaLogoPath}{assets/logo.png}    % Leave empty to omit
 
% TITLE PAGE
\newcommand{\metaTitlePage}{standard}          % standard, abstract, or compact
 
% BIBLIOGRAPHY
\newcommand{\metaBibFile}{references.bib}
\newcommand{\metaBibStyle}{ieee}               % ieee or apa
\newcommand{\metaShowBackref}{true}            % true or false
\newcommand{\metaShowUnusedCitations}{false}   % true or false
 
% APPEARANCE
\newcommand{\metaDefaultFont}{sans}            % sans or serif
\newcommand{\metaLineSpacing}{onehalf}         % single, onehalf, or double
\newcommand{\metaShowTodo}{true}               % true or false
\newcommand{\metaWatermarkText}{}              % Leave empty for no watermark
\newcommand{\metaWatermarkScale}{1}
 
% COLOURS
\newcommand{\metaThemeColour}{}   % Hex code, colour name, or leave empty for default
\newcommand{\metaLinkColour}{}
\newcommand{\metaCiteColour}{}
\newcommand{\metaUrlColour}{}
 
% NUMBERING BY SECTION
\newcommand{\metaNumberEquations}{true}
\newcommand{\metaNumberFigures}{true}
\newcommand{\metaNumberTables}{true}
\newcommand{\metaNumberTheorems}{true}
\newcommand{\metaNumberProblems}{true}
\newcommand{\metaNumberAlgorithms}{true}
\newcommand{\metaNumberListings}{true}
 
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% ABSTRACT
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\newcommand{\metaAbstract}{Type abstract here.}
```
 
---
 
## Uncommenting Packages
 
Some packages are commented out by default to reduce compile time. If your project needs them, uncomment the relevant lines in `assets/stemtemplate-overleaf.sty`:
 
| Package | What it enables |
|---|---|
| `tikz` | Flowcharts and block diagrams |
| `pgfplots` | Data plots and function graphs |
| `circuitikz` | Circuit schematics |
| `algorithm` + `algpseudocode` | Pseudocode listings |
| `mhchem` | Chemical equations via `\ce{}` |
| `pdfpages` | Inserting external PDF pages |
 
Note that uncommenting `tikz`, `pgfplots`, or `circuitikz` will noticeably increase compile time on Overleaf.
 
---
 
## Logo
 
The faculty logo is not included in this repository. Download the official logo from the [York University Brand Assets page](https://www.yorku.ca/brand/assets-downloads/faculty-assets/) and upload it to the `assets/` folder on Overleaf. Then update `\metaLogoPath` in the metadata.
 
Leave `\metaLogoPath` empty to display no logo.
 
---
 
## Acknowledgements
 
This template was developed with the assistance of generative AI.
 
---
 
## License
 
MIT License — see [LICENSE](LICENSE) for details.
 
Copyright (c) 2026 Tyler Bignell
 
York University and faculty logos are the property of York University and are not covered by this license.
