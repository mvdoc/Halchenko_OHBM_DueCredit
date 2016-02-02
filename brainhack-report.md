---
event: '2015 OHBM Hackathon (HI)'

title:  'DueCredit: automated collection of citations for software, methods, and data'

author:

- initials: YOH
  surname: Halchenko
  firstname: Yaroslav O.
  email: yoh@onerussian.com
  affiliation: aff1
  corref: aff1
- initials: MVdOC
  surname: Visconti di Oleggio Castello
  firstname: Matteo
  email: matteo.visconti.gr@dartmouth.edu
  affiliation: aff1

affiliations: 

- id: aff1
  orgname: 'Department of Pscyhological & Brain Sciences, Dartmouth College'
  street: 6207 Moore Hall
  postcode: 03755
  city: Hanover
  state: New Hampshire
  country: USA


url: https://github.com/duecredit/duecredit

coi: None

acknow: The authors would like to thank the organizers and attendees of the 2015 OHBM Hackathon. This project is supported in part by a grant from the NSF (award 1429999).

contrib: YOH and MVdOC performed the project and wrote the report.
  
bibliography: brainhack-report

gigascience-ref: REFXXX
...

#Introduction
Data analysis software and canonical datasets are the driving force behind many fields of empirical sciences. Despite being of paramount importance, those resources are most often not adequately cited. Although some can consider this a “social” problem, its roots are technical: Users of those resources often are simply not aware of the underlying computational libraries and methods they have been using in their research projects. This in-turn fosters inefficient practices that encourage the development of new projects, instead of contributing to existing established ones. Some projects (e.g. FSL \cite{smith2004advances}) facilitate citation of the utilized methods, but such efforts are not uniform, and the output is rarely in commonly used citation formats (e.g. BibTeX). DueCredit is a simple framework to embed information about publications or other references within the original code or dataset descriptors. References are automatically reported to the user whenever a given functionality or dataset is being used.

#Approach
DueCredit is currently available for Python, we envision extending support to other frameworks (e.g., Matlab, R).  Until DueCredit gets adopted natively by the projects, it provides the functionality to “inject” references for 3rd party modules. 

#Results
The initial release of DueCredit (0.1.0) was implemented during the OHBM 2015 hackathon and uploaded to pypi and is freely available. DueCredit provides a concise API to associate a publication reference with any given module or function. For example: To provide a reference for an entire module the cite function can be used, while functions and methods can be conveniently decorated using dcite. DueCredit comes with a simple demo code which demonstrates its utility. Running a sample analysis produces a summary of references. At each run, the information is stored in a pickled file, and incremental runs update that file. Thus, DueCredit summary can be used to show that information again or export it as a BibTeX file ready for reuse.


# Conclusions
DueCredit is in its early stages of development, but two days of team development at the OHBM hackathon were sufficient to establish a usable prototype implementation.  Since then, the code-base was further improved and multiple beta-releases followed, expanding the coverage of citable resources (e.g., within scipy, sklearn modules via injections and PyMVPA natively).
