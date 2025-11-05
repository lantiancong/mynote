## 配置项

```mysql
CREATE TABLE student (
  id INT PRIMARY KEY AUTO_INCREMENT,
  stu_name VARCHAR(10) NOT NULL,
  stu_age INT NOT NULL,
  stu_gender CHAR(1) NOT NULL,
  stu_phone BIGINT NOT NULL,
  stu_edu VARCHAR(5),
  stu_birth DATE
)
  ENGINE INNODB 
  DEFAULT CHARSET utf8;

```

> ENGINE INNODB 
>
> DEFAULT CHARSET utf8;
>
> 这两个字段要放括号外