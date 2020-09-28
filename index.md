<!-- You can use the [editor on -->
<!-- GitHub](https://github.com/maple-repair/expression-templates/edit/master/index.md) to maintain and preview the content for your website in Markdown files. -->

<!-- # Automated Program Repair using Formal Specifications. -->

## Abstract
We propose a novel approach to automatically repair buggy heap-manipulating
programs using separation logic specifications.
Given an input program C and its formal specification in the form of a Hoare
triple: {P}~C~{Q}, we
utilize
a verification
system to verify if C is correct against the provided specification.
If the input program is found buggy, we then repair it in the following steps.
We first rely on the verification results to collect suspicious statements
of the buggy program
and rank them
by their
likelihood
to introduce bugs.
For each suspicious statement, we temporarily replace it by a
template patch which may comprise several statements.
We also capture this patch
by using
a pair of
unknown second-order pre- and post-conditions.
We then utilize the verification tool again to analyze the temporarily
patched program to collect constraints
on the specification
of the template patch with the help of the original specification
P and Q.
These constraints
are inferred
by our constraint solver to discover the suitable specification of the
template patch.
This discovered specification can be used to synthesize a candidate
patch for the buggy program.
The candidate patch
is marked as a correct patch
if it is
validated by the verification engine.
We demonstrate the effectiveness of our
method by comparing our implemented tool with a mutation-based approach on
buggy versions of 15 heap-manipulating programs.
Evaluation results show that our tool successfully
repairs {\ourresult} buggy programs and
considerably outperforms a
state-of-the-art specification-based repair tool.

## NEM
NEM is build on top of the [HIP](http://loris-5.d2.comp.nus.edu.sg/hip/index.html)
verification system and [Songbird](https://songbird-prover.github.io/) prover. 

## Compared Tool
- [Enhancing Automated Program Repair with Deductive Verification](https://dblp.org/db/conf/icsm/icsme2016.html#LeLLG16)

<!-- ## The Benchmarks and Experiments. -->
<!-- - The test suites for the *TCAS* benchmark is provided by Xianglong Kong. You -->
<!--   can download by this [link](files/genprog-demo.zip). The benchmark contains 41 -->
<!--   buggy cases. Each case has its own test suite of 40 tests. -->
<!-- - The details about the second benchmark is provided -->
<!-- in [Github](https://github.com/maple-repair/recursive-benchmark). -->
<!-- - The experiments of AllRepair and Forensic are done with the same format which -->
<!--   uses an assertion that compares the results of buggy and correct programs, -->
<!--   e.g. assert(buggy\_sum(x, y) == correct\_sum(x,y) -->
<!-- - For GenProg and Angelix, we create test suites of 10 for each buggy program in -->
<!--   the second experiment. We follow their tutorials in setting up this experiment. -->

## People
- Dr. Wei-Ngan Chin (Associate Professor - National University of Singapore)
- Dr. Ilya Sergey (Associate Professor - National University of Singapore)
- Dr. Quang-Trung Ta (Research Fellow - National University of Singapore) 
- Thanh-Toan Nguyen (PhD Candidate - National University of Singapore)

<!-- ## Our VMCAI paper -->

<!-- ## Header 2 -->
<!-- ### Header 3 -->

<!-- - Bulleted -->
<!-- - List -->

<!-- 1. Numbered -->
<!-- 2. List -->

<!-- **Bold** and _Italic_ and `Code` text -->

<!-- [Link](url) and ![Image](src) -->
<!-- ``` -->

<!-- For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/). -->

<!-- ### Jekyll Themes -->

<!-- Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/maple-repair/expression-templates/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file. -->

<!-- ### Support or Contact -->

<!-- Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out. -->
