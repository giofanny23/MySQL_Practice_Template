# MySQL_Practice_Sample

Repository to try to make, alter, join, and other in MySQL

===STEP 1 CREATE THE DATABASE===
===HOW TO MAKE THE DATABASE IN MySQL===
===FORMULA TO CREATE DATABASE: CREATE DATABASE name_of_database; (database name must be in lower case without the space)
===EXAMPLE TO MAKE DATABASE: CREATE DATABASE liverpool;
===EVERY syntax on MySQL end by ; to execute 

===STEP 2 USE THE DATABASE===
===WE MUST CHOOSE AND USE WHAT DATABASE TO USE IN OUR PROJECT
===WE ALREADY MADE THE DATABASE IN STEP 1, SO WE USE IT
===FORMULA TO USE THE DATABASE: USE name_of database
===EXAMPLE: USE liverpool; 
===AFTER WE USE THE DATABASE, ALL PROCESS WILL BE RECORDED ON IT


===STEP 3 TRY TO CREATE TABLE IN DATABASE===

CREATE TABLE player(
player_id INT NOT NULL,
name VARCHAR(30) NOT NULL,
position_code VARCHAR(5) NOT NULL,
email VARCHAR(30) NOT NULL,
birth_place VARCHAR(15) NOT NULL,
birth_date DATE NOT NULL,
join_date DATE,
PRIMARY KEY(position_code)
) ENGINE = InnoDB;

===STEP 4 INSERT VALUES ON THE TABLE===

INSERT INTO player VALUES
(202401001,'Jurgen Klopp','C', 'thenormalone@gmail.com','Stuttgart', '2004-06-16','2024-08-01'),
(202401002,'Allison Becker','GK','AB01@gmail.com','Brasilia', '2004-01-10','2024-08-01'),
(202401003,'Trent Alexander Arnold','DF', 'iamTAA66@gmail.com','Liverpool', '2004-12-11','2024-08-01'),
(202401004,'Virgil Van Dijck', 'DF', 'calmasyoulike@gmail.com','Suriname', '2003-05-23','2024-08-01'),
(202401005,'Joel Matip', 'DF', 'matipjoel@gmail.com','Medan', '2002-04-14','2024-08-01'),
(202401006,'Arne Slot', 'C', 'slot78@gmail.com','Bergentheim', '2002-09-17','2024-08-01'),
(202401007,'Andy Robertson','DF', 'robbo26@gmail.com','Glasgow', '2004-03-11','2024-08-01'),
(202401008,'Mohammed Salah','AF', 'runonthewings@gmail.com','Nagrig', '2004-06-15','2024-08-01'),
(202401009,'Darwin Nunez','AF', 'darwizzy@gmail.com','Artigas', '2004-06-24','2024-08-01'),
(202401010,'Luis Diaz','AF', 'luisdiaz07@gmail.com','Barrancas', '2004-01-13','2024-08-01'),
(202401011,'Dominik Szoboszlai','MF', 'szobosz@gmail.com','Szekesfehevar', '2004-10-25','2024-08-01'),
(202401012,'Wataru Endo', 'MF', 'endo03@gmail.com','Totsuka Ward', '2004-02-09','2024-08-01'),
(202401013,'Cody Gakpo','AF', 'gakpo18@gmail.com','Eindhoven', '2004-05-07','2024-08-01'),
(202401014,'Alexis Mac Allister','MF', 'macca10@gmail.com','Santa Rosa', '2004-12-24','2024-08-01'),
(202401015,'Diogo Jota','AF', 'diogoal20@gmail.com','Porto', '2004-12-04','2024-08-01'),
(202401016,'Harvey Elliot','AF', 'harvey19@gmail.com','Chertsey', '2004-04-04','2024-08-01'),
(202401017,'Fabio Carvalho','AF', 'FabioC@gmail.com','Torres Vedras', '2004-08-30','2024-08-01'),
(202401018,'Conor Bradley','DF', 'bradley84@gmail.com','Castlederg', '2004-06-09','2024-08-01'),
(202401019,'Sepp Van den Berg','DF', 'SVdB@gmail.com','Zwolle', '2004-12-20','2024-08-01'),
(202401020,'Jayden Danns','DF', 'danss76@gmail.com','Liverpool', '2004-01-16','2024-08-01'),
(202401021,'Caoiminhin Kelleher','GK', 'kelleher62@gmail.com','Cork', '2004-11-23','2024-08-01'),
(202401022,'Stefan Bajcetic','MF', 'bajecetic43@gmail.com','Vigo', '2004-10-22','2024-08-01'),
(202401023,'Ibrahima Konate','DF', 'konate05@gmail.com','Paris', '2004-05-25','2024-08-01'),
(202401024,'Joe Gomez','DF', 'gomez02@gmail.com','Catford', '2004-05-23','2024-08-01'),
(202401025,'Ryan Gravenberch','MF', 'graven38@gmail.com','Amsetrdam', '2004-05-16','2024-08-01'),
(202401026,'Curtis Jones','MF', 'jones17@gmail.com','Liverpool', '2004-01-30','2024-08-01'),
(202401027,'Jarell Amorin Quansah','DF', 'amorinQ7876@gmail.com','Warrington', '2004-01-29','2024-08-01'),
(202401028,'Ben Doak','DF', 'bendoak50@gmail.com','Dairy', '2004-11-11','2024-08-01'),
(202401029,'Kostantinos Tsimikas','DF', 'tsimi21@gmail.com','Tesalonika', '2004-05-12','2024-08-01'),
(202401030,'Vitezslav Jaros','GK', 'vitesz23@gmail.com','Pribram', '2004-07-23','2024-08-01'),
(202401031,'Boby Clark','MF', 'clark32@gmail.com','Epsom', '2004-02-07','2024-08-01'),
(202401032,'Rhys William','DF', 'william88@gmail.com','Preston', '2004-02-03','2024-08-01'),
(202401033,'Nathaniel Phillips','DF', 'np2323@gmail.com','Bolton', '2004-03-21','2024-08-01'),
(202401034,'James McConnell', 'DF','jamesmccinnel533@gmail.com','Pribram', '2004-09-13','2024-08-01'),
(202401035,'Giofanny Sigalingging','MF', 'giofannysigalingging23@gmail.com','Sidikalang', '2004-12-23','2024-08-01');

