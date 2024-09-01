***

**Bar Graph
```    
SELECT exam_id  
    FROM marks  
    GROUP BY exam_id  
    HAVING COUNT(*) = 6;  
  
-- Subquery to merge data from marks and subjects  
WITH merged_data AS (  
    SELECT  
        m.exam_id,  
        GROUP_CONCAT(CONCAT(s.name, ': ', COALESCE(m.grade_point, '0')) SEPARATOR ', ') AS subject_and_grade_points  
    FROM marks m  
    JOIN subjects s ON m.subject_id = s.id  
    WHERE m.exam_id IN (  
        SELECT exam_id  
        FROM marks  
        GROUP BY exam_id  
        HAVING COUNT(*) = 6  
    )  
    GROUP BY m.exam_id  
),  
  
-- Subquery to get student names and semester names by joining exams, report_cards, students, and semester tables  
student_and_semester_data AS (  
    SELECT  
        e.id,  
        st.name AS student_name,  
        sem.name AS semester_name  
    FROM exams e  
    JOIN report_cards rc ON e.report_card_id = rc.id  
    JOIN students st ON rc.student_id = st.id  
    JOIN semesters sem ON rc.semester_id = sem.id  
)  
  
-- Main query to get remarks from the graphs table and join with the merged data and student and semester data  
SELECT  
    sd.student_name,  
    sd.semester_name,  
    md.subject_and_grade_points,  
    g.remark  
FROM merged_data md  
JOIN student_and_semester_data sd ON md.exam_id = sd.id  
LEFT JOIN graphs g ON md.exam_id = g.exam_id;
```


**Line Graph

```
SELECT  
    s.symbol_no,  
    s.name AS student_name,  
    sem.name AS semester_name,  
    g.remark AS remark,  
    GROUP_CONCAT(CONCAT(subj.name, ': ', ROUND(tm.final_grade_point, 1)) ORDER BY subj.name SEPARATOR ', ') AS subjects_and_grades  
FROM  
    total_marks tm  
JOIN  
    students s ON tm.student_id = s.id  
JOIN  
    subjects subj ON tm.subject_id = subj.id  
JOIN  
    exams e ON tm.exam_id = e.id  
JOIN  
    semesters sem ON tm.semester_id = sem.id  
JOIN  
    graphs g ON e.id = g.exam_id  
WHERE  
    g.remark NOT IN ('First Semester', 'Second Semester', 'Third Semester') -- List other semester remarks to exclude  
GROUP BY  
    s.symbol_no,  
    s.name,  
    sem.name,  
    g.remark;
```