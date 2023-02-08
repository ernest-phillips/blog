---
title: "Understanding Instance Variables in Ruby"
date: 2023-02-08
draft: false
---

Instance variables in Ruby are variables that belong to a specific instance or object of a class.

Ruby instances are objects that are created from a class. 

```ruby
class Person
  def initialize
    @name = "John Doe"
  end
end
```

By understanding and using instance variables in Ruby, you can create powerful and flexible classes that can be used to represent and interact with real-world objects.

A Ruby object is an instance of a class in Ruby. It is an entity that contains data and behaviors that can be manipulated and interacted with. Objects can be created from a class to represent real-world objects, such as people, places, or things. Each object is unique and has its own set of data and behaviors.

To define an instance variable in Ruby, you use the `@` symbol followed by the name of the instance variable. For example, if you wanted to create an instance variable to store the name of a person, you would do the following:

```ruby
@name = "John Doe"

```

To access an instance variable, you use the same `@` symbol followed by the name of the instance variable. For example, if you wanted to access the name of a person, you would do the following:

```ruby
puts @name
#=> "John Doe"

```

Instance variables can be used to store information associated with an instance of a class. They can also be used to communicate between methods in a class. For example, if you had a class that had two methods, you could use an instance variable to store information in one method and then access that information in the other method.

Instance variables can also be used to set default values for a class. For example, if you had a class that had a `name` instance variable, you could set the default value of `name` to `"John Doe"` like this:

```ruby
def initialize
  @name = "John Doe"
end

```

This would ensure that all instances of the class would have the `name` instance variable set to `"John Doe"` by default.

Instance variables can also be used to create class methods. For example, if you had a `Person` class, you could create a class method to get the name of a person like this:

```ruby
def self.get_name
  @name
end

```

This class method could then be used like this:

```ruby
Person.get_name
#=> "John Doe"

```

Class methods that use instance variables are a great way to easily access the data stored in an instance of a class.

## What instance variables are NOT for

It is important to understand when not to use Ruby instance variables. Instance variables should not be used to store global state, as they are only available within the scope of a particular instance of a class. This means that if you want to access data from multiple objects, instance variables will not be the right solution. Additionally, instance variables should not be used to store data that is not related to a particular instance of a class. This can lead to confusion and unexpected results.