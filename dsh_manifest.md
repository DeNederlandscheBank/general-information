# DNB Data Science Community Manifest
Working with data has always been a core competency at De Nederlandsche Bank (DNB). Given the increased availability of data and new tools becoming available, interest is growing and a community is emerging. Community membership comes with benefits but also with responsibilities. Joining our community implies adhering to the principles laid out in this document.

## Introduction 
A "paper trail" is the cornerstone of any policy institution. In designing, setting and upholding policy we should be able to explain how the available information has shaped our thinking. Some of this information is soft (e.g., impression, market views) but we aim to be increasingly data driven.

New tools and technologies, massive amounts of data (certainly since the Great Financial Crisis), interdisciplinary approaches, and the complexity of the questions being asked are complicating efforts to follow the `paper trail' that has resulted in policy relevant conclusions. 

As full step-by-step replication of analysis – sometimes with ad hoc data – is often not feasible, we should aim for reproducible analysis as an attainable minimum standard for assessing the value of policy conclusions. This requires that analyses describe the results and provide a sufficiently clear protocol to allow successful repetition and extension of analyses based on original data.

The importance of replication and reproducibility is key to being transparent about our policy process, to be consistent over time and across institutions, and be able to reap cross-divisional efficiency benefits. 

Reproducibility is not only a moral responsibility with respect to our professional calling, but a lack of reproducibility can also be a burden for you as an individual analyst. As an example, a good practice of reproducibility is necessary in order to allow previously developed methodology to be effectively applied on new data, or to allow reuse of code and results for new projects. In other words, good habits of reproducibility may actually turn out to be a time-saver in the longer run. The challenge is to let these long run benefits get the better of the short run time pressures.

Note also that reproducibility is just as much about the habits that ensure reproducible research as the technologies that can make these processes efficient and realistic. Each of the following rules captures a specific aspect of reproducibility, and discusses what is needed in terms of information handling and tracking of procedures. If you are taking a bare-bones approach to analysis, i.e., running various custom scripts from the command line or – worse – in Excel, you will probably need to handle each rule explicitly. If you are instead performing your analyses through an integrated framework (such as GITLab, the OSBE-IMK R-package or the VPS-ECDB python-packages), the system may already provide partial or full support for most of the rules. What is needed on your part is then merely the knowledge of how to exploit these existing possibilities. The Data Science Community is there to help you find your way in this respect.

At DNB, with meeting deadlines and SSM requests, you may face the need to make a trade-off between the ideals of reproducibility and the need to get the analysis out while it is still relevant. This trade-off becomes more important when considering that a large part of the analyses being tried out never end up yielding any results. However, frequently you will, with the wisdom of hindsight, contemplate the missed opportunity to ensure reproducibility, as it may already be too late to take the necessary notes from memory (or at least much more difficult than to do it while underway). We believe that the rewards of reproducibility will compensate for the risk of having spent valuable time developing an annotated catalogue of analyses that turned out as blind alleys.

As a minimal requirement, you should be able to reproduce results yourself. This would satisfy the most basic requirements of sound policy research, allowing any substantial future questioning of the policy decisions to be met with a precise explanation. Although it may sound like a very weak requirement, even this level of reproducibility will often require a certain level of care in order to be met. For any analysis there will be an exponential number of possible combinations of software versions, parameter values, pre-processing steps, and so on, meaning that a failure to take notes may make exact reproduction essentially impossible.

With this basic level of reproducibility in place, there is much more that can be wished for. An obvious extension is to go from a level where you can reproduce results in case of a critical situation to a level where you can practically and routinely reuse your previous work and increase your productivity. A second extension is to ensure that colleagues have a practical possibility of reproducing your results, which can lead to reaping cross-divisional efficiency gains.

In parallel to this manifest we are also developing more practical best practice: what naming convention to use? How to use GITLab on RAN Secure and so on and so forth. You can find this living document on SharePoint (link).

## The Rules
With this in mind, we come to the following rules to make your analysis more accessible — be it for colleagues, externals or for your future self. Although we use the prescriptive ‘rule’, we should come to see these as self-imposed commandments that will make working together easier. To have a solid starting point we borrow extensively from Sandve et al (2013) in this draft.  Over time we should make more of the text our own.

- Rule 1:	For Every Result, Keep Track of How It Was Produced
- Rule 2:	Avoid Manual Data Manipulation Steps
- Rule 3:	Archive the Exact Versions of All External Programs Used
- Rule 4:	Version Control all Custom Scripts
- Rule 5:	Add more Comments than you need yourself
- Rule 6:	Record All Intermediate Results – if Possible in Standardized Formats
- Rule 7:	Always Store Raw Data behind Plots
- Rule 8:	Generate Hierarchical Analysis Output, Allowing Layers of Increasing Detail to Be Inspected	
- Rule 9:	Provide the widest possible Access to Scripts and Results	
- Rule 10: Celebrate

## Rule 1:	For Every Result, Keep Track of How It Was Produced
You will frequently find that getting from raw data to the final result involves many interrelated steps (single commands, scripts, programs). We refer to such a sequence of steps, whether it is automated or performed manually, as an analysis workflow. While the essential part of an analysis is often represented by only one of the steps, the full sequence of pre- and post-processing steps are often critical in order to reach the achieved result.
Best Practices:
-	Keep track of how a result was produced whenever it may be of potential interest. For every involved step, ensure that every detail that may influence the execution of the step is recorded. If the step is performed by a computer program, the critical details include the name and version of the program, as well as the exact parameters and inputs that were used.
-	Specify the full analysis workflow in a form that allows for direct execution to ensure that the specification matches the analysis that was (subsequently) performed, and that the analysis can be reproduced by yourself or others in an automated way. Such executable descriptions might come in the form of simple .do files, at the command line, or in the form of stored workflows in a workflow management system (e.g. SAS EG). This avoids getting the documentation get out of sync with how the analysis was really performed in its final version.
-	Many analyses and predictions include some element of randomness, meaning the same program will typically give slightly different results every time it is executed (even when receiving identical inputs and parameters). However, given the same initial seed, all random numbers used in an analysis will be equal, thus giving identical results every time it is run. Therefore, random elements should in principle be reproduced exactly.
What you should do as a minimum:
-	Record sufficient details on programs, parameters, and manual procedures to allow yourself, in a year or so, to approximately reproduce the results.
-	Manually note the precise sequence of steps taken to be able to reproduce the analysis.

## Rule 2:	Avoid Manual Data Manipulation Steps
There will typically be a quite rich collection of components for data manipulation. Manual procedures are not only inefficient and error-prone, they are also difficult to reproduce. 
Best Practices:
-	Rely on the execution of programs instead of manual procedures to modify data as much as possible. 
-	To attain format compatibility, replace manual tweaking of data files by dedicated format converters or general purpose languages that can be re-enacted and included into executable workflows. 
-	Avoid other manual operations like the use of copy and paste between documents.
What you should do as a minimum:
-	If manual operations cannot be avoided, note down which data files were modified or moved, and for what purpose.

## Rule 3:	Archive the Exact Versions of All External Programs Used
In order to exactly reproduce a given result, it may be necessary to use programs in the exact versions used originally. Also, as both input and output formats may change between versions, a newer version of a program may not even run without modifying its inputs. Even having noted which version was used of a given program, it is not always trivial to get hold of a program in anything but the current version.
Best Practices:
-	Archive the exact versions of programs actually used to save a lot of hassle at later stages. In some cases, all that is needed is to store a single executable or source code file. In other cases, a given program may again have specific requirements to other installed programs/packages, or dependencies to specific operating system components. To ensure future availability, the only viable solution may then be to store a full virtual machine image of the operating system and program.
What you should do as a minimum:
-	Note the exact names and versions of the main programs you use.

## Rule 4:	Version Control all Custom Scripts
Even the slightest change to a computer program can have large intended or unintended consequences. When a continually developed piece of code (typically a small script) has been used to generate a certain result, only that exact state of the script may be able to produce that exact output, even given the same input data and parameters. As also discussed for rules 3 and 6, exact reproduction of results may in certain situations be essential. If computer code is not systematically archived along its evolution, backtracking to a code state that gave a certain result may be a hopeless task. This can cast doubt on previous results, as it may be impossible to know if they were partly the result of a bug or otherwise unfortunate behavior. Thus even when approximate reproduction is sufficient, small differences in outcomes will absorb disproportionate effort because you need to make sure these differences are not due to material errors.
Best Practices:
-	Use a standard version control solution to track the evolution of code, GITLab in our case. GITLab is easy to set up and use, and may be used to systematically store the state of the code throughout development at any desired time granularity.
What you should do as a minimum:
-	Archive copies of your scripts from time to time, so that you keep a rough record of the various states the code has taken during development.

## Rule 5:	Add more Comments than you need yourself
Comment your code as much as possible and needed. The comments are essential to understand what your code is doing. It also helps the reader to understand what the way of thinking of the programmer was – which may not be immediately obvious from the code. Don’t underestimate the many ways a reader – who might be your future self – can misunderstand. Therefore you should add more explanation than what you think is necessary at the time of writing.
Best Practices:
-	Add a description to every script and every function.

## Rule 6:	Record All Intermediate Results – if Possible in Standardized Formats
In principle, as long as the full process used to produce a given result is tracked, all intermediate data can also be regenerated. In practice, having easily accessible intermediate results may be of great value. Quickly browsing through intermediate results can reveal discrepancies toward what is assumed, and can in this way uncover bugs or faulty interpretations that are not apparent in the final results. Secondly, it more directly reveals consequences of alternative programs and parameter choices at individual steps. Thirdly, when the full process is not readily executable, it allows parts of the process to be rerun. Fourthly, when reproducing results, it allows any experienced inconsistencies to be tracked to the steps where the problems arise. Fifth, it allows critical examination of the full process behind a result, without the need to have all executables operational. 
Best Practices:
-	Store intermediate results in standardized formats as much as possible.
What you should do as a minimum:
-	Archive any intermediate result files that are produced when running an analysis (as long as the required storage space is not prohibitive).

## Rule 7:	Always Store Raw Data behind Plots
From the time a figure is first generated to it being part of a published article, it is often modified several times. In some cases, such modifications are merely visual adjustments to improve readability, or to ensure visual consistency between figures. 
Best Practices:
-	Store raw data behind figures in a systematic manner so you can simply modify the plotting procedure by retrieving the data, instead of having to redo the whole analysis. An additional advantage of this is that if you need the exact values in a plot, you can consult the raw numbers. 
-	In cases where plotting involves more than a direct visualization of underlying numbers, store both the underlying data and the processed values that are directly visualized. An example of this is the plotting of histograms, where both the values before binning (original data) and the counts per bin (heights of visualized bars) could be stored. 
-	When plotting is performed using a command-based system like Stata, Pyhon or R, store the code used to make the plot. You can then apply slight modifications to these commands, instead of having to specify the plot from scratch.
What you should do as a minimum:
-	Make sure that from the name of the output it is clear where in the code the output is generated. So, naming a graph “total.svg” is not helpful.
-	Note which data formed the basis of a given plot and how this data could be reconstructed.

## Rule 8:	Generate Hierarchical Analysis Output, Allowing Layers of Increasing Detail to Be Inspected
The final results that make it to an article, be it plots or tables, often represent highly summarized data. For instance, each value along a curve may in turn represent averages from an underlying distribution. In order to validate and fully understand the main result, it is often useful to inspect the detailed values underlying the summaries. A common but impractical way of doing this is to incorporate various debug outputs in the source code of scripts and programs. 
Best Practices:
-	When the storage context allows, incorporate permanent output of all underlying data when a main result is generated, using a systematic naming convention to allow the full data underlying a given summarized value to be easily found. We find hypertext (i.e., html file output) to be particularly useful for this purpose. This allows summarized results to be generated along with links that can be very conveniently followed (by simply clicking) to the full data underlying each summarized value. 
What you should do as a minimum:
-	When working with summarized results, at least once generate, inspect, and validate the detailed values underlying the summaries. 

## Rule 9:	Provide the widest possible Access to Scripts and Results
Making reproducibility of your work by other authorities and the general public a realistic possibility sends a strong signal of quality, trustworthiness, and transparency.
Best Practices:
-	Make available as wide as possible all input data, scripts, versions, parameters, and intermediate results. In some cases, this circle will be very small but in most cases, the vast majority of the code developed is not in itself sensitive. For those parts of the code that are shareable we should strive to share this with other central banks and supervisors or even beyond.  
What you should do as a minimum:
-	Have your scripts reviewed by a peer, who is not working on the project. Such a reviewer is more likely to spot implicit choices arising from tunnel vision or flaws in the line of reasoning. Also, you’ll receive feedback whether your code is understandable (see rule 5) and errors might be pointed out.

## Rule 10:	 Celebrate
Celebrate success. Data Science is hard work and requires perseverance to get to a (monitoring) tool or a scientific paper. Take some time to celebrate achievements with the group.

References
Sandve GK, Nekrutenko A, Taylor J, Hovig E (2013) Ten Simple Rules for Reproducible Computational Research. PLOS Computational Biology 9(10): e1003285. https://doi.org/10.1371/journal.pcbi.1003285
