## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
AR is a liason between your models and database(s); It is mostly a DSL (domain-specific language) that allows you to write Ruby code to access & manipulate data by translating it to SQL. It also has many methods built-in that are accessible when you inherit from it & process data calculations about 1000x faster than Ruby. :)

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
#all
#find(<id>)
#find_by(<attribute>: <attr_val>)
#sum(<attribute>)
You have access because you inherit from Active Record which has 100s!

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
Team.find(4)
Owner(Team.find(4).owner_id)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Team.find(4).owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
Students have_many :teachers
Teachers have_many :students
see bottom for schema xml

6. Define foreign key, primary key, and schema.
primary key is the unique identifier for an instance in a table (:id)
foreign key is the primary key of another, related table
schema has two meanings: either the layout of tables and relationships in your projects or the list of tables and their attributes and attribute types (and defaults and foreign keys, etc.) in your database

7. Describe the relationship between a foreign key on one table and a primary key on another table.
a foreign key is located on the "many" table and connects the table that it's on to the table that is the "one" table, where it is the uniquie identifier (primary key) 

8. What are the parts of an HTTP response?
Header(with Response Code)
Body

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
#average - it simply takes the average of whatever attribute column (or other collection) you pass in
#order - orders your query based on whatever arguments or attributes you pass in
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
rake db:migrate - migrates your migration actions to the database and updates your schema
rake db:seed - seeds your database with data!
3. What two columns does `t.timestamps null: false` create in our database?
created_at
updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
one-to-many (hopefully, for their sake!)

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
connect the primary key from the schools table as a foreign key in the teachers table

6. Give an example of when you might want to store information besides ids on a join table.
when there are attributes created by the relationship (enrollments for students-courses could also have course_number)

7. Describe and diagram the relationship between patients and doctors.
many-to-many; they would need a join table

8. Describe and diagram the relationship between museums and original_paintings.
one-to-many; the primary key from original_paintings would become the foreign_key in museums

9. What could you see in your code that would make you think you might want to create a partial?
repetition!! dry it out.



<?xml version="1.0" encoding="utf-8" ?>
<!-- SQL XML created by WWW SQL Designer, https://github.com/ondras/wwwsqldesigner/ -->
<!-- Active URL: http://ondras.zarovi.cz/sql/demo/ -->
<sql>
<datatypes db="mysql">
	<group label="Numeric" color="rgb(238,238,170)">
		<type label="Integer" length="0" sql="INTEGER" quote=""/>
	 	<type label="TINYINT" length="0" sql="TINYINT" quote=""/>
	 	<type label="SMALLINT" length="0" sql="SMALLINT" quote=""/>
	 	<type label="MEDIUMINT" length="0" sql="MEDIUMINT" quote=""/>
	 	<type label="INT" length="0" sql="INT" quote=""/>
		<type label="BIGINT" length="0" sql="BIGINT" quote=""/>
		<type label="Decimal" length="1" sql="DECIMAL" re="DEC" quote=""/>
		<type label="Single precision" length="0" sql="FLOAT" quote=""/>
		<type label="Double precision" length="0" sql="DOUBLE" re="DOUBLE" quote=""/>
	</group>

	<group label="Character" color="rgb(255,200,200)">
		<type label="Char" length="1" sql="CHAR" quote="'"/>
		<type label="Varchar" length="1" sql="VARCHAR" quote="'"/>
		<type label="Text" length="0" sql="MEDIUMTEXT" re="TEXT" quote="'"/>
		<type label="Binary" length="1" sql="BINARY" quote="'"/>
		<type label="Varbinary" length="1" sql="VARBINARY" quote="'"/>
		<type label="BLOB" length="0" sql="BLOB" re="BLOB" quote="'"/>
	</group>

	<group label="Date &amp; Time" color="rgb(200,255,200)">
		<type label="Date" length="0" sql="DATE" quote="'"/>
		<type label="Time" length="0" sql="TIME" quote="'"/>
		<type label="Datetime" length="0" sql="DATETIME" quote="'"/>
		<type label="Year" length="0" sql="YEAR" quote=""/>
		<type label="Timestamp" length="0" sql="TIMESTAMP" quote="'"/>
	</group>
	
	<group label="Miscellaneous" color="rgb(200,200,255)">
		<type label="ENUM" length="1" sql="ENUM" quote=""/>
		<type label="SET" length="1" sql="SET" quote=""/>
		<type label="Bit" length="0" sql="bit" quote=""/>
	</group>
</datatypes><table x="208" y="107" name="students">
<row name="id" null="1" autoincrement="1">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<row name="name" null="1" autoincrement="0">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<row name="sparkles" null="1" autoincrement="0">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<key type="PRIMARY" name="">
<part>id</part>
</key>
</table>
<table x="616" y="94" name="teachers">
<row name="id" null="1" autoincrement="1">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<row name="name" null="1" autoincrement="0">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<row name="favorite_fruit" null="1" autoincrement="0">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<key type="PRIMARY" name="">
<part>id</part>
</key>
</table>
<table x="377" y="247" name="students_teachers">
<row name="id" null="1" autoincrement="1">
<datatype>INTEGER</datatype>
<default>NULL</default></row>
<row name="id_teachers" null="1" autoincrement="0">
<datatype>INTEGER</datatype>
<default>NULL</default><relation table="teachers" row="id" />
</row>
<row name="id_students" null="1" autoincrement="0">
<datatype>INTEGER</datatype>
<default>NULL</default><relation table="students" row="id" />
</row>
<key type="PRIMARY" name="">
<part>id</part>
</key>
</table>
</sql>

