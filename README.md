Hello,

This API is developed based on below technologies

  1. I choose Oracle as DB layer becasue I dont have previous work experience on KAFKA,No-SQL (But I do know some of the concepts and did some POC 3 yeas ago) :-)
  
  2. I have used  Java8+Springboot+Hibernate+Oracle to implement this logic.
  
  3. I have created Kafka producer with spring boot to publish the message on Kafka topic.
  
  4. As Hibernate wont allow to create a table without PK. I have created TRASNACTION_ID column for ACCOUNT_TRANSACTIONS table.
  
  5. I have created 2 tables nad insert some test data. For this, we just need run below sql scripts. Infact I can add it to Spring boot project, But I am busy with my work and        its almost 2 days of your deadline is about to finish.
  
  6. No test cases implemented ( It was not asked in your Assesment) :-) If its required I can add them.
  
  create table ACCOUNT_DETAILS(
TRANSACTION_ID number not null,
ACCOUNT_NUMBER varchar2(100) not null,
LAST_UPD_BY timestamp,
AMOUNT number,
PRIMARY KEY (TRANSACTION_ID)
);
    

create table ACCOUNT_TRANSACTION_DETAILS( 
TRANSACTION_ID number not null,
ACCOUNT_NUMBER varchar2(100) not null,
TRANSACTION_TS timestamp not null,
TRANSACTION_TYPE varchar2(30) not null,
TRANSACTION_AMOUNT number not null,
PRIMARY KEY (TRANSACTION_ID)
);
 
 commit;
 
 
 
 
