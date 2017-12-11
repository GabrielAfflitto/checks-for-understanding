## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  Active Record is a ORM which allows us to interact with a database more easily by providing methods
  that act as SQL queries
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
  I can call many ActiveRecord methods such as .join, .where, .group, etc

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
  Team.all.where(:id = 4)
4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  Team.find(params[:owner_id])
5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  student belongs_to teacher
  teachers have_many students
6. Define foreign key, primary key, and schema.
  The primary key of a table is the id attribute by which the table is identified e.g. (students: {id:, name:, age:}, teachers: {id:, name:, age:})
  the foreign key of a table refers to the primary key in another table in a one-to-many relationship, which sets up the has_many/belongs_to relationship between two tables e.g.(students: {id:, name:, age:, teacher_id:}, teachers: {id:, name:, age:}) The teacher_id: inside of students is the foreign key which refers to the key id: in the teachers table.
  the Schema is the visual representation of the database which is updated with every mirgation
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  see question 6
8. What are the parts of an HTTP response?
  the status line, headers, and the body

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What two columns does `t.timestamps null: false` create in our database?
  the columns created by t.timestamps are the created_at: and updated_at: columns, which track when the object has been created and updated
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  teachers have_many students
  student belongs_to teachers
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
6. Give an example of when you might want to store information besides ids on a join table.
7. Describe and diagram the relationship between patients and doctors.
8. Describe and diagram the relationship between museums and original_paintings.
9. What could you see in your code that would make you think you might want to create a partial?
  forms
