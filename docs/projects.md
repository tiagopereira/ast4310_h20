# Projects

## Overview

There are a total of six projects, to be handed in at different times and with a different weight on the final grade, as listed below.

|        | Deadline          | Weight  |  Topic  |
| ------------- |:-------------:| :----:|:---|
| [Project 1](https://github.com/tiagopereira/ast4310/tree/master/notebooks/project1)     | 04.09.2020 | Pass/fail | Basic spectral line formation |
| [Project 2](https://github.com/tiagopereira/ast4310/tree/master/notebooks/project2)    | 18.09.2020 | 10% | Line strengths and curve of growth |
| [Project 3](https://github.com/tiagopereira/ast4310/tree/master/notebooks/project3)     | 02.10.2020 | 15% | *La Palma* |
| [Project 4](https://github.com/tiagopereira/ast4310/tree/master/notebooks/project4)     | 23.10.2020 | 25% | Solar stratification and continua |
| [Project 5](https://github.com/tiagopereira/ast4310/tree/master/notebooks/project5)     | 13.11.2020 | 25% | LTE line formation |
| Project 6     | 11.12.2020 | 25% | *Different options:* |
| <ul><li><a href="https://github.com/tiagopereira/ast4310/tree/master/notebooks/project6a">Project 6a</a></li></ul>    | | | <ul><li>3D Radiative Transfer</li></ul>|
| <ul><li><a href="https://github.com/tiagopereira/ast4310/tree/master/notebooks/project6b">Project 6b</a></li></ul>   | | | <ul><li>Scattering</li></ul> |

For project 6 there will be a few different options to chose from (each person/group can only select one). Please check this page to see when new options have been added.


## Repository

The projects are given in Jupyter notebook format, and can be found at the [course's github repository](https://github.com/tiagopereira/ast4310). You can [download a zip file](https://github.com/tiagopereira/ast4310/archive/master.zip) of the repository from github, but the recommended way to get it is via git, so you can get updates more easily. In a directory of your choice, you can do:

```bash
$ git clone https://github.com/tiagopereira/ast4310.git
```

This will create a directory called `ast4310` in the current directory. If there are any updates, once inside the directory `as4310` you can do 
```bash
$ git pull
```

This will update your files to match the latest versions. In some cases, if you have made changes to the project files, you may get an error or a conflict. In these cases, it is generally best to do a `git reset` and then a `git pull`. 

!!! danger
    Doing a `git reset` is generally safe, but it brings back the repository version of the files. If you made any changes to e.g. the notebook files, they will be lost. To avoid this, *you should not change the notebook files* (ie, files with the questions). Instead, either make a copy or start your edits on a different file. 

In the `notebooks` directory there are sub-directories for the different projects. They contain two notebooks: a Python version and a Julia version. In addition, they also contain auxiliary files needed for the computations and images for illustrations. Some projects require the download of large files; those are not included, but should be linked in the notebooks. 

To see the projects, you should open the notebook files with Jupyter lab. In some cases the LaTeX parts in Markdown may not render. You can try waiting a bit, or re-running (Ctrl+Enter) the problematic markdown cells. In some cases, making a small change (e.g. adding a space) and re-running the cell fixes the problem.

## Format and delivery

The projects should be handed in as Jupyter notebooks (Python or Julia). Please have a look at the [Guidelines notebook](https://github.com/tiagopereira/ast4310/blob/master/notebooks/Guidelines.ipynb) (under `ast4310/notebooks`) for more details on what is expected in the notebooks. There is also a [Template notebook](https://github.com/tiagopereira/ast4310/blob/master/notebooks/template.ipynb) that you can copy and use as a starting point for your assignments. The project deliveries will be assessed anonymously, but please remember to include your candidate numbers in the notebook submitted.

The assignments will be handed using [Devilry](https://devilry.ifi.uio.no).  The projects can be handed in individually or in groups of two. It is strongly recommended that students get together in groups for the projects. For Projects 3 and 5, groups will be mandatory and will be assigned. For all other projects, students are free to choose their groups. 

!!! info
    Groups are not enabled in Devilry. This means that students in a group will need to submit the same files on Devilry. The reason for this is that given the chances to improve the grade via the optional peer review (see below), group members will not necessarily have the same final grade for a project.

In addition to the notebook file, you should upload also all necessary files to run or notebook, or additional files you created along your notebook (e.g. a data file with the results of a long calculation). *You do not need to upload the additional files that were present in the repository* (e.g. atom files, images, etc.). Loading data files or code from the internet is not allowed.

## Grading

Project 1 will be pass/fail and have no effect on your final grade (assuming you pass!). The other projects will have weights of 10%, 15%, 25%, 25%, and 25% (see table above). Each project will have a numerical grade between 0 and 100, and the final grade is the weighed sum of all project grades. The final numerical grade will be converted to the A-F scale according to the usual scale:

| Points | Grade |
|:-------:|:-----|
| 92 - 100 |  A |
| 77 - 91 |  B |
| 58 - 76  | C |
| 46 - 57 |  D |
| 40 - 45 |  E |
| 0 - 39 |  F |

The grade of each project can be improved in two ways: by peer review (**5% extra**), or by submitting an improved version (**up to 30% of points not earned**), see below for details. The improved grade cannot be more than 100 points.

### Peer review

To mimic the peer-review process in scientific publications, you will have the opportunity to review the work of your colleagues. The main goal of peer review is to give constructive feedback so that your colleagues can learn from their mistakes and improve the submission. As a bonus for this extra effort, you will receive an extra 5% on your project grade. Peer review will be double-blind and individual. Each element of a group will be given a different assignment to review. If only one person in the group sends a review report, only that person gets the extra 5%. The bonus will be awarded regardless of the quality of the review report, although submissions that are obviously low quality will receive no bonus. Examples of a low-quality review are:

* Few comments on the work
* Meaningless or off-the-mark comments, where it is obvious the reviewer did not properly read the work
* Contains offensive or inappropriate comments

#### Peer review for the *reviewer*

* After the projects are handed in in Devilry, we will work quickly to assign you a project to review. A Jupyter notebook will be sent to you. You should write your review in that notebook, by adding additional markdown cells, enclosing your comments with an HTML box of the following kind:

```html
<div style="background-color:#e6e6e6; padding:10px; border-style:
solid;; border-color:#0d0d0d; border-width:1px">

Your markdown comments here.

* Can also use
* a bulleted list,

Other markdown, LaTeX: $\epsilon$, etc.

</div>
```

* There is a deadline of one week to submit the peer review, counting from the original submission deadline.
* Your job as a reviewer is to find out if each question is adequately answered, for example by answering the following questions:
    * Are the assumptions correct, and well spelled out?
    * Are the computations adequate to the job, and the code easy to read?
    * Are there any major flaws in the answer(s)?
    * Is the text well-written and concise?
    * Are plots well laid out?
* You don't need to answer all of the above, or go exhaustively through the calculations or the code. The point is more to look at the big picture.
* It is not the job of the reviewer to spell check or correct the language (in scientific publications, this is the job of the editor and/or language editor). If you find there are too many language errors, you can mention it as a general comment, e.g.: *This work would benefit from some proofreading, there are several typos and grammatical errors.*
* It is not the job of the reviewer to force her/his view into the writing of the answers, but provide a neutral viewpoint. 
* Do not be afraid to point out mistakes if you find them, but always try to do so in a constructive manner and criticise the work, not the person. Write your feedback as you would like to receive it.
* Avoid discussing your peer review assignments with your colleagues. 
* The only exception of the above is sharing with your group colleague if you happen to find an answer that is markedly better than your own. This is also a learning experience for you, and in such cases you are encouraged to use what you've learned from other projects when submitting a revised version (see below).
* If you are using parts of someone else's project in your revised submission, **always give credit**. E.g. *we changed X and Y based on an approach learned from another project we reviewed*. In these cases, try to modify your own answer as opposed to copying someone else's answer or source code. **Wholesale copying of other answers will be considered cheating.**




#### Peer review for the *authors*

* About one week after the original submission deadline, you will receive feedback from the teachers plus any feedback from peer review
* Comments you receive from peer review will not affect your grade, only the assessment by the teachers.
* Do not take the comments from peer review at face value. It is possible that the reviewer is wrong.
* Do not take any negative comments personally. The reviewer is commenting on the work that you submitted, not on you as a person.
* Avoid discussing the comments from peer review outside your group, and especially do not confront other students or suggest she/he was the referee.


### Submitting an improved version

Another way to get bonus point is to submit an improved version of your project. You will be able to get 30% of the points you did not get in the first submission. For example, assume you got 50 in your first submission. This means that you can gain up to 30% of 50 points, or 15 points. If you got 80 points initially, you can get up to 6 points more, and so on.

Submitting an improved version is optional. The goal is not to work towards a perfect delivery, but to make you reflect on your answers and learn from any shortcomings. You should consider the feedback you got from the teachers and from the peer review when working on a revised version. Trivial resubmissions with little improvement will not get bonus points. The bonus points will be awarded if there is improvement, even if the revised answer is not 100% correct. How much improvement is enough? That will be decided on a case-by-case basis. But the bar will not be set very high. 

Bonus points from submitting an improved version will be added to both group members. As in the original submission, both will be asked to submit the new version on Devilry.
