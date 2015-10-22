# Rails

Quick note

Reset primary key sequence!
```ruby ActiveRecord::Base.connection.tables.each { |t| ActiveRecord::Base.connection.reset_pk_sequence!(t) }```
