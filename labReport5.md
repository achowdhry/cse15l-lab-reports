**Lab Report 5**
In this lab report, I will be looking forward to explore the functioning of different grep commands. In lab report 3, I saw the use of different find commands. I felt that I wanted to explore the grep commands as well.

* Option 1: -r: This option allows grep to search for a pattern recursively within directories and their subdirectories.

Example 1: Searching for a pattern within files in a directory.

```
grep -r "keyword" ./technical
```

Output:
```
[cs15lsp23nj@ieng6-202]:docsearch:47$ grep -r "keyword" ./technical
./technical/biomed/1471-2105-3-16.txt:        articles for keywords alluding to methods or techniques,
./technical/biomed/1471-2105-3-16.txt:            keywords/phrases that include the commonly used methods
./technical/biomed/1471-2105-3-16.txt:          significance of a specific keyword in determining the
./technical/biomed/1471-2164-3-9.txt:          ORFs was searched with the keyword "myosin" to identify
./technical/biomed/1471-2164-3-9.txt:          the keywords "myosin" (40 hits) and "coiled-coil" (0
./technical/biomed/1471-2180-2-29.txt:          (Release 129) by using keyword HCV or Hepatitis C. D90208
./technical/biomed/1471-2288-2-10.txt:        keyword 'cancer', and only 19 with the keyword COPD and 41
./technical/biomed/1471-2288-2-10.txt:        with the keyword 'epilepsy' among the 9,055 articles
./technical/biomed/1471-2326-2-4.txt:          keywords: thalassemia, serum ferritin, urinary iron
./technical/biomed/1471-2474-3-3.txt:        articles for this review. The keywords used for were strain
./technical/biomed/1472-6807-2-3.txt:            Ranking results by methods used (based on keywords
./technical/biomed/1472-6882-3-1.txt:        three times using general and specific keywords and
./technical/biomed/1472-6882-3-3.txt:        keywords among authors, indexers, and investigators [ 1 ] .
./technical/biomed/1472-6882-3-3.txt:        14 ] . Computer generation of keywords is referred to as
./technical/biomed/1472-6882-3-3.txt:        Plus. Author Keywords are taken from a list of keywords
./technical/biomed/1472-6882-3-3.txt:        the study title, abstract, or list of author keywords [ 17
./technical/biomed/1472-6882-3-3.txt:          descriptors, and potentially related keywords for these
./technical/biomed/1472-6882-3-3.txt:          Standard" as keyword and 
./technical/biomed/1472-6882-3-3.txt:          useful than analytic indexing because keyword indexing is
./technical/biomed/1472-6882-3-3.txt:          Science did not generate any keywords for 11/26 studies.

```

Example 2: Searching for a pattern within filenames.

```
grep -r -l "pattern" ./technical
```

Output:

```
[cs15lsp23nj@ieng6-202]:docsearch:61$ grep -r -l "pattern" ./technical
./technical/911report/chapter-1.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-8.txt
./technical/biomed/1468-6708-3-4.txt
./technical/biomed/1471-2091-2-10.txt
./technical/biomed/1471-2091-2-5.txt
./technical/biomed/1471-2091-2-7.txt
./technical/biomed/1471-2091-3-14.txt
./technical/biomed/1471-2091-3-15.txt
./technical/biomed/1471-2091-3-18.txt
./technical/biomed/1471-2091-3-22.txt
./technical/biomed/1471-2091-3-30.txt
./technical/biomed/1471-2091-3-31.txt
./technical/biomed/1471-2091-4-5.txt
./technical/biomed/1471-2105-1-1.txt
./technical/biomed/1471-2105-2-8.txt
./technical/biomed/1471-2105-2-9.txt
./technical/biomed/1471-2105-3-18.txt
```
Sources Used:
```
https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix
```
* Option 2: -i: This option allows grep to perform case-insensitive matching, ignoring the distinction between uppercase and lowercase letters.

Example 1: Searching for the word "GPT" in all files within a directory:

```
grep -ri "GPT" ./technical/
```

Output:

