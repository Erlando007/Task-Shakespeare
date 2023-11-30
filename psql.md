###                      1

select * from wordform limit 10;

###                      2

select * from wordform where plaintext ILIKE 'a%';

###                      3

select title, genretype from work where genretype = 'p';

###                      4

select avg(totalparagraphs) from work where genretype = 't';

###                      5

select title from work where totalwords > (select avg(totalwords) from work);

###                      6

SELECT character.charname, speechcount, work.title FROM character LEFT JOIN character_work ON character.charid = character_work.charid LEFT JOIN work ON character_work.workid = work.workid

###                      7

select round(avg(speechcount)), work.title from character join character_work on character.charid = character_work.charid join work on character_work.workid = work.workid where work.title = 'Romeo and Juliet' group by work.title;

###                      8

select section, sum(wordcount) as sum from paragraph group by section;

###                      9

select charname, speechcount from character where speechcount between 15 and 30;

###                      10

select title, year from work where year between 1601 and 1699

###                      11

select longtitle from work where longtitle like '%the%';

###                      12

select distinct section from paragraph;

###                      13

select chapterid, description, title from chapter,work where chapter.workid= work.workid;

###                      14

select paragraphnum, character.charname, character.speechcount from paragraph join character on paragraph.charid = character.charid;

###                      15

select paragraphnum, title, work.year from paragraph join work on paragraph.workid = work.workid;