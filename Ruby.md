# Ruby

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