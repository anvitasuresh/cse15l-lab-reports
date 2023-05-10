# Using `grep` in the command line

Grep is a command line argument that is used to search through files for a specific pattern. It will display any lines in the file that match the pattern given in the command line. The basic usage for grep is as follows: `grep (argument 1) (argument 2)`. In this case, (argument 1) is the patter that you are looking for and (argument 2) is the file that you want to search in. Additionally, there are many options that can be used to modify the behavior of grep in the command line. 

## Option 1: `grep -r`
One option is -r which recursively searches for the pattern in all of the files and subdirectories. This will come in handy when you need to find a string that repeats multiple times in a directory.

## Option 2: `grep -v`
Another option is `grep -v` which inverts the search and shows the lines that do not match the pattern. 
One example of using this command with the string search data is as shown below. This grep command using -v will show all of the lines in the file chapter-1.txt that do not contain the string 'the'. This is useful in any scenario where you want to find lines that do not contain a certain string, since this might be easier than searching for the string itself: 
`grep -v "the" chapter-1.txt`

`"WE HAVE SOME PLANES"
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

## Option 3: `grep -e`
Another option is -e which can be used to search for multiple patterns in one search at the command line.

## Option 4: `grep -C`
Another option is -C which shows the lines before and after the line where the pattern matches.
