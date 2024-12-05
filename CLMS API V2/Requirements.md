Visitor Details
---
1. Events
	1. All Done
2. Visitor Details
	1. No event name - Individual
	2. Event Handle Logic - Done
		1. Individual Insert
			1. Remarks
				1. Creator
				2. Date
					1. Remarks
						1. DTO
		2. Bulk
			1. Remarks
				1. Event Name (Event Visited : {Name})
	* * Highlights
		* Admitted Visitor:
			* Comes from admission (Name and Number) Exact match
			* Model update - Visitor Category - 10
		* Duplicate Profile
			* Every Data Logic Check
			* == (Walk IN & Event) != Duplicate
		-  Merged Data (Overwrite Event **priority**)
			- `Visitor profile " **samjhana karki**" (**9847799090**) was merged with visitor profile "**Test Dev Merge Event Yes**" (**9847799090**), "**Jiya**" (**9847799090**), "**Johnsonnn**" (**9847799090**) by **kritika**.`
			- **another message for cancellation**
			- First Event
				- True
					- == Walk IN
						- Merge
			- Else
				- Duplicate



---
Import / Import Logs

-----
VISITOR TYPE

---

Policy
---
Superadmin - *
Ingsupervisor - | -(Delete, ID Logs, Remarks Delete, Update {Timeframe}) | Event Add, Update
supervisor - | -(Import, ID Logs, Delete, Remarks Delete, Update {Timeframe}, Event CRUD)
BD | -(Import, ID Logs, Delete, Remarks Delete, Update {Timeframe}, Event CRUD)
caller | -DO(Remarks, Update (Visitor category, Secondary Phone Number (Personal))) | Assigned Date ()

---

Additional Requirement
---



College 
	1. All other address removed
------
Remarks Reporting
	1. College Distinct
		1. Last Caller - Date
		2. Total Remarks

Assign
	1. 