===CREATE ANOTHER TABLE===
CREATE TABLE training_code(
player_id INT NOT NULL,
position VARCHAR(20) NOT NULL,
training_code VARCHAR(10) NOT NULL,
PRIMARY KEY(player_id, training_code)
) ENGINE = InnoDB;

===INSERT VALUES===
INSERT INTO training_code VALUES
(202401001,'Coach','T001'),
(202401002,'Goal Keeper','T002'),
(202401003,'Defensive Fielder','T003'),
(202401004,'Defensive Fielder','T004'),
(202401005,'Defensive Fielder','T005'),
(202401006,'Coach', ,'T006'),
(202401007,'Defensive Fielder','T007'),
(202401008,'Attacking Fielder','T008'),
(202401009,'Attacking Fielder','T009'),
(202401010,'Attacking Fielder','T010'),
(202401011,'Mid Fielder','T011'),
(202401012,'Mid Fielder','T012'),
(202401013,'Attacking Fielder','T013'),
(202401014,'Mid Fielder','T014'),
(202401015,'Attacking Fielder','T015'),
(202401016,'Attacking Fielder','T016'),
(202401017,'Attacking Fielder','T017'),
(202401018,'Defensive Fielder','T018'),
(202401019,'Defensive Fielder','T019'),
(202401020,'Defensive Fielder','T020'),
(202401021,'Attacking Fielder','T021'),
(202401022,'Mid Fielder','T022'),
(202401023,Defensive Fielder,'T023'),
(202401024,Defensive Fielder','T024'),
(202401025,'Mid Fielder','T025'),
(202401026,'Mid Fielder','T026'),
(202401027,'Defensive Fielder','T027'),
(202401028,'Defensive Fielder','T028'),
(202401029,'Defensive Fielder','T029'),
(202401030,'Goal Keeper','T030'),
(202401031,'Mid Fielder','T031'),
(202401032,'Defensive Fielder','T032'),
(202401033,'Defensive Fielder','T033'),
(202401034,'Defensive Fielder','T034'),
(202401035,'Mid Fielder','T035');


===CREATE ANOTHER TABLE===
CREATE TABLE training_activity (
training_code VARCHAR(10) NOT NULL,
activity_1 VARCHAR(30) NOT NULL,
activity_2 VARCHAR(30) NOT NULL,
activity_3 VARCHAR(30) NOT NULL,
PRIMARY KEY(training_code)
) ENGINE = InnoDB

===INSERT THE VALUES===
INSERT INTO training_activity VALUES
('T001', 'Communication', 'Physiology', 'Tactical'),
('T002', 'Reflex', 'Catching Ball', 'Saving Ball'),
('T003', 'Tackling', 'Body Charge', 'Heading'),
('T004', 'Tackling', 'Body Charge', 'Heading'),
('T005', 'Tackling', 'Body Charge', 'Heading'),
('T006', 'Communication', 'Physiology', 'Tactical'),
('T007', 'Tackling', 'Body Charge', 'Heading'),
('T008', 'Shooting', 'Speed', 'Positioning'),
('T009', 'Shooting', 'Speed', 'Positioning'),
('T010', 'Shooting', 'Speed', 'Positioning'),
('T011', 'Passing', 'Dribbling', 'Positioning'),
('T012', 'Passing', 'Dribbling', 'Positioning'),
('T013', 'Shooting', 'Speed', 'Positioning'),
('T014', 'Passing', 'Dribbling', 'Positioning'),
('T015', 'Shooting', 'Speed', 'Positioning'),
('T016', 'Shooting', 'Speed', 'Positioning'),
('T017', 'Shooting', 'Speed', 'Positioning'),
('T018', 'Tackling', 'Body Charge', 'Heading'),
('T019', 'Tackling', 'Body Charge', 'Heading'),
('T020', 'Tackling', 'Body Charge', 'Heading'),
('T021', 'Shooting', 'Speed', 'Positioning'),
('T022', 'Passing', 'Dribbling', 'Positioning'),
('T023', 'Tackling', 'Body Charge', 'Heading'),
('T024', 'Tackling', 'Body Charge', 'Heading'),
('T025', 'Passing', 'Dribbling', 'Positioning'),
('T026', 'Passing', 'Dribbling', 'Positioning'),
('T027', 'Tackling', 'Body Charge', 'Heading'),
('T028', 'Tackling', 'Body Charge', 'Heading'),
('T029', 'Tackling', 'Body Charge', 'Heading'),
('T030', 'Reflex', 'Catching Ball', 'Saving Ball'),
('T031', 'Passing', 'Dribbling', 'Positioning'),
('T032', 'Tackling', 'Body Charge', 'Heading'),
('T033', 'Tackling', 'Body Charge', 'Heading'),
('T034', 'Tackling', 'Body Charge', 'Heading'),
('T035', 'Passing', 'Dribbling', 'Positioning');

===NEXT STEP IS HOW TO MAKE CONNECTIVITY FROM EACH TABLE TO ANOTHER TABLE===
===WE ALREADY MADE THE PRIMARY KEY IN OUR TABLE===
===PRIMARY KEY is THE KEY TO CONNECT THE TABLE===

===FORMULA TO ADD THE CONNECTIVITY===
ALTER TABLE player
ADD FOREIGN KEY (player_id) REFERENCES training_code(player_id); #this connection is connection between table player and training_code
==syntax ALTER allows us to change the table even though the table has been created

# MAKE ANOTHER CONNECTION
ALTER TABLE training_code
ADD FOREIGN KEY(training_code) REFERENCES training_activity(training_code); #this connection is connection between table training_code and training_activity

===NEXT STEP IS HOW TO JOIN THE TABLE===
==== FORMULA TO JOIN THE TABLE ====
SELECT * FROM player
JOIN training_code ON (player.player_id = training_code.player_id)
JOIN training_activity ON (training_activity.training_code = training_code.training_code);

===sign * means all the column will be displayed
===YOU CAN CHOOSE WHAT COLUMN TO SELECT, example:
SELECT name, position, training_ activity from player
JOIN training_code ON (player.player_id = training_code.player_id)
JOIN training_activity ON (training_activity.training_code = training_code.training_code);

# Sytax:
=== CREATE DATABASE >>> to make database
=== USE DATABASE >>> to use database
=== CREATE TABLE >>>  to create table
=== ALTER TABLE >>> to change the table
=== PRIMARY KEY >>> to make the key velues on the table
=== FOREIGN KEY (...) REFERENCES (...) >>> to make connection
=== JOIN (.....) ON (....) >>> to join some table
