# Intro
I'm using the first three pilots, as i should be. I am then going to add another 3:  
Pilot 1 - Normal  
Pilot 2 - KB  
Pilot 3 - NoJS  
Pilot 4 - Screen reader  
I want 2 normal pilots just for data collection  

## Pilot 1  
Date: 2025-02-12  
Participant code: P1  
Session ID: P1_5zljfj  
Variant: Standard (HTMX, mouse, JS-on)  
### Task T3  
Participant took 18 seconds out of a given 120  
Participant did not look confused, immediately found box   
Participant did not submit blank by mistake  
Participant did notice success, but it wasn't very obvious at first to them  
Cofnidence: 5  
```
2025-12-02T14:06:00.170233600Z,P1_5zljfj,r_cf7e60bf,T3_add,success,,90,200,on  
```
### Task T1
Participant took 6 seconds out of a given 120  
Participant typed "report"  
There is no result, but there is no visible indication of this   
note: will add items for the next test - don't know if this was needed before this, but a good test of no results  
Confidence: 3 -- due to no result and not being told   
```
2025-12-02T14:09:58.869399300Z,P1_5zljfj,r_62958dbe,T1_filter,success,,30,200,on  
2025-12-02T14:09:59.856707500Z,P1_5zljfj,r_c87d5be9,T1_filter,success,,6,200,on  
2025-12-02T14:10:00.342958600Z,P1_5zljfj,r_9678ddf5,T1_filter,success,,4,200,on  
2025-12-02T14:10:01.879752800Z,P1_5zljfj,r_2eee8d9e,T1_filter,success,,9,200,on  
```
### Task T2
Participant took 15 seconds out of a given 90s  
Participant found the edit button very quick  
Verified that edit saved was easy, as the scroll didn't   
No confusion  
Confidence: 4  
### Task T4
Participant took 10 seconds out of a given 45  
Confirmation was a nice decision   
Confidence: 5
``` 
2025-12-02T14:14:08.969239300Z,P1_5zljfj,r_48898893,T4_delete,success,,10,200,on  
```
### Debrief P1:  
- "It is a good system, i think, but its a bit odd how there is no confirmation of task added"  
- "It worked well enough that i can navigate the system easily"  
- "No "no result found" message ever"  

## Task T1 Notes  

There actually is a notfiication for task added, its just stupidly hidden and almost invisible   

## Pilot 2
Date: 2025-02-12  
Participant code: P2  
Session ID: P2_JUisui  
Variant: Keyboard (HTMX, keyboard, JS-on)  
### Task T3
Timestamp: 14:23   
Took about 30 seconds  
Candidate missed the button originally, this could also be because they never used keyboard navigation  
Didn't shift-tab, instead he went all the way back around  
Apart from that (human) error, the task was completed successfully  
Nothing submitted accidently  
Confidence: 4  
```
2025-12-02T14:22:09.015149900Z,P2_JUisui,r_b7b9b2d5,T0_list,success,,22,200,off  
2025-12-02T14:22:26.508560Z,P2_JUisui,r_56e339ad,T3_add,success,,14,200,on  
```
### Task T1
Timestamp: 14:25  
Took about 20 seconds  
Very quick snap to filter box  
Very quick typing  
Results immediately came up   
```2025-12-02T14:25:50.317912800Z,P2_JUisui,r_e1b29fd3,T1_filter,success,,9,200,on  
2025-12-02T14:25:52.385796800Z,P2_JUisui,r_4374224e,T1_filter,success,,0,200,on  
2025-12-02T14:25:53.586247400Z,P2_JUisui,r_4fba6b9b,T1_filter,success,,7,200,on  
2025-12-02T14:25:56.491719100Z,P2_JUisui,r_58c81a6d,T1_filter,success,,6,200,on  
2025-12-02T14:25:56.607099300Z,P2_JUisui,r_949ef33c,T1_filter,success,,6,200,on
``` 
Confidence: 5  
### Task T2
Timestamp 14:26  
Took about 18 seconds
Very quick finding edit filter button  
The text snapped to the start of the text box, even though it was filled  
This means that he started deleting the old text, but nothing happened until he used arrow key  
Verified and tested  
Confidence: 3  
### Task T4  
Timestamp 14:28  
Took about 10 seconds  
Delete button right below edit, so found easily  
The prompt easily navigated, and shown that it is deleted  
```
2025-12-02T14:28:51.335513200Z,P2_JUisui,r_e843551a,T4_delete,success,,2,200,on  
2025-12-02T14:28:56.299673300Z,P2_JUisui,r_b71735c2,T4_delete,success,,8,200,on  
```
Confidence: 4   
### Debrief P2  
- " I thought the system worked well, even though I did not have much past experience using a keyboard as the only input"  
- "Though I would love it if the colours used for the selection was more contrasty, sometimes it was hard to see if the item was selected"  

