# Rails API Quiz

**Using whatever resources you like (e.g., Google, Stack Overflow, lectures, labs, notes, etc.), answer the following questions.**

1. Write the command to create a new Rails application in API mode with a Postgresql database.

```rails new project_name -g -d postgresql
```

2. What are 5 other options that can be passed in to the `rails new` command and what do they do?

```
```

3. What one line of code can be put into `routes.rb` to get all the RESTful routes for a given resource (e.g., dogs)?

```resources: dogs
```

4. In the context of API development, what is versioning? How do we implement versioning in a Rails API?

```
```

5. What is serialization in reference to a Rails API?

```
```

6. Imagine a dog walking domain in which a walker has many dogs. Write the `index` action from the `WalkersController`. Remember, your endpoint should return JSON.

```def index
      walkers = Walkers.all

      render json: walkers
   end
```

7. Change the code from the question above so that the walkers' dogs get embedded in the JSON being returned from the `index` endpoint.

```
```

8. Again, change the code above to exclude the timestamps from the data being returned in the JSON.

```def index
      walkers = Walkers.all

      render json: walkers except: [:updated-at, :created-at]
   end
```

9. What does CORS mean? Why do we have to think about it when making an API?

```Cross-Origin Resource Sharing. It determines who is allowed access to our database.
```

10. What changes do we have to make in our application to allow CORS?

```Make sure its in the Gemfile, and run bundle update/install. Then modify the code in cors.rb to 
   allow access. "*" is the origins that allow full access.
```

11. In our dog walking app, what needs to be added to the following class to allow method calls like `Dog.create(name: "Neikko", breed: "mostly rat", age: 13)` and `Dog.find_by(name: "Neikko")` to function properly?

```
class Dog < ApplicationRecord
end
```

```
```




