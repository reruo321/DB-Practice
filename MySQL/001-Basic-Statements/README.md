# Basic Statements
## DDL
### CREATE
    CREATE TABLE student(
      id INT,
        name VARCHAR(5),
        major VARCHAR(15),
        sex ENUM('남', '여'),
        PRIMARY KEY(id),
        FOREIGN KEY(major) REFERENCES major(major_name)
          ON DELETE SET NULL
          ON UPDATE CASCADE
    );

Beware that there is **no CREATE DOMAIN** in MySQL. Instead, you can set the similar thing with **ENUM**.

    CREATE DOMAIN sex CHAR(1)
      CONSTRAINT valid-sex CHECK(VALUE IN ('남', '여'));
    
    sex ENUM('남', '여')

### ALTER

    ALTER TABLE major ADD major_dept VARCHAR(15);
    ALTER TABLE major ADD PRIMARY KEY(major_name);

    ALTER TABLE major ALTER major_dept SET DEFAULT '단과대학';

    ALTER TABLE major DROP COLUMN major_id;


### DROP

## DML

## DCL
