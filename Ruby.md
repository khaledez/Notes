# Ruby

## Ruby Development Ecosystem

- Bundler: Dependency Management
- RubyGems: Package Manager
- Rake: Make-like build/automation system
- Rack: Webserver Interface
- Spring & Guard: Speed development and testing

## Rails Undoing changes
1. Rollback db changes if `db:migrate` was called: `rails db:rollback`
1. Destroy generated files by calling: `rails destroy [Generated section] [name]`.  
examples:
```
rails destroy scaffold Users
rails destroy controller StaticPages
rails destroy model Account
```


## Ruby Console (irb)

Add these lines to `~/.irbrc`  
```ruby
require 'irb/completion'
require 'what_methods'
require 'pp'

IRB.conf[:AUTO_INDENT]=true

class Object
  def local_methods
    (methods - Object.instance_methods).sort
  end
end
```

Inspiration from: http://drnicwilliams.com/2006/10/12/my-irbrc-for-consoleirb/