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

