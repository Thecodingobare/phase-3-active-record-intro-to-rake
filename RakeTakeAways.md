### Define Rake File

```rb
desc 'all the greerings'

task :hello do 
puts "Hello from Rake"
end
```

### Now if we run rake -T in the terminal we should see:

```rb
$ rake -T
rake hello    #outpus all the greetings
```

### Namespacing Rake Tasks

```rb
namespace :greeting do

desc 'outputs hello to the terminal'
    task :hello do 
    puts "hello from Rake!"
    end

    desc 'outputs ohoro waku to the terminal'
    task :ohoro do
    puts "Ohoro waku wa nyina!"
    end

end
```

### Now to use either of our ruby tasks, we use the following syntax

```rb
$ rake greeting:hello

hello from Rake!

$ rake greeting:ohoro

Ohoro waku wa nyina!
```

### bundle exec rake
#### One common issue is that you should run Rake tasks using the following command always.

```rb
$ bundle exec rake greeting:ohoro

Ohoro waku wa nyina!
```

### Common Rake Tasks

####  While in developing Sinatra and Rails web applications, you'll begin to use some common Rake tasks that handle certain database-related jobs.
___
### rake db:migrate
___


