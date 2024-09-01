


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