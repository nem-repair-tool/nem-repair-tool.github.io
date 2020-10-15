<!-- You can use the [editor on -->
<!-- GitHub](https://github.com/maple-repair/expression-templates/edit/master/index.md) to maintain and preview the content for your website in Markdown files. -->

<!-- # Automated Program Repair using Formal Specifications. -->

## Abstract
We propose a novel method to automatically repairing buggy heap-manipulating
programs using constraint solving and deductive synthesis.
Given an input program C and its formal specification in the form of a Hoare
triple: {P} C {Q}, we use a separation-logic-based verifier to
verify if program C is correct w.r.t. its specifications.
If program C is found buggy, we then repair it in the following steps.
First, we rely on the verification results to collect a list of suspicious
statements of the buggy program.
For each suspicious statement, we temporarily replace it with a template patch
representing the desired statements.
The template patch is also formally specified using a pair of unknown pre- and
postcondition.
Next, we use the verifier to analyze the temporarily
patched program to collect constraints related to the pre- and postcondition of
the template patch.
Then, these constraints are solved by our constraint solving technique
to discover the suitable specifications of the template patch.
Subsequently, these specifications can be used to synthesize
program statements of the template patch, consequently creating a candidate
program.
Finally, if the candidate program is validated, it is returned as the repaired
program.
We demonstrate the effectiveness of our approach by evaluating our implementation
and a state-of-the-art approach on a benchmark of 231 buggy programs.
The experiment results show that our tool successfully repairs 223 buggy
programs and considerably outperforms the compared tool.

## NEM
NEM is build on top of the [HIP](http://loris-5.d2.comp.nus.edu.sg/hip/index.html)
verification system and [Songbird](https://songbird-prover.github.io/) prover. 

## Compared Tool
- [Enhancing Automated Program Repair with Deductive Verification](https://dblp.org/db/conf/icsm/icsme2016.html#LeLLG16)

## The Benchmarks and Experiments.

- The details about the benchmark we use in our experiments is provided
in [Github](https://github.com/nem-repair-tool/heap-repair).

+ README provides information about our virtual machine.
+ Folder "benchmark" contains correct programs
+ Folder "evaluated" contains buggy versions of each program in corresponding folder

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
