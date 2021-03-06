# Pair Rotation Kata

This kata simulates pair switching on a team of eight developers who practice pair-programming to complete stories within a sprint. Each pair works on a story that takes one, two, or three days to complete, and the sprint is 10 days (two work weeks). The team has a backlog of stories and a sprint commitment which they agreed on. The purpose of this kata is to implement a system for managing pair switching within a sprint that allows the team to meet their sprint commitment.

## Feature 1: Pair rotation

*As a member of the development team*

*In order to spread knowledge of the project*

*I want to pair switch regularly*

This team has normed on pair switching on Mondays and Wednesdays in order to keep the pairing fresh and spread knowledge optimally. There is a problem however, in that there are two tech leads on this team.  These tech leads get pulled into meetings frequently, which causes friction for the developers that they pair with.

Pairing should begin on a Monday (the start of the sprint). Each developer has a name and a title (either 'DEVELOPER' or 'TECH LEAD').  The system should walk through each day of the sprint, printing the day of the week ('MONDAY', 'TUESDAY', 'WEDNESDAY, 'THURSDAY', 'FRIDAY'), followed by the pairs. When a pair is formed the system should output the message *'New pair: &lt;TITLE&gt; &lt;NAME&gt; and &lt;TITLE&gt; &lt;NAME&gt;'* where each title/name pair belongs to the member of a pair in question.  If a pair does not change the system should output *'Paired &lt;NUMBER OF DAYS PAIRED&gt; days: &lt;TITLE&gt; &lt;NAME&gt; and &lt;TITLE&gt; &lt;NAME&gt;'*. Pair switching should follow the rules listed below:

### Rules

1. No pair should work together twice in one week when pair switching.
2. No developer should pair consecutively with a tech lead when pair switching unless not doing so breaks Rule 1.
3. Tech leads should not pair together unless not doing so breaks Rule 1 or 2.

Example output:
<pre>
MONDAY
New Pair: DEVELOPER Tom and TECH LEAD Mark
New Pair: DEVELOPER Kristen and DEVELOPER Jim
New Pair: DEVELOPER Jason and DEVELOPER Matt
New Pair: DEVELOPER Cory and TECH LEAD Kevin

TUESDAY
Paired 2 days: DEVELOPER Tom and TECH LEAD Mark
Paired 2 days: DEVELOPER Kristen and DEVELOPER Jim
Paired 2 days: DEVELOPER Jason and DEVELOPER Matt
Paired 2 days: DEVELOPER Cory and TECH LEAD Kevin

WEDNESDAY
New Pair: DEVELOPER Kristen and DEVELOPER Matt
New Pair: DEVELOPER Jason and TECH LEAD Kevin
New Pair: DEVELOPER Jim and TECH LEAD Mark
New Pair: DEVELOPER Tom and DEVELOPER Cory

...
</pre>
## Feature 2: Completing stories

*As a member of the dev team*

*In order to complete features for the project*

*I want to work on user stories*

Throughout the sprint pairs will complete user stories in order to complete the project.  A pair may pick up a story which is sized as either 1, 2, or 3 days.  When a story is complete the pair will pick up another story.  If a pair switch occurs while a story is in progress at least one individual must "anchor" the story in order to minimize context switching. The rules from the previous feature must still be observed, with the added anchor requirement.  

## Feature 3: Meeting Sprint commitment
