---
title: Digital Humanities
layout: page
lang: en
ref: dh
---

# Digital Humanities Curriculum
Inspired by a project by David Venturi which aimed at creating [his own Data Science Curriculum](http://davidventuri.com/data-science-masters/) using only courses and resources available online, I decided to do something similar, but instead of focussing on Data Science, my goal is to get a better grasp of the field of Digital Humanities.

## Why?
I took this decision because of an experience I made during my ›traditional‹ course of studies. I got in contact with the Digital Humanities a few times in this time, but never in a way that allowed for a deep and thorough understanding. For this reason, I remained fascinated but at the same time rather ignorant of the methodologies and concepts utilised by the practitioners of the discipline. I didn't even come close to what one could call _code literacy_ (Cf. [Rieder und Röhle 2012](https://doi.org/10.1057/9780230371934_4), p. 76): a critical understanding of the techniques and methods used in the Digital Humanities, a critical understanding of what coding means in the humanities.

At the same time, I noticed in discussions with ›traditionally‹ oriented classmates that there is some sort of discontent when it comes to the Digital Humanities. This discontent was of a rather vague nature, but for most it just didn't seem necessary to bring informatics into the mix, to change learned ways of tackling problems. Evidently, books and papers written by academics in the Digital Humanities are oftentimes irritating to read when approached by a more ›traditional‹ scholar. Not only is the way of writing significantly different, the form and structure of arguments also seem to differ substantially. The most obvious marker of this is the use of numerical data and graphic representations (Cf. topic of relative incommensurability [Ramsay 2003](https://doi.org/10.1093/llc/18.2.167)).

## The dream of a transdisciplinary method in the humanities
Oftentimes the hope that gets placed in the Digital Humanities is the prospect of a stronger trans- and interdisciplinary communication within the humanities without homogenising their disciplinary diversity. This hope is not without its reasons: The use of digital methods is not restricted to one use case or discipline and it is already discernible at this point that the Digital Humanities have the potential to transgress boundaries within the humanities conceptually as well as systematically (Cf. [Meister 2012](https://www.jstor.org/stable/41636598), p. 84). If, on the other hand, the reformulation of humanist problems into abstract code will result in the rise of a new _lingua franca_ that has to be spoken by every scholar in the humanities in the future as Meister seems to propose (Cf. ibid, p. 83), remains to be seen.

In my opinion, it would be misguided to demand all kinds of humanities research to conform to an informatics rule set. Such a development would be detrimental considering the productive specialisations of the individual disciplines which have their own histories. Convergence on the basis of digital methods, however, seems possible. The perspectives and possibilities in the area of Digital Humanities are still in their infant state which means that experimentation about what works and what doesn't is still important.

## Developments and positions in the Digital Humanities
Since I started studying in 2012 the professionalisation (and ›[professoralisation](https://dhd-blog.org/?p=6174)‹) of the Digital Humanities has steadily increased. In 2013 the organisation [Digital Humanities im deutschsprachigen Raum](https://dig-hum.de/ueber-dhd) was established and it seems like there is a new Bachelor or Master course in Digital Humanities established each year. Still the main question about what defines or should define Digital Humanities remains at the centre of many disciplinary discussions. For this reason, the following paragraphs point out some of the more prominent positions and definitions.

Franco Moretti is considered to be one of the most important emissaries of the discipline. Ten years before he established the [Stanford Literary Lab](https://litlab.stanford.edu/) in 2010, he had coined the term _Distant Reading_ which he used almost like a battle cry against ›traditional‹ literature criticism. Moretti defines _Distant Reading_ as the »focus on units that are much smaller or much larger than the text: devices, themes, tropes — or genres and systems« ([Moretti 2000](https://newleftreview.org/II/1/franco-moretti-conjectures-on-world-literature), p. 57) which is why, he argued, these units could only be adequately captured and described using large amounts of text. His plea to literary criticism was a polemical one: "[W]e know how to read texts, now let’s learn how _not_ to read them." (Ibid.).

During the almost two decades since this plea, a form of consolidation took place, leading to a more grounded tone of the discussion. The Digital Humanities have arrived in the academic mainstream. This is also perceptible in the broad definition of the discipline by [Jannidis et. al (2017)](https://doi.org/10.1007/978-3-476-05446-3). The authors describe the field as the »the sum of all attempts to utilise informatics in the context of humanities research« (p. 13). A figure that depicts this intersection can be found in Patrick Sahle's Paper _[DH Studieren! Auf dem Weg zu einem Kern- und Referenzcurriculum (2013)](http://cceh.uni-koeln.de/files/DARIAH-M2-3-3_DH-programs_1_2_0.pdf)_:

![Figure 1]({{site.url}}{{site.baseurl}}/assets/images/abb1.png)
Sahle (2013), p. 27.
{: style="color:gray; font-size: 80%; text-align: center;"}

One can, therefore, differentiate at least four different main areas of the Digital Humanities at this point (Cf. Jannidis et. al. 2017, p. 13):
1. Natural language processing, e.g. Text Mining, Topic Modeling, Stylometry, Corpus Linguistics.
2. Computer-assisted analysis of non-textual media like images, music and film.
3. Digital processing of source material for databases and other use cases.
4. Humanities research into new technologies, e.g. the question of the extent to which modern media change our society.

## Approach and Goals
I'm particularly interested in the first and the last point of this list. The curriculum, however, focusses on learning skills related to the first point, it is supposed to facilitate basic knowledge in Python supplemented by a knowledge of basic concepts and methods of corpus linguistics, the areas of Natural Language Processing (NLP) and Machine Learning. The courses are offered by different universities as well as platforms, partly leading to redundancies which are, in my opinion, helpful on a didactic level. I will document my progress in the blog and also try to find and present further helpful resources. The bars indicate how far I have progressed in the respective course.

The courses used can each be understood as an introduction to the relevant subject area, be it in dealing with Python or with regard to special applications of digital methods for dealing with large amounts of text/data. My aim is not to acquire full informatics knowledge, but instead to enable myself to independently design and apply digital methods for checking and answering own research questions, as well as the ability to critically evaluate those very techniques and methods.

<div class="breaker"></div>

<h1 text-align="center">Introduction</h1>
<div class="side-by-side">
    <div class="toright">
        <img class="image" src="{{ site.url }}{{ "/assets/images/oopcourse.png" }}" alt="Programming Foundations with Python">
    </div>
    <div class="toright">
    	<a href="https://eu.udacity.com/course/programming-foundations-with-python--ud036">Programming Foundations with Python</a>
        <p class="programming">Introduction to object-oriented programming with Python with basic units for the structure and modules of the standard library as well as for the concept and application of functions and classes. Various projects for application-oriented learning of algorithmic problem solving.</p>
		<progress value="100" max="100">Abgeschlossen</progress>
		<figcaption class="caption">Abgeschlossen</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://bertelsmann-university.com/fileadmin/_processed_/0/1/csm_Bertelsmann-Data-Science-Scholarship-Badge_7f392548dc.png" alt="Bertelsmann Data Science Challenge">
    </div>
    <div class="toright">
    	<a href="https://www.udacity.com/bertelsmann-data-scholarships">Bertelsmann Data Science Challenge Scholarship Course</a>
        <p class="programming">Three-month <i>Challenge Course</i> in which the basics of data science were taught. Basic concepts from the areas of descriptive statistics, Python and SQL necessary for the description, research and visualization of given data.</p>
		<progress value="100" max="100">Done</progress>
		<figcaption class="caption">Done</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="http://www.cs50xhelpers.org/img/fb.png" alt="Harvard CS50">
    </div>
    <div class="toright">
        <a href="https://cs50.edx.org">Introduction to Computer Science (CS50)</a>
        <p class="programming">Introductory course in computer science. Introduction to the basics of algorithmic thinking and basic concepts of computer science (abstraction, data structures, software engineering and security, web development). Introduction to common programming languages like C, Python, SQL as well as HTML/CSS and Javascript.</p>
    	<progress value="2" max="11">Paused</progress>
    	<figcaption class="caption">Paused</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://online-learning.harvard.edu/sites/default/files/styles/header/public/course/HarvardX_DH_course_graphic_small%209.16.16%20AM-1.jpg" alt="Harvard DH101">
    </div>
    <div class="toright">
        <a href="https://online-learning.harvard.edu/course/introduction-digital-humanities">Introduction to Digital Humanities (DH101)</a>
        <p class="programming">Introductory course in the Digital Humanities. 
        Conveys the basics of research in the Digital Humanities by showing different projects as well as tools and how and why they were developed. Includes units on acquiring, cleaning, and creating data as well as using the command line and the tool <a href="https://voyant-tools.org/">Voyant</a>.</p>
    	<progress value="7" max="7">Done</progress>
    	<figcaption class="caption">Done</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://the-javascripting-english-major.org/v1/assets/images/logo-no-border.svg" height="75%" width="auto" alt="The Javascripting English Major">
    </div>
    <div class="toleft">
        <a href="https://the-javascripting-english-major.org/v1/contents">The JavaScripting English Major</a>
        <p class="programming">Application-oriented course in JavaScript for <i>English Majors</i> and other humanists from <a href="https://moacir.com/" >Moacir P. de Sá Pereira</a>. Especially helpful for the interactive mediation and presentation of theories and results in the humanities for the digital space.</p>
    	<progress value="15" max="15">In process</progress>
    	<figcaption class="caption">In process</figcaption>
    </div>
</div>

<!-- <div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://coursera-course-photos.s3.amazonaws.com/08/8c6610c07e11e6a7f5e70b413367a6/DMSIcon.jpg" alt="Data Science Math Skills">
    </div>
	<div class="toright">
		<h3><a href="https://www.coursera.org/learn/datasciencemathskills">Data Science Math Skills</a></h3>
        <p>Mathematische Vokabeln, Konzepte und Regeln für ein tieferes Verständnis der Data Science.</p><br />
		<progress value="0" max="100">Noch nicht begonnen</progress>
		<figcaption class="caption">Noch nicht begonnen</figcaption>
    </div>
</div> -->

---
<h1 text-align="center">Corpus linguistics</h1>
<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://s3.amazonaws.com/coursera-course-photos/52/9974b07ed211e7a70247c29493f328/MOOC_Sprachtechnologie-Digital-Humanities_Coursera-Header_1200x1200.jpg" alt="Sprachtechnologie in den Digital Humanities">
    </div>
    <div class="toright">
    	<a href="https://www.coursera.org/learn/digital-humanities">Sprachtechnologie in den Digital Humanities</a>
        <p class="programming">Basic terms and concepts of corpus linguistics: word frequencies, collocations, N-grams. In addition, learning units for manual and automatic corpus annotation (Named-entity recognition (NER), Part-of-Speech-Tagging (POS) and Lemmatization).</p>
    	<progress value="100" max="100">Done</progress>
    	<figcaption class="caption">Done</figcaption>
    </div>
</div>

<!--<h1 text-align="center">Social Network Analysis</h1>
<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://s3.amazonaws.com/coursera-course-photos/ec/50a9bcc99dfc058198c9d4827b11e7/Logo1.jpg" alt="Social and Economic Networks: Models and Analysis">
    </div>
    <div class="toright">
    	<a href="https://www.coursera.org/learn/social-economic-networks">Social and Economic Networks: Models and Analysis</a>
        <p>Modellierung von Netzwerken für die Visualisierung von Zusammenhängen in Gesellschaft und Ökonomie.</p><br />
    	<progress value="0" max="8">Noch nicht begonnen</progress>
    	<figcaption class="caption">Noch nicht begonnen</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://s3.amazonaws.com/coursera-course-photos/24/2ca1701e1511e6846dd70314906f93/python_datascience_thumbnail_social_1x1.png" alt="Social and Economic Networks: Models and Analysis">
    </div>
    <div class="toright">
    	<a href="https://www.coursera.org/learn/python-social-network-analysis">Applied Social Network Analysis in Python</a>
        <p>Einführung in die Netzwerkanalyse mit NetworkX.</p><br />
    	<progress value="0" max="4">Noch nicht begonnen</progress>
    	<figcaption class="caption">Noch nicht begonnen</figcaption>
    </div>
</div>
-->
---
<h1 text-align="center">Natural Language Processing (NLP)</h1>
<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://masters.vu.nl/Content/images/VULogoWithText.svg" alt="Python for Text Analysis">
    </div>
    <div class="toright">
    	<a href="https://github.com/cltl/python-for-text-analysis">Python for Text Analysis</a>
        <p class="programming">Introduction to the use of Python for text analysis by the Computational Lexicology and & Terminology Lab of the Vrije Universiteit Amsterdam. Supplemented by the workbook <i><a href="https://github.com/walshbr/textanalysiscoursebook">Introduction to Text Analysis</a></i> by Brandon Walsh and Sarah Horowitz.</p>
		<progress value="17" max="18">In progress</progress>
		<figcaption class="caption">In progress</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://d3njjcbhbojbot.cloudfront.net/api/utilities/v1/imageproxy/https://s3.amazonaws.com/coursera-course-photos/2d/3ee200533711e4815fe98a35e8e32a/Mining_Text_Data_2.jpg" alt="Text Mining and Analytics">
    </div>
    <div class="toright">
    	<a href="https://www.coursera.org/learn/text-mining">Text Mining and Analytics</a>
        <p class="programming">Techniques and methods for the extraction and analysis of text data (Natural Language Processing), including learning units on Topic Analysis, Text Clustering and Text Categorization.</p>
    	<progress value="0" max="6">Not yet started</progress>
    	<figcaption class="caption">Not yet started</figcaption>
    </div>
</div>

---
<h1 text-align="center">Machine Learning</h1>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://s3-us-west-2.amazonaws.com/udacity-email/pytorch-acceptance-badge.png" alt="PyTorch Scholarship Challenge">
    </div>
    <div class="toright">
    	<a href="https://www.udacity.com/facebook-pytorch-scholarship">PyTorch Scholarship Challenge</a>
        <p class="programming">Two-month <i>Challenge Course</i>, which teaches the basics of deep learning with the Python program library <a href="https://pytorch.org/">PyTorch</a>. Construction, training and application of machine learning algorithms.</p>
    	<progress value="25" max="100">Paused</progress>
    	<figcaption class="caption">Paused</figcaption>
    </div>
</div>

<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://prod-discovery.edx-cdn.org/media/course/image/17920e6b-e3ed-4819-8116-e48854e62cce-f78831c35d44.jpg" alt="Deep Learning with Python and PyTorch">
    </div>
    <div class="toright">
    	<a href="https://www.edx.org/course/deep-learning-with-python-and-pytorch">Deep Learning with Python and PyTorch</a>
        <p class="programming">In addition to Deep Learning with PyTorch, the course also includes units for the use of Numpy and Pandas for machine learning.</p>
		<progress value="0" max="6">Not yet started</progress>
		<figcaption class="caption">Not yet started</figcaption>
    </div>
</div>