## Pilot 3 
Date: 2025-02-12  
Participant code: P3  
Session ID: P3_1FhG3d  
Variant: noJS (HTMX, mouse, noJS)  
### Task T3
Took participant 12 seconds  
Participant mentioned that there is no task added confirmation (at least in NoJS)  
Task was added successfully, page refresh and user scrolled for confimration  
No hesistaion as the button is quite obvious   
```2025-12-02T14:37:48.911654800Z,P3_1FhG3d,r_9178ca6e,T3_add,success,,23,200,off
2025-12-02T14:37:48.938694800Z,P3_1FhG3d,r_f6800ad4,T0_list,success,,19,200,off
```
Confidence: 5   
### Task T1  
Took participant 17 seconds  
no-JS implementation with updating the HMTL element server-side worked perfectly  
correct task identified, no total list of tasks avaliable  
```
2025-12-02T14:40:59.212334500Z,P3_1FhG3d,r_da3642c9,T1_filter,success,,10,200,on
2025-12-02T14:41:00.259630800Z,P3_1FhG3d,r_4aad4cc5,T1_filter,success,,7,200,on
2025-12-02T14:41:03.775989100Z,P3_1FhG3d,r_396cf391,T1_filter,success,,10,200,on
```
Confidence: 4  
### Task T2
Took participant 25 seconds  
Task was edited successfully  
Correct button easily found and used  
EDIT WORKS IN NO-JS - this didn't work earlier, maybe a bug?!?   
Confidence: 3   
### Task T4   
Took participant 10 seconds   
Task was deleted and page refreshed without task   
Confirmation worked, but user didn't expect it, maybe because theres no other confirmation of tasks that this seems "out of place" 
```
2025-12-02T14:44:33.812354400Z,P3_1FhG3d,r_9b24b622,T4_delete,success,,6,200,on
```
Confidence: 3  
### Debrief P3:
- "I thought that this was quite easy to use"  
- "Literally 1 or two things were wrong I think one of them was with the confirmation, I didn't expect it"  
- "You looked shocked when I edited tasks" - yeah because it was broken 10 minutes ago...?  
## Pilot 4 
Date: 2025-02-12  
Participant code: P4  
Session ID: P4_AEh6u7  
Variant: Screen Reader (HTMX, mouse allowed (but keyboard actually used), JS-on)  
### Task T3  
Took about 50 seconds  
Alert and document noises worked fine  
Uses NVDA screen reader  
My friend accidentally clicked on the submit button before anything else, and the alert was read out   
I guided my friend to the box, as he never used a screen reader before, but it worked fine  
The alert after adding task was not spoken!    
```
2025-12-02T14:51:32.684580800Z,P4_AEh6u7,r_36ac3d74,T0_list,success,,24,200,off
2025-12-02T14:55:02.984197400Z,P4_AEh6u7,r_47253b5d,T3_add,success,,44,200,on
```
Confidence: 3/5  
### Task T1
Took about 45 seconds  
Task was filtered easily  
The alert sounds played correctly, and the system worked perfectly   
Friend could go through all the tasks, and make sure the right one appeared  
```
2025-12-02T14:58:57.622544Z,P4_AEh6u7,r_c8f2910e,T1_filter,success,,11,200,on
2025-12-02T14:59:01.472216600Z,P4_AEh6u7,r_980acac3,T1_filter,success,,6,200,on
```
Confidence: 3/5  
### Task T2
Took about 30 seconds, task edit was read fine  
There was no confirmation, just like some other tasks taken by P4  
Confidence: 3/5          
### Task T4  
Took about 30 seconds, Task deletion warning was read, and the task was deleted   
No confirmation for some reason - I think I need to check this   
Even though - my friend did not care much for the conformation, as he trusts the system   
```
2025-12-02T15:01:15.317114400Z,P4_AEh6u7,r_5f382d6a,T1_filter,success,,11,200,on  
2025-12-02T15:01:39.907001200Z,P4_AEh6u7,r_0161e344,T4_delete,success,,6,200,on  
```
Confidence: 4/5  
### Debrief P4  
- "This was really really weird, ive never done anything like this"  
- "It was really hard to visualise the website, but that was expected as I didn't do anything like this before"  
- (asked about confirmation) "Oh yeah, theres no confirmation, and sometimes I missed the text and had to repeat it.  "















