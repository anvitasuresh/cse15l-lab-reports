# Using `grep` in the command line

Grep is a command line argument that is used to search through files for a specific pattern. It will display any lines in the file that match the pattern given in the command line. The basic usage for grep is as follows: `grep (argument 1) (argument 2)`. In this case, (argument 1) is the patter that you are looking for and (argument 2) is the file that you want to search in. Additionally, there are many options that can be used to modify the behavior of grep in the command line. 

## Option 1: `grep -i`
One option is -i which searches for lines that matches the pattern given regardless of whether it is uppercase or lowercase. 
An example of using this command with string search data is shown below. Using grep -i will show all of the lines in the file jounal.pbio.0020001.txt that have the word science in it even if it is upper/lowercase. This is useful because it helps to find any string regardless of case.

command: `grep -i "science" journal.pbio.0020001.txt`

output: ` the clear inequalities in science between developing and developed countries and to the
        importance of reducing the inequalities in science between developed and developing
        88% of all scientific and technical publications registered by the Science Citation Index
        It is rather obvious that richer countries are able to invest more resources in science
        contributions to science, despite the fact that the average proportion of gross domestic
        product (GDP) invested in science in Latin America throughout this 10-year period was only
        productivity is remarkable when we compare it with the relatively low investment in science
        rate as well as in financial investment in science and technology. Some countries have
        funding to the most productive scientists from the national science development programs
        and global change biology) between 1990 and 2002 in both the two top general science
        Science ; with impact factors of 27.96 and 23.33, respectively) and in
        Science and 
        Science and 
        American researchers are not shying away from the two top-ranked general science journals.
        Science and 
        ecology and environmental sciences emphasizes the overwhelming contributions of authors
        conspiracy, but rather it implies that the perception of the most important science is
        science is most interesting to them. Another consideration is that more local journals from
        developing world (Goldemberg 1998; Annan 2003). One is that science, as a discipline, would
        Brazil (Goldemberg 1998) and biomedical sciences in Cuba (Castro Díaz-Balart 2002). These
        to the sciences will be an excellent investment by developing nations in terms of`
        
Here is another example. In this one, I am searching for the word "diversity" in the file diversity_priorities.txt. This is helpful because I want to see where it mentions diversity, not caring about whether it is uppercase or not.

command: `grep -i "diversity" diversity_priorities.txt`

output: `national conference on diversity in the legal services community.
Focusing on broad aspects of diversity - including, among others,
national origin - participants examined diversity-related strengths
the context of a series of dialogues on diversity that NLADA and
Identify and prioritize diversity-related issues that
Identify key diversity-related challenges that exist
Although there was concern about diversity, there was
greater gender diversity and pursued activities to bring women into
Many programs hold diversity training sessions for staff
serious diversity challenges continue to affect our
dialogue on diversity to local action. How can programs strengthen
Today's diversity approaches stress inclusion of people
excuses. We realize that diversity can help programs reach clients
to achieving diversity in program leadership.
third careers. Our leadership will reflect the expanded diversity
leaders. Diversity will be reflected in our community's everyday
and new definitions of diversity and leadership will be crafted. We
Turning to the importance of diversity, participants agreed that
giving diversity concerns their time, energy, attention and
others. Diversity allows us to tap into human genius, inspiration
not achieved without certain difficulties. Diversity "pioneers"
Proponents of increased diversity may face criticism from staff or
supervisors for "spending too much time on diversity." Since legal
diversity work within programs is not easy and requires the support
Framing diversity efforts in positive and practical terms
authentic commitment to diversity throughout each program is
program's belief in the value of diversity is best shown by the
diversity and developing strategies to maximize the benefits and
diversity
place to ensure that "diversity" goes beyond race. Additionally,
definition and vision of diversity and earmarking resources so that
of supporting people who are advocates for diversity, including
vision of diversity. Some felt that there had been loss of trust by
reflect the diversity of the communities they serve.
Indicators of success --We endorse a common vision of diversity
and diversity issues are included in every state plan. Effective
policies that implement diversity goals are adopted throughout each
on aggressive discrimination-based advocacy and attaining diversity
innovative diversity agendas and model projects.
diversity. A national leadership institute is created and begins to
compile and disseminate information on successful diversity
commitment to diversity. On the local and national levels,
Developing a Common Definition and Vision of Diversity
A common definition of diversity is developed. It is informed by
success is tied to and evaluated in terms of diversity initiatives.
All programs commit to addressing internal diversity concerns.
developed where programs share ideas on diversity successes. There
are regular diversity conferences for state justice community`

