##Fuzzing

TOC

* [Videos/Presentations](#presentation)
* [Techniques](#tech)
* [Methodologies](#method)
* [Write-ups](#writeup)
* [Tools](#tools)
* [Papers](#papers)
* [Books](#books)
* [Miscellaneous](#misc)


[Quick explanation of fuzzing and various fuzzers](http://whoisjoe.info/?p=16)

###Cull


[Advice From A Researcher: Hunting XXE For Fun and Profit](https://blog.bugcrowd.com/advice-from-a-researcher-xxe/)
File Format Fuzzing in Android
https://deepsec.net/docs/Slides/2015/File_Format_Fuzzing_in_Android_-Alexandru_Blanda.pdf

| **honggfuzz** - A general-purpose, easy-to-use fuzzer with interesting analysis options. Supports feedback-driven fuzzing based on code coverage | https://github.com/google/honggfuzz
| **USB Fuzzing Basics: From fuzzing to bug reporting** | http://blog.quarkslab.com/usb-fuzzing-basics-from-fuzzing-to-bug-reporting.html









Fuzzing Object s d�ART Digging Into the New Android L Runtime Internals
http://census-labs.com/media/Fuzzing_Objects_d_ART_hitbsecconf2015ams_WP.pdf

MFFA - Media Fuzzing Framework for Android
https://github.com/fuzzing/MFFA


How to fuzz a server with American Fuzzy Lop
https://www.fastly.com/blog/how-fuzz-server-american-fuzzy-lop



http://nullcon.net/website/archives/ppt/goa-15/analyzing-chrome-crash-reports-at-scale-by-abhishek-arya.pdf



libFuzzer � library for in-process evolutionary fuzzing of other libraries.
http://llvm.org/docs/LibFuzzer.html

[Unusual bugs - 23C3](https://www.youtube.com/watch?v=qj79Qdmw0Pk) * In this presentation I'll present a series of unusual security bugs. Things that I've ran into at some point and went "There's gotta be some security consequence here". None of these are really a secret, and most of them are even documented somewhere. But apparently most people don't seem to know about them.  What you'll see in this presentation is a list of bugs and then some explanation of how these could be exploited somehow. Some of the things I'll be talking about are (recursive) stack overflow, NULL pointer dereferences, regular expressions and more. 

[From Fuzzing to 0day.](http://blog.techorganic.com/2014/05/14/from-fuzzing-to-0-day/)

###<a name="presentation">Presentations/Videos</a>

[The Best of Bug Finding - Duo Tech Talk (Charlie Miller)](https://www.youtube.com/watch?v=1M1EOzulQsw)
* I look at how security vulnerabilities are found (or missed) and some of my favorite bugs and exploits I�ve come across in my career. 

[Implementing an USB Host Driver Fuzzer - Daniel Mende - Troopers14](https://www.youtube.com/watch?v=h777lF6xjs4)

[The Power Of Pair: One Template That Reveals 100+ Uaf Ie Vulnerabilities - BlackhatEU14](http://www.securitytube.net/video/12924?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+SecurityTube+%28SecurityTube.Net%29)

[What Happens In Windows 7 Stays In Windows 7 - Marion Marschalek & Joseph Moti - Troopers14](https://www.youtube.com/watch?v=s_7Cy2w2dCw)
* Diffing libs in Win7 compared to Win8 to id vuln dlls.
* [DiffRay](https://github.com/pinkflawd/DiffRay)
..* Tool for diffing Win7 & Win8 Libraries based on textfile outputs from IDA Pro.

[Mining for Bugs with Graph Database Queries [31c3]](https://www.youtube.com/watch?v=291hpUE5-3g)
* [Starting out with Joern](http://tsyrklevich.net/2015/03/28/starting-out-with-joern/)




###General Writeups
[Fuzzing for MS15-010](http://blog.beyondtrust.com/fuzzing-for-ms15-010)
* Is what it says on the tin.




###<a name="tech">Techniques</a>



####Taint Analysis





###<a name="writeup">Writeups</a>

[Taint analysis and pattern matching with Pin - Jonathan Salwan](http://shell-storm.org/blog/Taint-analysis-and-pattern-matching-with-Pin/)

[Faster Fuzzing with Python](https://labs.mwrinfosecurity.com/blog/2014/12/10/faster-fuzzing-with-python/)

[Walkthrough of setting up CERT�s FOE fuzzer and fuzzing irfanview](http://www.singlehop.com/blog/lets-fuzz-irfanview/)


###<a name="papers">Papers</a>

[Smart COM Fuzzing - Auditing IE Sandbox Bypass in COM Objects� Xiaoning Li � Haifei Li](https://0b3dcaf9-a-62cb3a1a-s-sites.googlegroups.com/site/zerodayresearch/Smart_COM_Fuzzing_Auditing_IE_Sandbox_Bypass_in_COM_Objects_final.pdf?attachauth=ANoY7crUl9OP1JfFa6KaCXsjVLjsNXDgUp1SmrZZAgGiPdp7MvUVnfg-FsuFvt7lfV5s3-kcK3K2uT05XMt6zUU_cP5WWQKxmKedjlQjvTZWdLyVZVcUMUrxUr5i68jpISP84HE0hihXOz7GtyWQG4gOtf-PXmcxmBf9KjYpVob08uR-62u2swlo396pKC0mSRrymia5PAakBFV9_0TbXGEhNVc101GIRdZ33C-j8DI6bIEYVlR1vG9jUKkfIcleu-rtjnJyDXD9FFBJwqxZsVOAUb9mcPvc4SZ04uefDvQwCDEg-C4I8eA%3D&attredirects=0)

[Applying Taint Analysis and Theorem Proving to Exploit Development - Sean Heelan - RECON2010](http://static1.squarespace.com/static/507c09ede4b0954f51d59c75/t/508eb764e4b047ba54db4999/1351530340153/applying_taint_analysis_and_theorem_proving_to_xdev.pdf)

[All You Ever Wanted to Know About Dynamic Taint Analysis and Forward Symbolic Execution (but might have been afraid to ask)](http://users.ece.cmu.edu/~ejschwar/papers/oakland10.pdf)
* Abstract �Dynamic taint analysis and forward symbolic execution are quickly becoming staple techniques in security analyses. Example applications of dynamic taint analysis and forward symbolic execution include malware analysis, input filter generation, test case generation, and vulnerability dis- covery. Despite the widespread usage of these two techniques, there has been little effort to formally define the algorithms and summarize the critical issues that arise when these techniques are used in typical security contexts. The contributions of this paper are two-fold. First, we precisely describe the algorithms for dynamic taint analysis and forward symbolic execution as extensions to the run-time se- mantics of a general language. Second, we highlight important implementation choices, common pitfalls, and considerations when using these techniques in a security context.

[A Critical Review of Dynamic Taint Analysis and Forward Symbolic Execution](https://asankhaya.github.io/pdf/ACriticalReviewofDynamicTaintAnalysisandForwardSymbolicExecution.pdf)
* In this note , we describe a critical review of the paper titled �All you wanted to know about dynamics taint analysis and forward symbolic execution (but may have been afraid to ask)� [1] . We analyze the paper using Paul Elder critical thinking framework [2] . We sta rt with a summary of the paper and motivation behind the research work described in [1]. Then we evaluate the study with respect to the universal intellectual standards of [2]. We find that the paper provides a good survey of the existing techniques and algorithms used for security analysis. It explains them using the theoretical framework of operational runtime semantics. However in some places t he paper can do a better job in highlighting what new insights or heuristics can be gained from a runtime seman tics formulation. The paper fails to convince the reader how such an intricate understanding of operational semantics of a new generic language SimpIL helps in advancing the state of the art in dynamic taint analysis and forward symbolic execution. We also found that the Paul Elder critical thinking framework is a useful technique to reason about and analyze research papers.

[Effective Bug Discovery](http://uninformed.org/?v=all&a=27&t=sumry)
* Sophisticated methods are currently being developed and implemented for mitigating the risk of exploitable bugs. The process of researching and discovering vulnerabilities in modern code will require changes to accommodate the shift in vulnerability mitigations. Code coverage analysis implemented in conjunction with fuzz testing reveals faults within a binary file that would have otherwise remained undiscovered by either method alone. This paper suggests a research method for more effective runtime binary analysis using the aforementioned strategy. This study presents empirical evidence that despite the fact that bug detection will become increasingly difficult in the future, analysis techniques have an opportunity to evolve intelligently. 

[TAJ: Effective Taint Analysis of Web Applications - Java Webapps](http://manu.sridharan.net/files/pldi153-tripp.pdf)
* Taint analysis, a form of information-flow analysis, establishes whether values from untrusted methods and parameters may flow into security-sensitive operations. Taint analysis can detect many common vulnerabilities in Web applications, and so has attracted much attention from both the research community and industry. However, most static taint-analysis tools do not address criti- cal requirements for an industrial-strength tool. Specifically, an industrial-strength tool must scale to large industrial Web applica- tions, model essential Web-application code artifacts, and generate consumable reports for a wide range of attack vectors. We have designed and implemented a static Taint Analysis for Java (TAJ) that meets the requirements of industry-level applica- tions. TAJ can analyze applications of virtually any size, as it em- ploys a set of techniques designed to produce useful answers given limited time and space. TAJ addresses a wide variety of attack vec- tors, with techniques to handle reflective calls, flow through con- tainers, nested taint, and issues in generating useful reports. This paper provides a description of the algorithms comprising TAJ, evaluates TAJ against production-level benchmarks, and compares it with alternative solutions.

###<a name="books">Books</a>

[*THE* Book on fuzzing](http://fuzzing.org/)



###<a name="tools">Tools</a>


[American Fuzzy Lop AFL](http://lcamtuf.coredump.cx/afl/)
* American fuzzy lop is a security-oriented fuzzer that employs a novel type of compile-time instrumentation and genetic algorithms to automatically discover clean, interesting test cases that trigger new internal states in the targeted binary. This substantially improves the functional coverage for the fuzzed code. The compact synthesized corpora produced by the tool are also useful for seeding other, more labor- or resource-intensive testing regimes down the road. 
* It was made by lcamtuf. What more do you need?

[afl-dyninst ; AFL Fuzzing blackbox binaries](https://github.com/vrtadmin/moflow/tree/master/afl-dyninst)
* American Fuzzy Lop + Dyninst == AFL Fuzzing blackbox binaries  The tool has two parts. The instrumentation tool and the instrumentation  library. Instrumentation library has an initialization callback and basic  block callback functions which are designed to emulate what AFL is doing with afl-gcc/afl-g++/afl-as.  Instrumentation tool (afl-dyninst) instruments the supplied binary by inserting callbacks for each basic block and an initialization  callback either at _init or at specified entry point.

[Grinder - Fuzzer](https://github.com/stephenfewer/grinder)
* Grinder is a system to automate the fuzzing of web browsers and the management of a large number of crashes. Grinder Nodes provide an automated way to fuzz a browser, and generate useful crash information (such as call stacks with symbol information as well as logging information which can be used to generate reproducible test cases at a later stage). A Grinder Server provides a central location to collate crashes and, through a web interface, allows multiple users to login and manage all the crashes being generated by all of the Grinder Nodes.


[crashwalk](https://github.com/bnagy/crashwalk)
* Bucket and triage on-disk crashes. OSX and Linux.(automated triaging of AFL-based crashes)

[CERT�s Failure Observation Engine (FOE)](https://www.cert.org/vulnerability-analysis/tools/foe.cfm)
* The CERT Failure Observation Engine (FOE) is a software testing tool that finds defects in applications that run on the Windows platform. FOE performs mutational fuzzing on software that consumes file input. (Mutational fuzzing is the act of taking well-formed input data and corrupting it in various ways looking for cases that cause crashes.) The FOE automatically collects test cases that cause software to crash in unique ways, as well as debugging information associated with the crashes. The goal of FOE is to minimize the effort required for software vendors and security researchers to efficiently discover and analyze security vulnerabilities found via fuzzing.

[Zulu Fuzzer](https://github.com/nccgroup/Zulu)
* The Zulu fuzzer
[Radamsa](https://code.google.com/p/ouspg/wiki/Radamsa)
* Radamsa is a test case generator for robustness testing, aka a fuzzer. It can be used to test how well a program can stand malformed and potentially malicious inputs. It operates based on given sample inputs and thus requires minimal effort to set up. The main selling points of radamsa are that it is easy to use, contains several old and new fuzzing algorithms, is easy to script from command line and has already been used to find a slew of bugs in programs that actually matter. 
[browserfuzz](https://bitbucket.org/blackaura/browserfuzz)
* A very simple browser fuzzer based on tornado.

[!exploitable Crash Analyzer](https://msecdbg.codeplex.com/)
* !exploitable (pronounced �bang exploitable�) is a Windows debugging extension (Windbg) that provides automated crash analysis and security risk assessment. The tool first creates hashes to determine the uniqueness of a crash and then assigns an exploitability rating to the crash: Exploitable, Probably Exploitable, Probably Not Exploitable, or Unknown. There is more detailed information about the tool in the following .pptx file or at http://www.microsoft.com/security/msec. Additonally, see the blog post at http://blogs.technet.com/srd/archive/2009/04/08/the-history-of-the-exploitable-crash-analyzer.aspx, or watch the video at http://channel9.msdn.com/posts/PDCNews/Bang-Exploitable-Security-Analyzer/.

####Peach Fuzzer
* [Peach Documentation](http://old.peachfuzzer.com/Introduction.html)
* [Creating Custom Peach Fuzzer Publishers](http://blog.opensecurityresearch.com/2014/01/creating-custom-peach-fuzzer-publishers.html)
* [Creating Custom Peach Fuzzer Publishers](http://blog.opensecurityresearch.com/2014/01/creating-custom-peach-fuzzer-publishers.html)
* [Code](https://github.com/OpenSecurityResearch/CustomPeachPublisher

Fuzzing with Peach tutorial
* [Part 1](http://www.flinkd.org/2011/07/fuzzing-with-peach-part-1/)
* [Part 2](http://www.flinkd.org/2011/11/fuzzing-with-peach-part-2-fixups-2/)

* [Fuzzing Vulnserver with Peach 3](http://rockfishsec.blogspot.com/2014/01/fuzzing-vulnserver-with-peach-3.html)




###<a name="misc">Misc</a>

[Good slides on fuzzing](https://courses.cs.washington.edu/courses/cse484/14au/slides/Section8.pdf)

[USB Fuzzing Basics from fuzzing to Bug Reporting](http://blog.quarkslab.com/usb-fuzzing-basics-from-fuzzing-to-bug-reporting.html)




