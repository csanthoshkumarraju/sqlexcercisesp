# sqlexcercisesp
-- table for employee details
create table employeedetails(employeeid number not null primary key,employeename varchar2(40),employeedepartment varchar2(40),employeeage number,employeedoj date,employeeeducation varchar2(40))
insert into employeedetails values (1,'eleni','ioo',25,to_date('2021-01-21','yyyy-mm-dd'),'B.tech')
insert into employeedetails values (2,'jamal','itis',26,to_date('2022-11-21','yyyy-mm-dd'),'M.tech')
insert into employeedetails values (3,'wilfred','cbo',27,to_date('2021-12-21','yyyy-mm-dd'),'MBA')
insert into employeedetails values (4,'fred','it',27,to_date('2020-10-20','yyyy-mm-dd'),'MCA')
insert into employeedetails values (5,'angelica','cloud',29,to_date('2019-01-19','yyyy-mm-dd'),'degree')
select * from employeedetails order by employeeid asc;
-- table for employee company
create table employeecompany(employeeid number not null primary key,employeename varchar2(40),employeecompany varchar2(40),employeeworklocation varchar2(40),companyhead_quarters varchar2(40),company_CEO varchar2(40),company_CHAIRMAN varchar2(40));
insert into employeecompany values (1,'eleni','company1','kolkata','usa','anderson','jerome');
insert into employeecompany values (2,'jamal','company2','bangalore','india','Shane','shelly');
insert into employeecompany values (3,'Wilfred','company3','mumbai','uk','alAN','zane');
insert into employeecompany values (4,'fred','company4','delhi','australia','ramsey','donald');
insert into employeecompany values (5,'Angelina','company5','Chennai','France','andrews','olephia');
select * from employeecompany
-- create table employeeprojects
create table employeeprojects(employeeid number not null primary key,employeename varchar2(40),projectname varchar2(40),projectdomain varchar2(30),projectaccess varchar2(30),projectlocation varchar2(40),projectmanager varchar2(30),projectteamleader varchar2(30),projectsupervisor varchar2(30),employee_project_performance varchar2(30),project_status_complete_percentage number);
insert into employeeprojects values (1,'eleni','projectnumber1','python','pycharm','kolkata','stephen','marissa','jordan','excellent',90);
insert into employeeprojects values (2,'jamal','projectnumber2','java','eclipse','bangalore','alexis','vanessa','karen','good',80);
insert into employeeprojects values (3,'wilfred','projectnumber3','webdevelopment','reactjs','mumbai','debra','kristie','snyder','above average',70);
insert into employeeprojects values (4,'fred','projectnumber4','fullstack','django','delhi','nicole','jason','isaac','average',50);
insert into employeeprojects values (5,'angelica','projectnumber5','cloud','azure','chennai','mark','robin','jamie','worst',75);
select * from employeeprojects
--create table employee salary

create table employeesalary(employeeid number not null primary key,employeename varchar2(40),empbank varchar2(30),empacnumber number,empdayspaid number,empleavebalance number,emp_loc varchar2(30),empbranch varchar2(40),emptotearnigamt number,empdeductions number,empnetpat number);
insert into employeesalary values (1,'eleni','icici',123,31,3,'kolkata','candore',28000,3000,25000);
insert into employeesalary values (2,'jamal','canara',456,30,4,'banglore','whitefield',19000 ,2000,17000);
insert into employeesalary values (3,'wilfred','hdfc',789,28,1,'hyderabad','adibatla',27000 ,4000,23000);
insert into employeesalary values (4,'fred','sbi',321,30,2,'delhi','gurugon',30000 ,3000,27000);
insert into employeesalary values (5,'angelica','hsbc',654,27,0,'chennai','siruseri',40000 ,5000,35000);
select * from employeesalary order by employeeid asc;

-- we can alter or rename the colum names in two ways using rename and change
-- changing employee details table
-- rename multiple columns using single query
alter table employeedetails rename column employeeid to Employee_Id,rename column employeename to Employee_Name,rename column employeedepartment to Employee_Department,rename column employeeage to Employee_Age,
rename column employeedoj to Employee_DOJ,rename column employeeeducation to Employee_Education;
-- rename single column using rename
alter table employeedetails rename column employeeid to Employee_Id
alter table employeedetails rename column employeename to Employee_Name
alter table employeedetails rename column employeedepartment to Employee_Department
alter table employeedetails rename column employeeage to Employee_Age
alter table employeedetails rename column employeedoj to Employee_DOJ
alter table employeedetails rename column employeeeducation to Employee_Education

