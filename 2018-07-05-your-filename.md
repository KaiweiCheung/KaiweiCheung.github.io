





Delimiter $$
create procedure archemy.insert_into_kad(
IN kad_name varchar(100), 
IN kad_link varchar(300),
IN kad_public_link varchar(300),
IN domain_id int(11), 
IN business_problem Integer,
OUT kad_id int(11))

BEGIN
insert into kads(kad_name,domain_id,kad_link,kad_link_public,RECURRING_BUS_PROBLEM_ID) 
values (kad_name,domain_id,kad_link,kad_public_link,business_problem);
select last_insert_id() into kad_id;
END $$
Delimiter ;

Delimiter $$
create procedure archemy.insert_into_kad_dim_area(
IN in_kad_id Integer, 
IN in_area_id Integer,
IN in_area_child_id Integer,
IN in_dimension_id Integer
)

BEGIN
insert into kad_dimensions_area(kad_id,dimension_id,area_id,area_parent_id) 
values (in_kad_id,in_dimension_id,in_area_child_id,in_area_id);
END $$
Delimiter ;



下载 jdk
C:\Program Files\Java\jdk1.7.0_79\

下载错了，要下载1.8.0
JAVA_HOME
C:\Program Files\Java\jdk1.7.0_80
C:\Program Files\Java\jdk1.7.0_80\bin






Run JDeveloper in studio mode and load the workspace: ArchNav\ArchNav
Application\AppArchemy.jws


Download the extension and then select HELP>CHECK FOR UPDATES and click Install
from Local File

restart


Creates new .war and .ear files

有很多bug

 Select glassfish-3.1.2-windows.exe (EN) and download it.
 
 
 首先下载了一个 JAVA RUNTIME




把全部都打开，然后把里面的文件放在最外面，是cmd解压的一种方式


Copy these two .jar files from the App directory into the
C:\glassfish3\glassfish\domains\domain1\lib directory also:


