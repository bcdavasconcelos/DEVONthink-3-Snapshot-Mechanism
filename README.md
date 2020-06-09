# A Snapshots Mechanism for DEVONthink 3

## Warning
1. **Do not use this as a backup mechanism.** These snapshots should be considered *a convenience*. It was not intended to protect from loss of data. There is no safety net here.
2. These are **potentially destructive** scripts. **You cannot ⌘Z your way out of changes made by scripts.**
3. Finally, this is intended for markdown and/or plain text **only**.

***

# The first script: Save Snapshot

The idea is very simple. I created custom metadata fields to store snapshots of the text (**v1**-**v9**) and the modification time (**d1**-**d9**).


![][image-1]  	

*I keep it at the bottom, so I don't see it if I don't want to.*

The [first script](1_Save_Snapshot.md) is for *storing the text*. It will store the current text in v1 and throw what was in v1 to v2, what was in v2 to v3 and so on. What was in v9 says goodbye.

***

## The second script: Compare/Restore Snapshot

The [second script](2_Compare_or_Restore_Snapshot.md) is for *restoring a snapshot*. When it is activated, it will ask whether you want to compare snapshots using BBEdit (could have used filemerge or something else, but I like BBEdit and you can install it for free) or simply restore to one of the previous snapshots.

![][image-2]

The next dialog will prompt for the desired snapshot to be compared or restored.


![][image-3]

If you chose to **restore**, that's it. The script will do so by replacing the text of the record by the stored snapshot and it will log the change in DEVONthink (I like how discrete the log is and prefer it over the notification function). If you chose to **compare** instead, you *can* make the changes you want and then *save*. 

*Here is the compare window open in BBEdit.*  

![][image-4]

***

## A third little script - Restore Directly to v0

Side-note: I am also keeping a v0, which is sort of a template for the note and which won't be touched by the first script. I also set up a special shortcut to restore directly to this snapshot without any prompts. This will be the [third script](3_Restore_Directly_to_v0.md).


[image-1]:	img/1.png
[image-2]: img/2.png
[image-3]: img/3.png
[image-4]: img/4.png

#Applescript #DEVONthink