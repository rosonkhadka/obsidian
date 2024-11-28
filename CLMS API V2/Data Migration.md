DONE
---
User
Cluster
Call Center Category
Lead Category
College
Lead
Assign
Archive
Cluster Follow up 
Remark


Remarks Migration
---
Current Table Setup
1. Cluster Follow up
	1. Lead ID
	2. User ID
	3. Remark ID
	4. Created By
	5. Updated By
	6. Follow Up Date
	7. Tentative Visit Date
	8. Next Follow UP Date
	9. Timestamp
	
2. Lead Remark
	1. Lead ID
	2. Remarks
	3. Status
	4. Created By
	5. Creator Email
	6. Updated By
	7. Deleted At
	8. Timestamp

Upcoming
1. Remarks
	1. id - Comes from remarks tbl - id
	2. remarkable_type - Defaults to Lead::class
	3. remarkable_id - Comes from remarks tbl - lead_detail_id
	4. user_id (Creator) - Can come from cluster_follow_ups tbl - user id (Deleted User Issue) 
	5. remark - Comes from remakrs tlb - remarks 
	6. follow_up_date - Comes from cluster_follow_ups tbl - follow_up_date
	7. tentative_visit_date - Comes from tentative_visit_date tbl - follow_up_date
	8. next_follow_up_date - Comes from next_follow_up_date tbl - follow_up_date
	9. follow_up_status - No Need
	10. status - Comes from remarks tbl - status
	11. meta - null
	12. deleted_at - Comes from remarks tbl - deleted_at
	13. created_at - Comes from remarks tbl
	14. updated_at - Comes from remarks tbl