## Option 2: `grep -v`
Another option is `grep -v` which inverts the search and shows the lines that do not match the pattern. 
One example of using this command with the string search data is as shown below. This grep command using -v will show all of the lines in the file chapter-1.txt (which is in the 911report directory) that do not contain the string 'the'. This is useful in any scenario where you want to find lines that do not contain a certain string, since this might be easier than searching for the string itself: 

command: `grep -v "the" chapter-1.txt`

output: `"WE HAVE SOME PLANES"
INSIDE THE FOUR FLIGHTS
    Boston: American 11 and United 175. Atta and Omari boarded a 6:00 A.M. flight from Portland to Boston's Logan International Airport.
    Between 6:45 and 7:40, Atta and Omari, along with Satam al Suqami, Wail al Shehri, and Waleed al Shehri, checked in and boarded American Airlines Flight 11, bound for Los Angeles. The flight was scheduled to depart at 7:45.
    Their flight was scheduled to depart at 8:00.
    The 19 men were aboard four transcontinental flights.
IMPROVISING A HOMELAND DEFENSE
The FAA and NORAD
American Airlines Flight 11
    NEADS: Is this real-world or exercise?
    FAA: No, this is not an exercise, not a test. 
United Airlines Flight 175 
    UAL 175: New York UAL 175 heavy.
    FAA: UAL 175 go ahead.
    FAA: Oh, okay. I'll pass that along over here.
    The New York Center controller and manager were unaware that American 11 had already crashed.
    Terminal: Got him just out of 9,500-9,000 now.
    Center: Do you know who he is?
    Terminal: We're just, we just we don't know who he is. We're just picking him up now.
    New England Region: Yes, I am.
    Unidentified Female Voice: They have what?
    Boston Center: Planes, as in plural.
    FAA: Yes.
    NEADS: On its way towards Washington?
    NEADS: Okay.
    NEADS: He-American 11 is a hijack?
    FAA: Yes.
    NEADS: And he's heading into Washington?
    FAA: Yes. This could be a third aircraft.
    There was no response.
    The controller responded: "United 93, understand you have a bomb on board. Go ahead." The flight did not respond.
    Command Center: Uh, do we want to think, uh, about scrambling aircraft?
    FAA Headquarters: Oh, God, I don't know.
    FAA Headquarters: Yes.
    FAA (DC): Go ahead.
    NEADS: United nine three, have you got information on that yet? FAA: Yeah, he's down.
    NEADS: He's down?
    FAA: Yes.
    NEADS: When did he land? 'Cause we have got confirmation- FAA: He did not land.
    NEADS: Oh, he's down? Down?
NATIONAL CRISIS MANAGEMENT
The Agencies Confer
    We believe this call would have taken place sometime before 10:10 to 10:15.
    Controllers: Copy that, sir.
    Floor Leadership: So if you're trying to divert somebody and he won't divert- Controllers: DO [Director of Operations] is saying no.
    SecDef: Yes, I understand. Who did you give that direction to?
    Vice President: Yes, it has.
    SecDef: We can't confirm that. We're told that one aircraft is down but we do not have a pilot report that did it.
What If?`

Another example is as follows. This command will search the file 1468-6708-3-1.txt which is in the biomed directory and find all of the lines that do not contain the letter a: `grep -v "a" 1468-6708-3-1.txt`

`Introduction
        elderly [ 9 ] .
          Study
         ] .
          (for persons who were never in excellent, very good, or
          report results using only the simpler definition.
          findings.     
        Results
        likely.
        from 25 to 29.9. The second column, which shows results
        under 20.
        groups.
        YOL or YHL.
        Discussion
          YHL.
        Conclusion
        'overweight' by the NHLBI guidelines. This suggests using      
        Competing interests
        CESD Center for Epidemiologic Studies Depression
        poor?`

## Option 3: `grep -e`
Another option is -e which can be used to search for multiple patterns in one search at the command line. This command can be very helpful when you want to narrow down your search in the files more than just down to one pattern. `grep` will print out the lines if it finds matches for any of the patterns provided.
An example of using this is shown below. In this case, I am searching the file DraftRecom-PDF.txt for two different strings ("recommendation" and "address"). It is much easier and more efficient to do this than searching for the patterns separately.

