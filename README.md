<!-- README.md is generated from README.Rmd. Please edit that file -->

# [IEA Data Guidance Doc](https://github.com/IEA-Data/IEA_Data_Guidance_Doc) <img src="https://avatars.githubusercontent.com/u/186961204?s=200&v=4" alt="Logo." align="right" width="139" height="139"/>

Use this repo to engage the broader IEA community to share recommended
approaches/best practices. The scripts therein reproducibly produce our
partner’s typical data products.

> This code is always in development. Find code used for various reports
> in the code
> [releases](https://github.com/IEA-Data/IEA_Data_Guidance_Doc/releases).

## This code is primarally maintained by:

**Emily Markowitz** (Emily.Markowitz AT noaa.gov;
[@EmilyMarkowitz-NOAA](https://github.com/EmilyMarkowitz-NOAA)); NMFS
Alaska Fisheries Science Center **Seann Regan** (Seann.Regan AT
noaa.gov) **Lynn Dewitt** (Lynn.Dewitt AT noaa.gov) **Carissa Gervasi**
(Carissa.Gervasi AT noaa.gov) **Chia-Wei Hsu** (Chia-Wei.Hsu AT
noaa.gov) **Kim Hyde** (Kim.Hyde AT noaa.gov) **Scott Cross**
(Scott.Cross AT noaa.gov) **Brittany Troast** (Brittany.Troast AT
noaa.gov) **Brendan Turley** (Brendan.Turley AT noaa.gov) **Courtney
Bouchard** (Courtney.Bouchard AT noaa.gov) **Cathy Smith** (Cathy.Smith
AT noaa.gov) **Corinne Burns** (Corinne.Burns AT noaa.gov) **Jennifer
Webster** (Jennifer.Webster AT noaa.gov) **Willem Klajbor**
(Willem.Klajbor AT noaa.gov) **Amy Freitag** (Amy.Freitag AT noaa.gov)

> The code in this repository is regularly being updated and improved.
> Please refer to
> [releases](https://github.com/afsc-gap-products/gap_products/releases)
> for finalized products and project milestones.

## Table of contents

``` r
toc <- strsplit(x = readtext::readtext(file = "./README.Rmd", verbosity = 0)[[2]], split = "\n")
toc <- toc[[1]][substr(x = toc[[1]], start = 1, stop = 1) == "#"]
toc <- toc[-c(1:3)]
toc_list <- toc
toc_list <- gsub(pattern = "### ", replacement = ">      - [*", x = toc_list, fixed = TRUE)
toc_list <- gsub(pattern = "## ", replacement = ">    - [*", x = toc_list, fixed = TRUE)
toc_list <- gsub(pattern = "# ", replacement = ">  - [*", x = toc_list, fixed = TRUE)
toc_link <- tolower(gsub(pattern = " ", replacement = "-", 
                          x = gsub(pattern = "#", replacement = "", 
                                   x = gsub(pattern = "# ", replacement = "", 
                                            x = toc, fixed = TRUE), fixed = TRUE)))
toc <- paste0(toc_list, "*](#", toc_link, ")", collapse = "\n")
```

> - \[\* \> - [*badge_lifecycle(“maturing”,
>   “blue”),*](#--badge_lifecycle(%22maturing%22,-%22blue%22),)
> - [\*
>   badge_last_commit(“afsc-gap-products/gap_products”)\*](#--badge_last_commit(%22afsc-gap-products/gap_products%22))
> - [*)*](#))
>   - [*This code is primarally maintained
>     by:*](#this-code-is-primarally-maintained-by:)
>   - [*Table of contents*](#table-of-contents)
>   - [*User Resources*](#user-resources)
>   - [*Access Constraints*](#access-constraints)
> - [*Relevant publications*](#relevant-publications)
> - [*Suggestions and Comments*](#suggestions-and-comments)
>   - [*R Version Metadata*](#r-version-metadata)
>   - [*NOAA README*](#noaa-readme)
>   - [*NOAA License*](#noaa-license)

## User Resources

- [GitHub
  repository](https://github.com/IEA-Data/IEA_Data_Guidance_Doc).

## Access Constraints

There are no legal restrictions on access to the data. They reside in
public domain and can be freely distributed.

**User Constraints:** Users must read and fully comprehend the metadata
prior to use. Data should not be used beyond the limits of the source
scale. Acknowledgement of the Integrated Ecosystem Assessment Program,
as the source from which these data were obtained, in any publications
and/or other representations of these data, is suggested.

**General questions and more specific data requests** can be sent to…
\[enter\]

# Relevant publications

``` r
source("https://raw.githubusercontent.com/afsc-gap-products/citations/main/cite/current_data_tm.r") # srvy_cite 
```

**Learn more about these surveys** ([Hoff, 2016](#ref-RN979); [Markowitz
et al., 2024](#ref-2023NEBS), [2024](#ref-2023NEBS); [Siple et al.,
2024](#ref-GOA2023); [Von Szalay et al., 2023](#ref-AI2022); [Zacher et
al., 2024](#ref-SAPcrab2024)).

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0" line-spacing="2">

<div id="ref-RN979" class="csl-entry">

Hoff, G. R. (2016). *Results of the 2016 eastern Bering Sea upper
continental slope survey of groundfishes and invertebrate resources*
(NOAA Tech. Memo. NOAA-AFSC-339). U.S. Dep. Commer.
<https://doi.org/10.7289/V5/TM-AFSC-339>

</div>

<div id="ref-2023NEBS" class="csl-entry">

Markowitz, E. H., Dawson, E. J., Wassermann, S., Anderson, C. B., Rohan,
S. K., Charriere, B. K., and Stevenson, D. E. (2024). *Results of the
2023 eastern and northern Bering Sea continental shelf bottom trawl
survey of groundfish and invertebrate fauna* (NOAA Tech. Memo.
NMFS-AFSC-487; p. 242). U.S. Dep. Commer.
<https://doi.org/10.25923/2mry-yx09>

</div>

<div id="ref-GOA2023" class="csl-entry">

Siple, M. C., Szalay, P. G. von, Raring, N. W., Dowlin, A. N., and
Riggle, B. C. (2024). *Data report: 2023 gulf of alaska bottom trawl
survey* (NOAA Tech. Memo. AFSC processed report; 2024-09). U.S. Dep.
Commer. <https://doi.org/10.25923/gbb1-x748>

</div>

<div id="ref-AI2022" class="csl-entry">

Von Szalay, P. G., Raring, N. W., Siple, M. C., Dowlin, A. N., Riggle,
B. C., and Laman, E. A. and. (2023). *Data report: 2022 Aleutian Islands
bottom trawl survey* (AFSC Processed Rep. 2023-07; p. 230). U.S. Dep.
Commer. <https://doi.org/10.25923/85cy-g225>

</div>

<div id="ref-SAPcrab2024" class="csl-entry">

Zacher, L. S., Richar, J. I., Fedewa, E. J., Ryznar, E. R., and Litzow,
M. A. (2024). *The 2024 eastern Bering Sea continental shelf trawl
survey: Results for commercial crab species DRAFT* \[NOAA Tech. Memo.\].
<https://www.fisheries.noaa.gov/resource/document/draft-2024-eastern-bering-sea-crab-technical-memorandum>

</div>

</div>

# Suggestions and Comments

If you see that the data, product, or metadata can be improved, you are
invited to create a [pull
request](https://github.com/IEA-Data/IEA_Data_Guidance_Doc/pulls), or
[submit an issue to the code’s
repository](https://github.com/IEA-Data/IEA_Data_Guidance_Doc/issues).

## R Version Metadata

``` r
sessionInfo()
```

    ## R version 4.4.3 (2025-02-28 ucrt)
    ## Platform: x86_64-w64-mingw32/x64
    ## Running under: Windows 10 x64 (build 19045)
    ## 
    ## Matrix products: default
    ## 
    ## 
    ## locale:
    ## [1] LC_COLLATE=English_United States.utf8  LC_CTYPE=English_United States.utf8    LC_MONETARY=English_United States.utf8 LC_NUMERIC=C                           LC_TIME=English_United States.utf8    
    ## 
    ## time zone: America/Los_Angeles
    ## tzcode source: internal
    ## 
    ## attached base packages:
    ## [1] stats     graphics  grDevices utils     datasets  methods   base     
    ## 
    ## loaded via a namespace (and not attached):
    ##  [1] generics_0.1.3          fontLiberation_0.1.0    xml2_1.3.6              stringi_1.8.4           digest_0.6.37           magrittr_2.0.3          readtext_0.91           evaluate_1.0.3          grid_4.4.3              flextable_0.9.7         fastmap_1.2.0           rprojroot_2.0.4        
    ## [13] zip_2.3.1               RODBC_1.3-26            googledrive_2.1.1       httr_1.4.7              purrr_1.0.2             viridisLite_0.4.2       scales_1.3.0            fontBitstreamVera_0.1.1 textshaping_1.0.0       cli_3.6.3               rlang_1.1.5             fontquiver_0.2.1       
    ## [25] munsell_0.5.1           yaml_2.3.10             gdtools_0.4.1           tools_4.4.3             officer_0.6.7           uuid_1.2-1              gargle_1.5.2            dplyr_1.1.4             colorspace_2.1-1        here_1.0.1              kableExtra_1.4.0        vctrs_0.6.5            
    ## [37] R6_2.6.1                lifecycle_1.0.4         stringr_1.5.1           fs_1.6.5                ragg_1.3.3              pkgconfig_2.0.3         gapindex_3.0.2          pillar_1.10.1           data.table_1.16.4       glue_1.8.0              Rcpp_1.0.14             systemfonts_1.2.1      
    ## [49] xfun_0.50               tibble_3.2.1            tidyselect_1.2.1        rstudioapi_0.17.1       knitr_1.49              htmltools_0.5.8.1       svglite_2.1.3           rmarkdown_2.29          compiler_4.4.3          askpass_1.2.1           openssl_2.3.1

## NOAA README

This repository is a scientific product and is not official
communication of the National Oceanic and Atmospheric Administration, or
the United States Department of Commerce. All NOAA GitHub project code
is provided on an ‘as is’ basis and the user assumes responsibility for
its use. Any claims against the Department of Commerce or Department of
Commerce bureaus stemming from the use of this GitHub project will be
governed by all applicable Federal law. Any reference to specific
commercial products, processes, or services by service mark, trademark,
manufacturer, or otherwise, does not constitute or imply their
endorsement, recommendation or favoring by the Department of Commerce.
The Department of Commerce seal and logo, or the seal and logo of a DOC
bureau, shall not be used in any manner to imply endorsement of any
commercial product or activity by DOC or the United States Government.

## NOAA License

Software code created by U.S. Government employees is not subject to
copyright in the United States (17 U.S.C. §105). The United
States/Department of Commerce reserve all rights to seek and obtain
copyright protection in countries other than the United States for
Software authored in its entirety by the Department of Commerce. To this
end, the Department of Commerce hereby grants to Recipient a
royalty-free, nonexclusive license to use, copy, and create derivative
works of the Software outside of the United States.

<img src="https://raw.githubusercontent.com/nmfs-general-modeling-tools/nmfspalette/main/man/figures/noaa-fisheries-rgb-2line-horizontal-small.png" alt="NOAA Fisheries" height="75"/>

[U.S. Department of Commerce](https://www.commerce.gov/) \| [National
Oceanographic and Atmospheric Administration](https://www.noaa.gov) \|
[NOAA Fisheries](https://www.fisheries.noaa.gov/)
