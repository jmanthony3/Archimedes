---
title: ${1:$TM_FILENAME_BASE}
author: ${2:author}
date: ${3:Month} ${4:Year}
site: ${5:url}
tags: 
---
<script type="text/javascript"
        src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS_CHTML">
</script>
<script type="text/x-mathjax-config">
	MathJax.Ajax.config.path["Extra"] = "https://jmanthony3.github.io/Codes/MathJax/extensions/TeX",
	MathJax.Hub.Queue(["Typeset",MathJax.Hub]);
	MathJax.Hub.Config({
		TeX: {
			equationNumbers: {
				autoNumber: "AMS"
			},
			extensions: [
				"[Extra]/Taylor.js",
				"[Extra]/NumericalMethods.js"
			]
		},
		tex2jax: {
			inlineMath: [["$", "$"], ["\\(", "\\)"]],
			blockMath: [["$$", "$$"], ["\\[", "\\]"]],
		},
});
</script>
<!-- %%%%%%%% Document Metadata %%%%%%%% -->
# ${1:$TM_FILENAME_BASE}

Date Created: $CURRENT_MONTH_NAME $CURRENT_DATE, $CURRENT_YEAR

- [${1:$TM_FILENAME_BASE}](#1tm_filename_base)
	- [Annotations](#annotations)
	- [Figures](#figures)
	- [Abstract](#abstract)
	- [Notes](#notes)
		- [Source Subtitle](#source-subtitle)
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- START WRITING BELOW -->





<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->
## Annotations
$0

Sources of Note:
- *insert text here$\dots$*

## Figures

## Abstract
$CLIPBOARD

## Notes
*insert text here$\dots$*

### Source Subtitle
*insert text here$\dots$*
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- %%%%%%%% End Document %%%%%%%% -->