```
[cs15lsp23nj@ieng6-202]:docsearch:79$ grep -ri "GPT" ./technical/
./technical/biomed/1471-2202-3-7.txt:        (<TgPT-0> and <TcPT-1>, respectively). In 288
./technical/biomed/1471-2202-3-7.txt:        35 unique insertions (17 <TgPT-0> and 18
./technical/biomed/1471-2202-3-7.txt:        transposon. The improved transposons, <TgPT-0> 
./technical/biomed/1471-2202-3-7.txt:        and <TgPT-0>/<TcPT-1> transposed clones by


```

Example 2: Searching for the word "distract" in all files within the ./technical directory, displaying line numbers:

```
grep -rin "distract" ./technical/*
```

Output:

```
[cs15lsp23nj@ieng6-202]:docsearch:109$ grep -rin "distract" ./technical/*
./technical/911report/chapter-11.txt:298:                put aside in the early planning of the exercise as too much of a distraction from
./technical/911report/chapter-13.4.txt:1445:                the projects as a "distraction" that would pull personnel and resources away from
./technical/911report/chapter-3.txt:1982:                war to distract public attention from a domestic scandal. Some Republicans in
./technical/biomed/1471-2148-2-15.txt:15:        new and improved strategies has sometimes distracted from
./technical/biomed/1471-2288-3-9.txt:44:        error has distracted researchers from the many other, often
./technical/biomed/1471-2415-3-4.txt:362:        irradiation [ 24 ] or the distraction of the epithelial
./technical/biomed/1471-244X-2-9.txt:65:        and distractability, and for some, greater success with
./technical/biomed/1471-244X-2-9.txt:440:        get so distracted.")
./technical/biomed/1471-2474-3-23.txt:329:          Stability in extension depends most on the distraction of
./technical/biomed/1472-6815-2-3.txt:65:        / distraction counseling program. Scott et al [ 14 ] had
./technical/biomed/1472-6815-2-3.txt:377:          or distraction from tinnitus . This is a vital
./technical/biomed/gb-2003-4-8-r51.txt:127:        distraction. To another, they might, in connection with
./technical/government/Alcohol_Problems/Session2-PDF.txt:93:been demonstrated in the presence of some of these distracting
./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt:5949:confuse or distract the users. Also, needless repetition should be
./technical/government/Media/Firm_to_the_Poor_Needs_Help.txt:35:distraction over the merger of LSEO with Legal Aid Services of
./technical/plos/journal.pbio.0020267.txt:225:        distracted.” Geschwind, Amaral, and other top experts have recently been recruited by
./technical/plos/journal.pbio.0020310.txt:41:        Conservation by Distraction
./technical/plos/journal.pbio.0020310.txt:45:        example of this ‘conservation by distraction’ is ploughing money into community-based

```

Sources Used:
```
https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix
```

* Option 3: -n: This option allows grep to print the line numbers along with the matching lines.



Example 1: Searching for the word "network" in all files within a directory, displaying line numbers:

```
grep -rn "network" ./technical/
```

Output:

