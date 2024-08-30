
### Agenda

1. Brainstorming marks logic

----


Marks entry with a feature to track history

1. marks table
	- id
	- marks_obtained
	- exam_results_id
	- student_id
	- subject_variation_id
	- percentage
	- is_absent
1. exams_result table
	- id
	- reportcard_id
	- type
2. students table
	- id
	- section_id
	- grade_id
	- stream_id
	- semester_id
3. subject_variations table
	- id
	 - subject_id

----
One approach
---

one to many

marks marks_history

helper isolate

marksHistory()

marks->marksHistory()

marks_obtainer: 56



marks


marks_history table
	- id
	- marks_id
	- marks_obtained
	- created_date
	- reason (absent | fail)



Marks

marks ob : 5
is_absent: false

validation - null


exam board




Marks history - upsert (uniq: marks ob, mark_id)

marks ob : 5
reason: false

marks ob : 0
reason: absent

marks ob : 55
reason: absent

---
System marks students as failed:
Failed Filter:


---
Second approach
---

Soft Delete




---
Final Approach - Event Sourcing
---