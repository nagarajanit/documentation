# MySQL Commands

**Create Table command**
```
CREATE TABLE `instructor` (
   `id` int NOT NULL AUTO_INCREMENT,
   `first_name` varchar(255) DEFAULT NULL,
   `instructid` varchar(255) DEFAULT NULL,
   `last_name` varchar(255) DEFAULT NULL,
   `instructor_detail_id` int DEFAULT NULL,
   PRIMARY KEY (`id`),
   KEY `FK5h8q2s9b2twvpdln31m1q70tw` (`instructor_detail_id`),
   CONSTRAINT `FK5h8q2s9b2twvpdln31m1q70tw` FOREIGN KEY (`instructor_detail_id`) 
   REFERENCES `instructor_detail` (`id`)
 );
 ```

 **Get Existing Table schema**
 > `Show CREATE TABLE`