```
[cs15lsp23nj@ieng6-202]:docsearch:95$ grep -rn "network" ./technical/
./technical/911report/chapter-10.txt:311:                terrorists, work with a coalition to eliminate terrorist groups and networks, and
./technical/911report/chapter-10.txt:393:            The United States would strive to eliminate all terrorist networks, dry up their
./technical/911report/chapter-10.txt:535:                our many Arab friends. Our enemy is a radicalnetwork of terrorists, and every
./technical/911report/chapter-11.txt:99:                They operate "outside traditional circles but have access to a worldwide network of
./technical/911report/chapter-11.txt:121:                global network, analysis of information from terrorists captured in Jordan in
./technical/911report/chapter-11.txt:192:                network was a nuisance that killed a score of Americans every 18-24 months. If that
./technical/911report/chapter-11.txt:787:                network television news. Though the Jordanian arrests only made page 13 of the New
./technical/911report/chapter-12.txt:49:                Qaeda network, its affiliates, and its ideology.
./technical/911report/chapter-12.txt:81:                network of terrorists that struck us on 9/11; and a radical ideological movement in
./technical/911report/chapter-12.txt:86:                our strategy must match our means to two ends: dismantling the al Qaeda network and
./technical/911report/chapter-12.txt:189:                a logistics network able to securely manage the travel of operatives, move
./technical/911report/chapter-12.txt:200:                them in isolated, desert camps. It built up logistical networks, running through
./technical/911report/chapter-12.txt:808:                successful, Pakistan's illicit trade and the nuclear smuggling networks of Pakistani
./technical/911report/chapter-12.txt:870:                    networks, search them out, and disrupt their operations. Intelligence and law
./technical/911report/chapter-12.txt:899:                terrorists need a financial support network-may become outdated. Moreover, some
./technical/911report/chapter-12.txt:944:                government officials, human smuggling networks, supportive travel agencies, and
./technical/911report/chapter-12.txt:1072:                    into a larger network of screening points that includes our transportation
./technical/911report/chapter-13.1.txt:31:                    knowledge in a network-based information-sharing system that transcends
./technical/911report/chapter-13.1.txt:685:                access granted or denied according to the rules set for the network-and with queries
./technical/911report/chapter-13.1.txt:687:                questions may not come at all unless experts at the "edge" of the network can
./technical/911report/chapter-13.1.txt:690:            We propose that information be shared horizontally, across new networks that
./technical/911report/chapter-13.1.txt:696:                A decentralized network model, the concept behind much of the information
./technical/911report/chapter-13.1.txt:699:                    system, secrets are protected through the design of the network and an
./technical/911report/chapter-13.1.txt:701:                    access to the whole network. An outstanding conceptual framework for this kind
./technical/911report/chapter-13.1.txt:702:                    of "trusted information network" has been developed by a task force of leading
./technical/911report/chapter-13.1.txt:712:                    technical issues across agencies to create a "trusted information network."
./technical/911report/chapter-13.1.txt:738:                that, ultimately, the network will be effective in protecting our security." The
./technical/911report/chapter-13.1.txt:920:                    facility; an existing network of informants, cooperating defendants, and other
./technical/911report/chapter-13.1.txt:1032:                United States, a community comprised mainly of state and local agencies. The network

```

Example 2: Searching for the word "algorithm" in all files within the ./technical directory, displaying line numbers:
```
grep -rin "algorithm" ./technical/*
```

Output:

```
[cs15lsp23nj@ieng6-202]:docsearch:38$ grep -rin "algorithm" ./technical/*
./technical/911report/chapter-12.txt:1030:                called algorithms, are just beginning to be used. Travel history, however, is still
./technical/911report/chapter-13.2.txt:94:                in addition to those flagged by the CAPPS algorithm, American's ticket agents were
./technical/911report/chapter-13.3.txt:789:                algorithm, a number of other passengers were selected at random, both to address
./technical/911report/chapter-13.3.txt:791:                algorithm and gaming the system. On no-fly lists, see FAA security directive,
./technical/911report/chapter-3.txt:570:                FAA-approved computerized algorithm (known as CAPPS, for Computer Assisted Passenger
./technical/911report/chapter-3.txt:572:                might pose more than a minimal risk to aircraft. Although the algorithm included
./technical/biomed/1471-2091-2-16.txt:288:          algorithm (MaxEnt) to transform the range of 650/1500 m/z
./technical/biomed/1471-2091-3-18.txt:464:        algorithm of SYBYL yielded 100 loops, of which only five
./technical/biomed/1471-2091-3-4.txt:122:          algorithm [ 38 ] was used to estimate secondary structure
./technical/biomed/1471-2105-2-1.txt:61:          "selection mapping" algorithm. The cornerstone of
./technical/biomed/1471-2105-2-1.txt:307:        We have developed an algorithm for using sequence data
./technical/biomed/1471-2105-2-1.txt:332:          QUASI--the selection mappingalgorithm
./technical/biomed/1471-2105-2-1.txt:366:          To overcome these limitations, the QUASI algorithm
./technical/biomed/1471-2105-2-1.txt:489:          The QUASI algorithm thus indicates at this exemplary
./technical/biomed/1471-2105-2-1.txt:524:          the goal, the QUASI algorith appears to have a practical
./technical/biomed/1471-2105-2-8.txt:11:        general genefinding algorithms. The number and diversity of
./technical/biomed/1471-2105-2-8.txt:19:        systematic RNA genefinding algorithm would be of use.
./technical/biomed/1471-2105-2-8.txt:42:        basis for a reliable ncRNA genefinding algorithm.
./technical/biomed/1471-2105-2-8.txt:94:        Algorithm
./technical/biomed/1471-2105-2-8.txt:279:          efficiently using an SCFG Inside algorithm (a dynamic
./technical/biomed/1471-2105-2-8.txt:280:          programming algorithm).
./technical/biomed/1471-2105-2-8.txt:621:            algorithm conventions from a single sequence to an
./technical/biomed/1471-2105-2-8.txt:709:            The full description of the algorithms associated to
./technical/biomed/1471-2105-2-8.txt:711:            algorithms requires two kind of emission
./technical/biomed/1471-2105-2-8.txt:756:          algorithm's discrimination ability on model generated
./technical/biomed/1471-2105-2-8.txt:771:          Alignment and scoring algorithms
./technical/biomed/1471-2105-2-8.txt:778:          Viterbi and/or Forward algorithms and SCFG CYK and/or
./technical/biomed/1471-2105-2-8.txt:779:          Inside algorithms. The OTH and COD pair-HMM alignment
./technical/biomed/1471-2105-2-8.txt:780:          algorithm would cost O( 
./technical/biomed/1471-2105-2-8.txt:782:          pair-SCFG algorithm would cost O( 
./technical/biomed/1471-2105-2-8.txt:786:          standard algorithms. Consider the RNA model. Recall that
./technical/biomed/1471-2105-2-8.txt:790:          algorithm rather than the CYK algorithm (which, like
./technical/biomed/1471-2105-2-8.txt:801:          the CYK (maximum likelihood parse) algorithm for the RNA
./technical/biomed/1471-2105-2-8.txt:803:          To combine the desired features of the two algorithms,

```

