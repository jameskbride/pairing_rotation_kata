# Pair Rotation Kata

This kata simulates pair switching on a team of eight developers who practice pair-programming to complete stories within a sprint. Each pair works on a story that takes one, two, or three days to complete, and the sprint is 10 days (two work weeks). The team has a backlog of stories and a sprint commitment which they agreed on. The purpose of this kata is to implement a system for managing pair switching within a sprint that allows the team to meet their sprint commitment.

## Feature 1: Pair rotation

As a member of the development team
In order to spread knowledge of the project
I want to pair switch regularly

Given a day within the sprint the system should determine what the current pairs are based on the rules listed below. Pairing should begin on a Monday (the start of the sprint). Each developer has a name and a title (either 'DEVELOPER' or 'TECH LEAD'). When a pair is formed the system should output the message 'New pair: &lt;TITLE&gt; &lt;NAME&gt; and &lt;TITLE&gt; &lt;NAME&gt;' where each title/name pair belongs to the member of a pair in question.

This team has normed on pair switching on Mondays and Wednesdays in order to keep the pairing fresh and spread knowledge optimally. There is a problem however, in that there are two tech leads on this team.  These tech leads get pulled into meetings frequently, which causes friction for the developers that they pair with. In order to keep the pairing moving smoothly the team has come up with some norms, listed below:

### Rules

1. No pair should work together twice in one week when pair switching.
2. No developer should pair consecutively with a tech lead when pair switching unless this breaks Rule 1.
3. Tech leads should not pair together unless this breaks Rule 1 or 2.

## Feature 2: Completing stories

## Feature 3: Meeting Sprint commitment
