// creating table
CREATE TABLE Actor ( 
actID INT NOT NULL, 
actName VARCHAR(255) NOT NULL, 
CONSTRAINT pk_actor PRIMARY KEY (actID),
CONSTRAINT ck_actor UNIQUE (actName)); 
)

alter table Actor modify actID int auto_increment

Movie Table
CREATE TABLE Movie (
mvID INT NOT NULL,
actID INT NOT NULL,
mvTitle VARCHAR (255) NOT NULL,
mvPrice REAL NOT NULL,
mvGenre VARCHAR (255) NOT NULL,
mvYear INT NULL,
CONSTRAINT pk_mv PRIMARY KEY (mvID),
CONSTRAINT fk_mv_act FOREIGN KEY (actID) REFERENCES Actor (actID) 
ON UPDATE CASCADE 
ON DELETE CASCADE;
);

//correcting DELETE option
ALTER TABLE Movie DROP FOREIGN KEY fk_mv_act;

//adding correct reference options
ALTER TABLE Movie
 	ADD CONSTRAINT fk_mv_act
FOREIGN KEY (actID) 
REFERENCES Actor (actID); 
ON UPDATE CASCADE 
ON DELETE RESTRICT;
Populate Tables
//populate Actor

INSERT INTO Actor (actName) VALUES ('Arethan');
INSERT INTO Actor (actName) VALUES ('Barry Nelson');
INSERT INTO Actor (actName) VALUES ('Bullet');
INSERT INTO Actor (actName) VALUES ('Danie'l);
INSERT INTO Actor (actName) VALUES ('James Bond');
INSERT INTO Actor (actName) VALUES ('Jonny');
INSERT INTO Actor (actName) VALUES ('Laura');
INSERT INTO Actor (actName) VALUES ('Ryan');

//populate Movie

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = ''Arethan''), 'Die hard with a Vengeance', 11.74, 'Action');

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = ''Barry Nelson"), 'Black Snake Moan', 9.99, 'Adventure');

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = "Bullet"), 'Snake on a plane', 9.99, 'Sci-Fi');

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = ''Daniel''), 'Freeway of Love', 8.05,  'Drama');

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = "James Bond"), 'I knew you were waiting for me', 11.74, 'Comedy');


INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = "Jonny"), 'Black Panther', 9.99, 'Drama');

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = "Laura"), 'The Jungle Book', 9.99, 'Crime');

INSERT INTO Movie (actID, mvTitle, mvGenre, mvYear, mvPrice) VALUES
((SELECT actID from Actor WHERE actName = "Ryan"), 'Infinity War', 7.99, 'Horror');