Sources Used:
```
https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix
```

* Option 4: -v: This option allows grep to display lines that do not match the given pattern.

Example 1: Searching for lines not containing the word "warning" in all files within a directory:

```
grep -rv "warning" ./technical/
```

Output:

```
[cs15lsp23nj@ieng6-202]:docsearch:99$ grep -rv "warning" ./technical/
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:	
./technical/911report/chapter-1.txt:		
./technical/911report/chapter-1.txt:"WE HAVE SOME PLANES"
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:INSIDE THE FOUR FLIGHTS
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:Boarding the Flights
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passenger Prescreening System), created to identify passengers who should be subject to special security measures. Under security rules in place at the time, the only consequence of Atta's selection by CAPPS was that his checked bags were held off the plane until it was confirmed that he had boarded the aircraft. This did not hinder Atta's plans.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    It would be their final conversation.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Between 6:45 and 7:40, Atta and Omari, along with Satam al Suqami, Wail al Shehri, and Waleed al Shehri, checked in and boarded American Airlines Flight 11, bound for Los Angeles. The flight was scheduled to depart at 7:45.

```

Example 2: Searching for lines that do not contain the word "openai" in all files within the ./technical directory:
```
grep -rvi "openai" ./technical/*
```
Output:
```
[cs15lsp23nj@ieng6-202]:docsearch:38$ grep -rvi "openai" ./technical/*
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:	
./technical/911report/chapter-1.txt:		
./technical/911report/chapter-1.txt:"WE HAVE SOME PLANES"
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    For those heading to an airport, weather conditions could not have been better for a safe and pleasant journey. Among the travelers were Mohamed Atta and Abdul Aziz al Omari, who arrived at the airport in Portland, Maine.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:INSIDE THE FOUR FLIGHTS
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:Boarding the Flights
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    When he checked in for his flight to Boston, Atta was selected by a computerized prescreening system known as CAPPS (Computer Assisted Passenger Prescreening System), created to identify passengers who should be subject to special security measures. Under security rules in place at the time, the only consequence of Atta's selection by CAPPS was that his checked bags were held off the plane until it was confirmed that he had boarded the aircraft. This did not hinder Atta's plans.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.
./technical/911report/chapter-1.txt:
./technical/911report/chapter-1.txt:    It would be their final conversation.
./technical/911report/chapter-1.txt:

```

Sources Used:
```
https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix
```
