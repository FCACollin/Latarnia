+++
date = "201223"
title = "Pharma - R + {rtables}: Tables"
draft = false
image = "img/portfolio/rtables.png"
showonlyimage = false
weight = -201223
+++

2020-12-23


<!--more-->


When working for Roche, I was involved in _NEST_, a project developing a
set of tools for the production of tables, figures and listings meeting
pharma requirements. The package `rtables`, developed at Roche by
Gabriel Becker & Adrian Waddell, was the
corner stone for the tables offering an appealing framework:

With this simple readable code:

    basic_table() %>% 
      split_cols_by(var = "ARMCD") %>%
      add_colcounts() %>%
      analyze(c("AGE", "SEX"), s_summary) %>%
      build_table(ADSL) 

You could get:

                          A: Drug X     B: Placebo    C: Combination
    ----------------------------------------------------------------
    AGE                                                             
      n                      134            134            132      
      Mean (sd)          33.77 (6.55)   35.43 (7.9)    35.43 (7.72) 
      IQR                     11            10              10      
      min - max            21 - 50        21 - 62        20 - 69    
    SEX                                                             
      F                       79            77              66      
      M                       51            55              60      
      U                       3              2              4       
      UNDIFFERENTIATED        1              0              2       

[_A Not So Short Introduction to rtables_](
https://waddella.github.io/RStudioTableContest2020/A_Not_So_Short_Introduction_to_rtables.html
) (by Gabriel Becker & Adrian Waddell, 2020) is available as a _GitHub_ page;
it was proposed at the [_2020 RStudio Table Contest_](
https://blog.rstudio.com/2020/12/23/winners-of-the-2020-rstudio-table-contest/).



```
@Manual{,
    title = {rtables: Reporting Tables},
    author = {Gabriel Becker and Adrian Waddell},
    year = {2021},
    note = {R package version 0.3.6},
    url = {https://CRAN.R-project.org/package=rtables},
}
  
```

[modeline]: # ( vim: set foldlevel=0 spell spelllang=en_gb: )
