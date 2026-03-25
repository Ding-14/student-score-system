表名：course
说明：存储课程信息
主键：course_id（课程号）
外键：teacher_id 关联 teacher(teacher_id)

字段：
course_id    VARCHAR(20)    NOT NULL    PRIMARY KEY     # 课程号（主键）
name         VARCHAR(50)    NOT NULL                    # 课程名称（非空）
teacher_id   VARCHAR(20)    NOT NULL                    # 授课教师编号（外键）
credit       INT              NOT NULL                 # 学分（非空）
class_time   VARCHAR(50)                               # 上课时间
表名：score
说明：学生选课成绩（核心关联表）
联合主键：student_id + course_id
外键：
  student_id  REFERENCES  student(student_id)
  course_id   REFERENCES  course(course_id)

字段：
student_id   VARCHAR(20)    NOT NULL     # 学生学号（外键）
course_id    VARCHAR(20)    NOT NULL     # 课程号（外键）
score        DECIMAL(5,1)                # 成绩（0~100.0）
PRIMARY KEY (student_id, course_id)      # 联合主键