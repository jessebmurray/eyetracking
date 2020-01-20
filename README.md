# Eyetracking

The data files are available for download here: 
https://www.dropbox.com/sh/4au2fky38gojrwj/AABITum8SzHVav1GUNYWgq7pa?dl=0


## Mistakes/edge cases in the data:
1. Switching to the next word immediately instead of doing a countdown begins with participant 4 (inclusive).
2. We started using five letter words and the new prompt, which means the  black_break_image was started, beginning with participant 5 (including participant 5). After that, no more changes were made to the stimuli.
3. Participant 6: Accidentally skipped the third word (brown) **(removed)**, accidentally skipped the final calibration.
4. Participant 7: Bad calibration.
5. Participants 8, 9: ‘P09’ in the ‘ParticipantName’ column is actually participant 8, ‘P9’ which comes after P09 is participant 9. **(Fixed: Replaced 'P09' with 'P08' and 'P9' with 'P09')**
6. Participant 12: Only use the data from the left eye because the participant has a lazy right eye, maybe copy the left eye data to the right eye. Also, the participant stared at the center of the screen for the third word ‘brown’ throughout the entirety of that word. **(Fixed: Replaced gen_gazeX and gen_gazeY with left eye gaze data, removed 'brown')**
7. Participant 13: Stares at the screen for the word ‘brown’ for a while, didn’t know that a new word was displayed.
8. Participant 14: Uses the same file, which means uses the same words, as participant 13. **(Not a Problem)**
9. Participant 15: Accidentally skipped final calibration. **(Not a Problem)**
10. Participant 16: The words brown and junior were switched, so the third word is actually junior, not brown, the participant never got to see junior because they only got to ‘closed’.  **(Not a Problem)**
11. Participant 19: Quality of data is terrible, probably can’t use. **(Fixed: Deleted Participant 19 Data)**
12. Participant 26: The words brown and power were switched so brown was second then power was third. **(Not a Problem)**


## Things to Add to the Dataset:
1. Add whether the participant solved the word.
2. Add what the participant’s guesses were.
3. Add the answers for the post-experiment questionnaire.

## Things to Remove from the Dataset:
1. If on the word for less than a second or so, remove (these are the ones we skipped past) although this will likely have an exception so verify with the Recording sheet. **(Done, still needs some fixing though)**

## Possible ML applications:
1. Predict whether the word was solved correctly (based on the eye-tracking data and possibly other data as well).
2. Predict which participant (out of the 29) is working on the anagram. 
3. Do KNN classification of the fixations and see how that lines up with the location of the letters.
4. Use metrics such as: average time between saccade (how slowly does the participant move their eyes around), the proportion of adjacent sequences - as opposed to moving across the screen, the tendency to scan clockwise versus counterclockwise, time spent within letter radius (dwell duration).

## Tests to run:
1. Compare the dwell durations on the letters for correct and incorrect (+ or - standard deviation for the error bar?).
2. Make a confidence level of 0 to 1 for distance of 2R to 0 from a letter, where R is 143 for for five letter and 129 for six letter. 
3. Averaged over all the participants, does the proportion of correct sequences immediately prior to a solution? (That would indicate prior knowledge of a solution).

## Things to do:
1. Start making a dataframe with 1 row per participant-word.
2. Fix the issue of the 123456 showing up twice, rename the second one.



