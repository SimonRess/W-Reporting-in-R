---
title: |
       ![](Slides_files/RUB.jpg){width=2.5in}
subtitle:  "The Influence of the German Statutory Minimum Wage's Introduction on Individuals' Health"
author: "Simon Ress | Ruhr-Universität Bochum"
institute: "Conference: 56. Jahrestagung der DGSMP, Leipzig, 2021"
date: "September 22, 2021"

output:
  beamer_presentation:
    keep_md: true
    keep_tex: no
    latex_engine: xelatex
    #theme: metropolis
    slide_level: 2 # which header level should be printed as slides
    incremental: no
header-includes:
  - \usetheme[numbering=fraction]{metropolis}
#Define footer:
  - \definecolor{beaublue}{rgb}{0.74, 0.83, 0.9}
  - \setbeamertemplate{frame footer}{\tiny{\textcolor{beaublue}{Conference 56. Jahrestagung der DGSMP, 2021 | SIMON RESS}}}
#hide footer on title page:
  - |
    \makeatletter
    \def\ps@titlepage{%
      \setbeamertemplate{footline}{}
    }
    \addtobeamertemplate{title page}{\thispagestyle{titlepage}}{}
    \makeatother
#show footer on section's start/title pages:
  #overwrite "plain,c,noframenumbering" in section pages definition -> enables footer:
  - |
    \makeatletter
    \renewcommand{\metropolis@enablesectionpage}{
      \AtBeginSection{
        \ifbeamer@inframe
          \sectionpage
        \else
          \frame[c]{\sectionpage}
        \fi
      }
    }
    \metropolis@enablesectionpage
    \makeatother
  #define footer of section pages:
  - |
    \makeatletter
    \def\ps@sectionpage{%
      \setbeamertemplate{frame footer}{\tiny{\textcolor{beaublue}{Conference 56. Jahrestagung der DGSMP, 2021 | SIMON RESS}}}
    }
    \addtobeamertemplate{section page}{\thispagestyle{sectionpage}}{}
    \makeatother
#add secrtion numbers to TOC:
  - |
    \setbeamertemplate{section in toc}{
    \leavevmode%
    \inserttocsectionnumber. 
    \inserttocsection\par%
    }
    \setbeamertemplate{subsection in toc}{
    \leavevmode\leftskip=2.5em\inserttocsubsection\par}
---




## Content
\tableofcontents[]

# Level I

Test

## Slide with Bullets

- Bullet 1
- Bullet 2
- Bullet 3

# Slide with R Output


```r
summary(cars)
```

```
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
```

## Slide with Plot

![](Slides_files/figure-beamer/pressure-1.pdf)<!-- --> 



## Two columns

Here is some text above which goes over to whole slide

<!-- -------------------------- -->
<!-- Start of two column layout -->

:::::::::::::: {.columns}
::: {.column width="50%"}

![](Slides_files/figure-beamer/AirPassengers-1.pdf)<!-- --> 

:::
::: {.column width="50%"}

- Description of plot
- Second point

:::
::::::::::::::

<!-- End of two column layout -->
<!-- ------------------------ -->


and here some text below which goes over to whole slide
