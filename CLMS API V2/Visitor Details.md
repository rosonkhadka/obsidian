1. Index VD - Done
2. Store VD - Changes Needed 
	1. Handle
3. Show VD - Done
4. Update VD - Changes Needed
	1. Handle
5. Delete VD - Done
6. Restore VD - Done
7. Force Delete VD - Done
8. Import VD - TODO
	1. Event name must exists on the db - Done
	2. Duplicate event name cannot be on the payload - Done
	3. Updated first_counselled_by - To auth user - Done
9. Data Merge
	1. Color - Assignment (Duplicate)
	2. Duplicate
		1. If visitor_type
			1. Walk-in
			2. Event
		2. Name and Number 
		Mark as duplicate - VD
	----
		1. Merged with other caes:
			1. Color assignment
			2. Add Remark - System
			3. Make visitor type - Event

1. Archive VD - Done
2. Unarchive VD - Done
3. Get Archive Visitor Details - Might need changes (UI)
4. Assign VD - Done
5. Unassign VD - Done
6. Admitted Visitor - TODO
	1. When the data comes from admission system, student details
		1. Check if user with name and email - is in the system, then update the VD lead with category (Name)
		2. Must - have the category in the rabbitmq - Queu

-----
Remarks
1. Store - Done
2. Delete - Verification need
	1. Caller - permission
3. Update - Done
4. Restore - Done
----
Event 
1. Index - Done
2. Show - Done
3. Store - Verification Need
	1. Name - Unique
4. Update - *
5. Delete - Done
6. Restore - Done
7. Force Delete - Done
8. Import - Done

----
Event Type
1. Index - Done