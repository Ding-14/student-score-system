表名：student

说明：存储学生基本信息

主键：student\_id（学号）



字段：

student\_id   VARCHAR(20)    NOT NULL    PRIMARY KEY     # 学号（主键，非空）

name         VARCHAR(10)    NOT NULL                    # 姓名（非空）

gender       CHAR(2)                                   # 性别（男/女）

age          INT                                       # 年龄

class\_name   VARCHAR(30)                               # 班级

create\_time  DATETIME                                  # 记录创建时间

表名：teacher

说明：存储教师信息

主键：teacher\_id（教师编号）



字段：

teacher\_id   VARCHAR(20)    NOT NULL    PRIMARY KEY     # 教师编号（主键）

name         VARCHAR(10)    NOT NULL                    # 姓名（非空）

subject      VARCHAR(30)    NOT NULL                    # 主讲课程（非空）

phone        VARCHAR(11)                               # 联系电话





\## 表名: course

说明: 存储课程基本信息

主键: course\_id (课程号)



字段:

course\_id  VARCHAR(20)  NOT NULL  PRIMARY KEY  # 课程号（主键，非空）

course\_name VARCHAR(50) NOT NULL               # 课程名称（非空）

credit     INT          NOT NULL               # 学分（非空）

teacher\_id VARCHAR(20)  NOT NULL               # 授课教师编号（外键，关联teacher表）



\---



\## 表名: score

说明: 存储学生选课成绩信息

主键: id (自增ID)



字段:

id         INT          NOT NULL  AUTO\_INCREMENT  PRIMARY KEY  # 自增ID（主键）

student\_id VARCHAR(20)  NOT NULL                 # 学号（外键，关联student表）

course\_id  VARCHAR(20)  NOT NULL                 # 课程号（外键，关联course表）

score      DECIMAL(5,2)                          # 成绩（0-100，保留两位小数）

create\_time DATETIME                             # 成绩录入时间

