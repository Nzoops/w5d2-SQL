
-- -- ALTER TABLE article
-- -- ADD FOREIGN KEY (author) 
-- -- REFERENCES user (name);

--PRAGMA foreign_keys = ON;

-- DROP TABLE article;

-- ------------------------------------
--CREATE THE TABLES

-- CREATE TABLE user (
--     id INTEGER PRIMARY KEY AUTOINCREMENT,
--     name TEXT
-- );

-- CREATE TABLE tag (
--     title TEXT PRIMARY KEY,
--     couleur TEXT 
-- );

-- CREATE TABLE category (
--     id INTEGER PRIMARY KEY AUTOINCREMENT,
--     title TEXT,
--     tag TEXT,
--     FOREIGN KEY (tag) REFERENCES tag(title)
-- );

-- CREATE TABLE article (
--     id INTEGER PRIMARY KEY AUTOINCREMENT,
--     author_id INTEGER,
--     category_id INTEGER,
--     title TEXT, 
--     content TEXT,
--     FOREIGN KEY (category_id) REFERENCES category(id)
--     FOREIGN KEY (author_id) REFERENCES user(id)
-- );

------------------------------------

-- DROP TABLE user

-------------------------------------
-- INSERT INTO article (author_id, category_id, title, content) VALUES (1, 1, 'sous le soleil', 'guide de la creme solaire sur la blockchain'); 
-- INSERT INTO category (title, tag) VALUES ('tech', 'jaune');
-- INSERT INTO user (name) VALUES ('Enzo');
-- INSERT INTO  user (name) VALUES ('Paul');
-- INSERT INTO category (title, tag) VALUES ('tech', 'Jaune")

SELECT *
FROM user
INNER JOIN article ON user.id = article.author_id;