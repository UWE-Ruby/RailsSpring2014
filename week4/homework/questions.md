```
Reading:
  Chapter 6: Sections 4-6
  Chapter 7: All
  Chapter 9: Section 1
  Chapter 11: Sections 9-11

Code:
  Add 2 relationships to your app:
    1. Has Many (one-to-many)
    2. Has Many Through (many-to-many)
  Add 2 named scopes
```

# Questions:

1. What is ActiveRecord and why is it useful?
ActiveRecord is an ORM. It is useful for making it easier to do common database tasks in an application.

# 2. What problems could happen if you change a migration file after you have run it and committed it to github? (list 2)

1. You will need to rollback the migration before your re-run the changed migration. If you don't rollback, then rails will not re-run the migration for you. 
2. If you have committed it and someone else has run your migration, that person will need to rollback. If you don't inform them do the same, your partner's database will not reflect the migrations.  (http://guides.rubyonrails.org/migrations.html#changing-existing-migrations)

# 3. What problems can you run into with the Rails has_and_belongs_to_many method? (list 2)

This relation just creates a table with two fields: one for each table in the relation. If you want other information on the relation, this method wont support your adding that in. On the other hand, if you use an intervening model, you can put other fields on it, such as a relation id, or a date added.

# 4. How is Rails form_for object oriented?

form_for can create a form for use in a view out of a model object. It automatically creates the form and sets up the behavior of the form based on the object passed to it.

#5. How would I use postgres in production and sqlite for development? What files would I change and how would I change them?

You would change the Gemfile to include sqlite gem in dev and test, while pg will be included in production. You would need to set up each database in config/database.yml Then you should be set.

#6. What is the seeds file? How do I run it?

The seeds file will seed your database with intial data. It is run automatically when you call rake db:reset or rake db:seed

### Link to code on Github:

https://github.com/psytau/week2_rails/tree/week4

http://how-to-listen-to-podcasts.herokuapp.com/
