# table: departments
- id BIGINTUNSIGNED PK AUTO UNIQUE NOTNULL
- name VARCHAR(80) NOTNULL

# table: degree_courses
- id BIGINTUNSIGNED PK AUTO UNIQUE NOTNULL
- name VARCHAR(80) NOTNULL
- id_department FK BIGINTUNSIGNED NOTNULL
<!-- many to many con courses -->

# table: courses
- id BIGINTUNSIGNED PK AUTO UNIQUE NOTNULL
- name VARCHAR(80) NOTNULL
- teacher_id BIGINTUNSIGNED FK NOTNULL
<!-- many to many con teachers -->

# table: teachers
- id BIGINTUNSIGNED PK AUTO UNIQUE NOTNULL
- name VARCHAR(40) NULL
- surname VARCAHR(40) NOTNULL

# table: exams
- id BIGINTUNSIGNED PK AUTO UNIQUE NOTNULL
- name VARCHAR(80) NOTNULL
- id_cours BIGINTUNSIGNED FK NOTNULL
- data DATATIME NOTNULL

# table: students
- id BIGINTUNSIGNED PK AUTO UNIQUE NOTNULL
- name VARCHAR(40) NULL
- surname VARCAHR(40) NOTNULL
- id_degree_cours FK BIGINTUNSIGNED NOTNULL
<!-- many to many con exams -->