alter table employeecompany rename column employeeid to Employee_Id,rename column employeename to Employee_Name,rename column employeecompany to employee_company,rename column employeeworklocation to employee_work_location,
rename column companyhead_quarters to company_head_quarters;
-- rename single column using rename
alter table employeecompany rename column employeeid to Employee_Id
alter table employeecompany rename column employeename to Employee_Name
alter table employeecompany rename column employeecompany to employee_company
alter table employeecompany rename column employeeworklocation to employee_work_location
alter table employeecompany rename column companyhead_quarters to company_head_quarters
select * from employeecompany

alter table employeeprojects rename column employeeid to Employee_Id,rename column employeename to Employee_Name,rename column projectname to project_name,
rename column projectdomain to project_domain,rename column projectaccess to project_access,
rename column projectlocation to project_location,rename column projectmanager to project_manager,
rename column projectteamleader to project_team_leader,rename column projectsupervisor to project_supervisor ;
-- rename single column using rename
alter table employeeprojects rename column employeeid to Employee_Id
alter table employeeprojects rename column employeename to Employee_Name
alter table employeeprojects rename column projectname to project_name
alter table employeeprojects rename column projectdomain to project_domain
alter table employeeprojects rename column projectaccess to project_access
alter table employeeprojects rename column  projectlocation to project_location
alter table employeeprojects rename column projectmanager to project_manager
alter table employeeprojects rename column projectteamleader to project_team_leader
alter table employeeprojects rename column projectsupervisor to project_supervisor

alter table employeesalary rename column employeeid to Employee_Id,rename column employeename to Employee_Name,rename column empbank to employee_bank_name,
rename column empacnumber to employee_account_number,rename column empdayspaid to employee_days_paid,
rename column empleavebalance to employee_leave_balance,rename column emp_loc to employee_loc,
rename column empbranch to employee_branch,rename column emptotearnigamt to employee_total_earnig_amount 
rename column empdeductions to employee_salary_deductions,rename column empnetpat to employee_salary_net_pay_amount ;
-- rename single column using rename
alter table employeesalary rename column employeeid to Employee_Id
alter table employeesalary rename column employeename to Employee_Name
alter table employeesalary rename column empbank to employee_bank_name
alter table employeesalary rename column empacnumber to employee_account_number
alter table employeesalary rename column empdayspaid to employee_days_paid
alter table employeesalary rename column  empleavebalance to employee_leave_balance
alter table employeesalary rename column emp_loc to employee_loc
alter table employeesalary rename column empbranch to employee_branch
alter table employeesalary rename column emptotearnigamt to employee_total_earnig_amount
alter table employeesalary rename column empdeductions to employee_salary_deductions
alter table employeesalary rename column empnetpat to employee_salary_deductions

—joins s
SELECT employeedetails.Employee_Id,employeedetails.Employee_Name,employeedetails.Employee_Department ,
       employeedetails.Employee_Age,employeedetails.Employee_DOJ,employeedetails.Employee_Education,
       employeecompany.Employee_Id,employeecompany.Employee_Name,employeecompany.employee_company,
       employeecompany.employee_work_location,employeecompany.company_head_quarters,employeecompany.company_CEO,employeecompany.company_CHAIRMAN,
       employeeprojects.Employee_Id, employeeprojects.Employee_Name,employeeprojects.project_name,employeeprojects.project_domain,
       employeeprojects.project_access,employeeprojects.project_location,employeeprojects.project_manager,employeeprojects.project_team_leader,
       employeeprojects.project_supervisor,
       employeesalary.Employee_Id, employeesalary.Employee_Name,employeesalary.employee_bank_name,employeesalary.employee_account_number,
       employeesalary.employee_days_paid,employeesalary.employee_leave_balance,employeesalary.employee_loc,
       employeesalary.employee_branch,employeesalary.employee_total_earnig_amount,employeesalary.employee_salary_deductions,
        employeesalary.employee_salary_Net_pay_amount_total,
FROM employeedetails
INNER JOIN employeecompany ON employeedetails.Employee_Id = employeecompany.Employee_Id 
INNER JOIN employeeprojects ON employeecompany.Employee_Id  = employeeprojects.Employee_Id
INNER JOIN employeesalary ON employeeprojects.Employee_Id = employeesalary.Employee_Id;

