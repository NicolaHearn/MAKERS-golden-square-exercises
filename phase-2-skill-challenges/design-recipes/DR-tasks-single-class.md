# Tasks Design Recipe

## 1. Problem

As a user
So that I can keep track of my tasks
I want to check if a text includes the string #TODO

As a user
So that I can keep track of my tasks
I want a program that I can add todo tasks to and see a list of them.

As a user
So that I can focus on tasks to complete
I want to mark tasks as complete and have them disappear from the list.

## 2. Class Interface

_Include the name of the method, its parameters, return value, and side effects._

```ruby
class TodoList
  def initialize
  end

  def add(task) # task is a string representing an instruction
    # Return nothing
  end

  def list()
    # Returns a list of the tasks added as strings
    # Except the completed ones
  end

  def complete(task) # task is a string representing a task to mark complete
    # Returns nothing
    # Fails is the task doesn't exist
  end
end
```

## 3. Examples as Tests

_Make a list of examples of what the method will take and return._

```ruby
# 1
todo_list = TodoList new 
todo_list.list # => []

# 2
todo_list = TodoList new 
todo_list.add('Book haircut')
todo_list.list # => ['Book haircut']

# 3
todo_list = TodoList new 
todo_list.add('Book haircut')
todo_list.add('Wash the windows')
todo_list.list # => ['Book haircut', 'Wash the windows']

# 4
todo_list = TodoList new 
todo_list.add('Book haircut')
todo_list.add('Wash the windows')
todo_list.complete('Wash the windows')
todo_list.list # => ['Book haircut']

# 4
todo_list = TodoList new 
todo_list.add('Book haircut')
todo_list.add('Wash the windows')
todo_list.complete('Wash the windows')
todo_list.list # => fails "No such task"
```

_Encode each example as a test. You can add to the above list as you go._

## 4. Implement the Behaviour

_After each test you write, follow the test-driving process of red, green, refactor to implement the behaviour._
