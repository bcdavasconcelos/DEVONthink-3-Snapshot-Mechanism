# A third little script - Restore Directly to v0

```applescript

-- Restore Directly to v0

-- bcdavasconcelos 2020-06-09-12-12-27
-- https://github.com/bcdavasconcelos/DEVONthink-3-Snapshot-Mechanism

-- **Do not use this as a backup mechanism.** 
-- These snapshots should be considered *a convenience* for editing plain text.
-- It was not intended to protect from loss of data.

tell application id "DNtp"
	
	set theRecord to (content record of think window 1)
	set thePath to the path of theRecord -- Get the file path	
	
	set theText to the plain text of theRecord
	
	set theText to get custom meta data for "v0" from theRecord default value ""
	
	set the plain text of theRecord to theText
	
	log message "Version restored" info "Restored to template version " & ((current date) as string) --	
	
end tell


```