command: `grep -e "recommendations" -e "address" DraftRecom-PDF.txt`

output: `recommendations from conference deliberations. Before the
conference, he and Daniel Pollock drafted recommendations for the
committee modified those recommendations, and they were distributed
achieve unanimity regarding the recommendations, but to have
be to discuss the recommendations one by one, identifying any gaps
sequence of the recommendations did not imply a priority order.
Because the published recommendations will include supporting text,
address the full spectrum of alcohol problems among ED
Gordon Smith suggested that the recommendations should address
recommendations.
to patients. Perhaps the recommendations should address alcohol
suggested that the recommendation be clear that it is addressing
Edward Bernstein pointed out that the recommendations would
research recommendations with a recommendation that included
in the supporting text, she suggested addressing the different
Daniel Pollock added that the message of the recommendations
clinicians understand the recommendations better. If we do not, a
Catherine Gordon proposed that the recommendations address the
Brown praised the recommendation for addressing a very important
addresses. He noted that alcohol screening in the ED is currently
recommendations to the high-risk environment in which these people
explicit somewhere in the recommendations.
"Research in this category may address a broad range of
Ries thought that the recommendations should encourage studying
Pat Lenaghan suggested that clinicians need recommendations
General comments about the recommendations
proposed recommendations, Hungerford asked if they had general
comments about the recommendations overall.`

Another example is shown below for this command. In this example, I am searching for the words drinking and anxiety in the file Session2-PDF.txt. 

command: `grep -e "drinking" -e "anxiety" Session2-PDF.txt`

output: `disease develops. WHO defines hazardous drinking as 4 or more
drinking as consumption of more than 14 drinks/week or more than 4
drinks/occasion is considered at risk. Binge drinking alone is also
identifying patients with binge drinking, we can define binge
drinking as 3, 4, 5, or 6 drinks on an occasion. Screening tests
other drug use, depression, and anxiety disorders. Many of the
spontaneously volunteer information about drinking. Cherpitel
reported that patient self-report of drinking prior to arrival had
setting-"Have you ever had a drinking problem?"-had a high
at-risk drinking in addition to alcohol abuse and dependence. AUDIT
at-risk drinking, alcohol abuse, and dependence. It is a
those screens, which covered feeling guilty after drinking,
blackouts, failing to do what is normally expected after drinking,
and morning drinking. However, this new instrument has not been
drinking, or abuse.5,36
primary care setting. For at-risk, hazardous, or harmful drinking,
self-reported drinking.7 In another ED study, a saliva alcohol
drinkers: lack of sensitivity of the two-question drinking test. Am
drinking: does a single question work? J Fam Pract
pregnancy risk-drinking. Alcohol Clin Exp Res 1994;18:1156-61.
prenatal detection of risk-drinking. Am J Obstet Gynecol
drinking in the emergency room: the RAPS4. Rapid Alcohol Problems
instruments for problem drinking among blacks, whites and Hispanics
screening instruments for identifying harmful drinking and alcohol
hazardous/harmful drinking among subcritically injured patients.
A. Screening for excessive alcohol drinking: comparative value of
Screening for problem drinking in college freshmen. J Am Coll
drinking in college students. J Am Coll Health 1991;39:227-31.
drinking among college freshman. J Adolesc Health
screening measure for problem drinking among female college
60. Dawson D, Archer L. Relative frequency of heavy drinking`

## Option 4: `grep -c`
Another option is -c which returns the number of lines that match the pattern provided in the command line. It does not display the lines itself, but rather a single integer. This command is useful when you do not want the actual lines themselves but just want to know how many times a certain pattern is present in a file.
One example is as shown below. Here, I am looking for how many lines in the file 1468-6708-3-4.txt for how many lines contain the word "death" and it returned 10. 

command: `grep -c "death" 1468-6708-3-4.txt`

output: `10`

Another example is shown below. In this case, I want to see how many lines in the file 1471-213X-1-10.txt contain the word "gene". 

command: `grep -c "gene" 1471-213X-1-10.txt`

output: `99`

## Sources
I found out about the options of the grep command in two ways. One was through this website [Link](https://man7.org/linux/man-pages/man1/grep.1.html). The other way was by asking ChatGPT!
