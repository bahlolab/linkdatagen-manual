[![Quarto publish to bioinf](https://github.com/bahlolab/linkdatagen-manual/actions/workflows/push_to_bioinf.yml/badge.svg)](https://github.com/bahlolab/linkdatagen-manual/actions/workflows/push_to_bioinf.yml) [![Quarto publish to Netlify](https://github.com/bahlolab/linkdatagen-manual/actions/workflows/publish_netlify.yml/badge.svg)](https://github.com/bahlolab/linkdatagen-manual/actions/workflows/publish_netlify.yml)

This is the source of the [LINKDATAGEN](https://github.com/bahlolab/linkdatagen) manual: 
- Website: [linkdatagen.netlify.app](https://linkdatagen.netlify.app "LINKDATAGEN Manual") 
- PDF: [linkdatagen-manual.pdf](http://linkdatagen.netlify.app/linkdatagen-manual.pdf) 
- MS Word: [linkdatagen-manual.docx](http://linkdatagen.netlify.app/linkdatagen-manual.docx)

This is currently a work in progress and users should continue to download documentation at https://bioinf.wehi.edu.au/software/linkdatagen/

If you spot **spelling/grammar mistakes** in the manual, please [submit an issue](https://github.com/bahlolab/linkdatagen-manual/issues). Pull requests should be accompanied by the note: "I assign the copyright of this contribution to Melanie Bahlo".

**Questions** about the LINKDATAGEN software should be submitted to [LINKDATAGEN Discussions](https://github.com/bahlolab/linkdatagen/discussions). To lodge a **bug report** on LINKDATAGEN, please [submit an issue to the LINKDATAGEN repository](https://github.com/bahlolab/linkdatagen/issues). Alternatively, you may email Melanie Bahlo at [bahlo\@wehi.edu.au](mailto:bahlo@wehi.edu.au){.email}.

# Build

This book is built with [Quarto](https://quarto.org) and can be previewed from within RStudio. This repository is set up to automatically update the [online manual](https://linkdatagen.netlify.app "LINKDATAGEN Manual") including the PDF and MS Word versions. If the website is not updating, please check the [Actions](https://github.com/bahlolab/linkdatagen-manual/actions/) have succeeded (a green tick).

In the future this may publish to the [Bioinf website](https://bioinf.wehi.edu.au/software/linkdatagen/). 
It will work by committing changes to the [WEHI-ResearchComputing/bioinf_rehost](https://github.com/WEHI-ResearchComputing/bioinf_rehost) repository through a Github action. 
This is currently by using a token provided by Rick Tankard that is set to expire on Thu, 7 Sep 2023. If Rick is no longer around, the following actions should be take: 

- A user, who will have their name attached to commits to bioinf_rehost, will have to generate a [personal access token](https://github.com/settings/tokens) on Github with the repo scope only. It is recommended to create a token that expires, up to one year away. 
- Copy the token and create and [update the value of the repository secret](https://github.com/bahlolab/linkdatagen-manual/settings/secrets/actions) REPO_ACCESS_TOKEN with this value. 
- Edit the file [.github/workflows/push_to_bioinf.yml](.github/workflows/push_to_bioinf.yml), changing: 
  - instances of 'trickytank' to your user name on Github 
  - "Rick Tankard" to your name 

For now this is pushing to a test Github repository to check the concept works.
