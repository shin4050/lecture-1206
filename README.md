# テクノロジー（藤原）12/6授業

## Bashの実行ログ

```
shin4050:~/workspace $ cd lecture-1206/asagao/
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rails g model member
      invoke  active_record
      create    db/migrate/20171206012410_create_members.rb
      create    app/models/member.rb
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rake db:migrate
== 20171206012410 CreateMembers: migrating ====================================
-- create_table(:members)
   -> 0.0007s
== 20171206012410 CreateMembers: migrated (0.0008s) ===========================

shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > Member.count
   (0.2ms)  SELECT COUNT(*) FROM "members"
 => 0 
2.4.0 :002 > member=Member.new
 => #<Member id: nil, created_at: nil, updated_at: nil> 
2.4.0 :003 > member.number=1
NoMethodError: undefined method `number=' for #<Member id: nil, created_at: nil, updated_at: nil>
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activemodel-4.2.10/lib/active_model/attribute_methods.rb:433:in `method_missing'
        from (irb):3
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :004 > member.number = 1
NoMethodError: undefined method `number=' for #<Member id: nil, created_at: nil, updated_at: nil>
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activemodel-4.2.10/lib/active_model/attribute_methods.rb:433:in `method_missing'
        from (irb):4
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :005 > member.name=1
NoMethodError: undefined method `name=' for #<Member id: nil, created_at: nil, updated_at: nil>
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activemodel-4.2.10/lib/active_model/attribute_methods.rb:433:in `method_missing'
        from (irb):5
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :006 > member.number = 1
NoMethodError: undefined method `number=' for #<Member id: nil, created_at: nil, updated_at: nil>
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/activemodel-4.2.10/lib/active_model/attribute_methods.rb:433:in `method_missing'
        from (irb):6
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :007 > 
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rake db:migrate:reset
== 20171206012410 CreateMembers: migrating ====================================
-- create_table(:members)
   -> 0.0009s
== 20171206012410 CreateMembers: migrated (0.0010s) ===========================

shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rake db:migrate
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > member = Member.new
 => #<Member id: nil, number: nil, name: nil, full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: nil, updated_at: nil> 
2.4.0 :002 > member.number = 1
 => 1 
2.4.0 :003 > member.name = "Taro"
 => "Taro" 
2.4.0 :004 > member.save
   (0.2ms)  begin transaction
  SQL (0.5ms)  INSERT INTO "members" ("number", "name", "created_at", "updated_at") VALUES (?, ?, ?, ?)  [["number", 1], ["name", "Taro"], ["created_at", "2017-12-06 01:51:23.539860"], ["updated_at", "2017-12-06 01:51:23.539860"]]
   (8.1ms)  commit transaction
 => true 
2.4.0 :005 > Member.first
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 01:51:23", updated_at: "2017-12-06 01:51:23"> 
2.4.0 :006 > pp Member.first
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
#<Member:0x00000004988510
 id: 1,
 number: 1,
 name: "Taro",
 full_name: nil,
 email: nil,
 birthday: nil,
 gender: 0,
 administrator: false,
 created_at: Wed, 06 Dec 2017 10:51:23 JST +09:00,
 updated_at: Wed, 06 Dec 2017 10:51:23 JST +09:00>
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 01:51:23", updated_at: "2017-12-06 01:51:23"> 
2.4.0 :007 > member = Member.first
  Member Load (0.4ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 1, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 01:51:23", updated_at: "2017-12-06 01:51:23"> 
2.4.0 :008 > member.number = 41
 => 41 
2.4.0 :009 > member.save
   (0.2ms)  begin transaction
  SQL (0.5ms)  UPDATE "members" SET "number" = ?, "updated_at" = ? WHERE "members"."id" = ?  [["number", 41], ["updated_at", "2017-12-06 01:53:23.529998"], ["id", 1]]
   (18.1ms)  commit transaction
 => true 
2.4.0 :010 > Member.first
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 41, name: "Taro", full_name: nil, email: nil, birthday: nil, gender: 0, administrator: false, created_at: "2017-12-06 01:51:23", updated_at: "2017-12-06 01:53:23"> 
2.4.0 :011 > ezit
NameError: undefined local variable or method `ezit' for main:Object
Did you mean?  exit
        from (irb):11
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :012 > exit
shin4050:~/workspace/lecture-1206/asagao (master) $ mkdir -p db/seeds/development
shin4050:~/workspace/lecture-1206/asagao (master) $ touch db/seeds/development/members.rb
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rake db:reset
-- create_table("members", {:force=>:cascade})
   -> 0.0175s
-- initialize_schema_migrations_table()
   -> 0.0406s
-- create_table("members", {:force=>:cascade})
   -> 0.0092s
-- initialize_schema_migrations_table()
   -> 0.0148s
Creating members...
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rake db:seed
Creating members...
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > Member.first
  Member Load (0.2ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
 => #<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24"> 
2.4.0 :002 > pp Member.first
  Member Load (0.3ms)  SELECT  "members".* FROM "members"  ORDER BY "members"."id" ASC LIMIT 1
#<Member:0x000000049d9a78
 id: 1,
 number: 10,
 name: "Taro",
 full_name: "佐藤 太郎",
 email: "Taro@example.com",
 birthday: Tue, 01 Dec 1981,
 gender: 0,
 administrator: true,
 created_at: Wed, 06 Dec 2017 11:02:24 JST +09:00,
 updated_at: Wed, 06 Dec 2017 11:02:24 JST +09:00>
 => #<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24"> 
2.4.0 :003 > exit
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rails db
SQLite version 3.8.2 2013-12-06 14:53:30
Enter ".help" for instructions
Enter SQL statements terminated with a ";"
sqlite> .table
members            schema_migrations
sqlite> .tables
members            schema_migrations
sqlite> .schema members
CREATE TABLE "members" ("id" INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL, "number" integer NOT NULL, "name" varchar NOT NULL, "full_name" varchar, "email" varchar, "birthday" date, "gender" integer DEFAULT 0 NOT NULL, "administrator" boolean DEFAULT 'f' NOT NULL, "created_at" datetime NOT NULL, "updated_at" datetime NOT NULL);
sqlite> SELECT * from members;
1|10|Taro|佐藤 太郎|Taro@example.com|1981-12-01|0|t|2017-12-06 02:02:24.955437|2017-12-06 02:02:24.955437
2|11|Jiro|鈴木 次郎|Jiro@example.com|1981-12-01|0|f|2017-12-06 02:02:24.970110|2017-12-06 02:02:24.970110
3|12|Hana|高橋 花子|Hana@example.com|1981-12-01|1|f|2017-12-06 02:02:24.983330|2017-12-06 02:02:24.983330
4|13|John|田中 太郎|John@example.com|1981-12-01|0|f|2017-12-06 02:02:24.993625|2017-12-06 02:02:24.993625
5|14|Mike|佐藤 次郎|Mike@example.com|1981-12-01|0|f|2017-12-06 02:02:25.005145|2017-12-06 02:02:25.005145
6|15|Sophy|鈴木 花子|Sophy@example.com|1981-12-01|1|f|2017-12-06 02:02:25.018035|2017-12-06 02:02:25.018035
7|16|Bill|高橋 太郎|Bill@example.com|1981-12-01|0|f|2017-12-06 02:02:25.030656|2017-12-06 02:02:25.030656
8|17|Alex|田中 次郎|Alex@example.com|1981-12-01|0|f|2017-12-06 02:02:25.054594|2017-12-06 02:02:25.054594
9|18|Mary|佐藤 花子|Mary@example.com|1981-12-01|1|f|2017-12-06 02:02:25.067116|2017-12-06 02:02:25.067116
10|19|Tom|鈴木 太郎|Tom@example.com|1981-12-01|0|f|2017-12-06 02:02:25.077334|2017-12-06 02:02:25.077334
11|10|Taro|佐藤 太郎|Taro@example.com|1981-12-01|0|t|2017-12-06 02:02:40.093907|2017-12-06 02:02:40.093907
12|11|Jiro|鈴木 次郎|Jiro@example.com|1981-12-01|0|f|2017-12-06 02:02:40.108721|2017-12-06 02:02:40.108721
13|12|Hana|高橋 花子|Hana@example.com|1981-12-01|1|f|2017-12-06 02:02:40.117574|2017-12-06 02:02:40.117574
14|13|John|田中 太郎|John@example.com|1981-12-01|0|f|2017-12-06 02:02:40.128931|2017-12-06 02:02:40.128931
15|14|Mike|佐藤 次郎|Mike@example.com|1981-12-01|0|f|2017-12-06 02:02:40.137714|2017-12-06 02:02:40.137714
16|15|Sophy|鈴木 花子|Sophy@example.com|1981-12-01|1|f|2017-12-06 02:02:40.149324|2017-12-06 02:02:40.149324
17|16|Bill|高橋 太郎|Bill@example.com|1981-12-01|0|f|2017-12-06 02:02:40.158810|2017-12-06 02:02:40.158810
18|17|Alex|田中 次郎|Alex@example.com|1981-12-01|0|f|2017-12-06 02:02:40.169564|2017-12-06 02:02:40.169564
19|18|Mary|佐藤 花子|Mary@example.com|1981-12-01|1|f|2017-12-06 02:02:40.181109|2017-12-06 02:02:40.181109
20|19|Tom|鈴木 太郎|Tom@example.com|1981-12-01|0|f|2017-12-06 02:02:40.189588|2017-12-06 02:02:40.189588
sqlite> .quit
shin4050:~/workspace/lecture-1206/asagao (master) $ bin/rails c
Loading development environment (Rails 4.2.10)
2.4.0 :001 > Members.ids
NameError: uninitialized constant Members
        from (irb):1
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :002 > Member.ids
   (0.1ms)  SELECT "members"."id" FROM "members"
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20] 
2.4.0 :003 > member = Members.find(3)
NameError: uninitialized constant Members
        from (irb):3
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :004 > member.email
NoMethodError: undefined method `email' for nil:NilClass
        from (irb):4
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :005 > member = Member.find(3)
  Member Load (0.3ms)  SELECT  "members".* FROM "members" WHERE "members"."id" = ? LIMIT 1  [["id", 3]]
 => #<Member id: 3, number: 12, name: "Hana", full_name: "高橋 花子", email: "Hana@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24"> 
2.4.0 :006 > 2.4.0 :002 > Member.ids
SyntaxError: (irb):6: unexpected fraction part after numeric literal
2.4.0 :002 > Member.ids
   ^
(irb):6: syntax error, unexpected ':', expecting end-of-input
2.4.0 :002 > Member.ids
       ^
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :007 >    (0.1ms)  SELECT "members"."id" FROM "members"
SyntaxError: (irb):7: syntax error, unexpected tIDENTIFIER, expecting ')'
   (0.1ms)  SELECT "members"."id" FROM 
         ^
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :008 >  => [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20] 
SyntaxError: (irb):8: syntax error, unexpected =>
 => [1, 2, 3, 4, 5, 6, 7, 8, 9, 1
   ^
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:110:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/console.rb:9:in `start'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:68:in `console'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands/commands_tasks.rb:39:in `run_command!'
        from /usr/local/rvm/gems/ruby-2.4.0@global/gems/railties-4.2.10/lib/rails/commands.rb:17:in `<top (required)>'
        from bin/rails:4:in `require'
        from bin/rails:4:in `<main>'
2.4.0 :009 > member.email                     
 => "Hana@example.com" 
2.4.0 :010 > member = Member.find_by(name: "Taro")
  Member Load (0.4ms)  SELECT  "members".* FROM "members" WHERE "members"."name" = ? LIMIT 1  [["name", "Taro"]]
 => #<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24"> 
2.4.0 :011 > member = Member.find_by(gender: 0, administrator: false)
  Member Load (0.3ms)  SELECT  "members".* FROM "members" WHERE "members"."gender" = ? AND "members"."administrator" = ? LIMIT 1  [["gender", 0], ["administrator", "f"]]
 => #<Member id: 2, number: 11, name: "Jiro", full_name: "鈴木 次郎", email: "Jiro@example.com", birthday: "1981-12-01", gender: 0, administrator: false, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24"> 
2.4.0 :012 > member = Member.find_by(gender: 1, administrator: true)
  Member Load (0.3ms)  SELECT  "members".* FROM "members" WHERE "members"."gender" = ? AND "members"."administrator" = ? LIMIT 1  [["gender", 1], ["administrator", "t"]]
 => nil 
2.4.0 :013 > member = Member.where(name: "Taro")
  Member Load (0.3ms)  SELECT "members".* FROM "members" WHERE "members"."name" = ?  [["name", "Taro"]]
 => #<ActiveRecord::Relation [#<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24">, #<Member id: 11, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:40", updated_at: "2017-12-06 02:02:40">]> 
2.4.0 :014 > puts member.to_sql
SELECT "members".* FROM "members" WHERE "members"."name" = 'Taro'
 => nil 
2.4.0 :015 > members = Member.where(name: "Taro").where("number < 20")
  Member Load (0.3ms)  SELECT "members".* FROM "members" WHERE "members"."name" = ? AND (number < 20)  [["name", "Taro"]]
 => #<ActiveRecord::Relation [#<Member id: 1, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24">, #<Member id: 11, number: 10, name: "Taro", full_name: "佐藤 太郎", email: "Taro@example.com", birthday: "1981-12-01", gender: 0, administrator: true, created_at: "2017-12-06 02:02:40", updated_at: "2017-12-06 02:02:40">]> 
2.4.0 :016 > members = Member.where(gender: 1).order("number")
  Member Load (0.3ms)  SELECT "members".* FROM "members" WHERE "members"."gender" = ?  ORDER BY number  [["gender", 1]]
 => #<ActiveRecord::Relation [#<Member id: 3, number: 12, name: "Hana", full_name: "高橋 花子", email: "Hana@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:24", updated_at: "2017-12-06 02:02:24">, #<Member id: 13, number: 12, name: "Hana", full_name: "高橋 花子", email: "Hana@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:40", updated_at: "2017-12-06 02:02:40">, #<Member id: 6, number: 15, name: "Sophy", full_name: "鈴木 花子", email: "Sophy@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:25", updated_at: "2017-12-06 02:02:25">, #<Member id: 16, number: 15, name: "Sophy", full_name: "鈴木 花子", email: "Sophy@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:40", updated_at: "2017-12-06 02:02:40">, #<Member id: 9, number: 18, name: "Mary", full_name: "佐藤 花子", email: "Mary@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:25", updated_at: "2017-12-06 02:02:25">, #<Member id: 19, number: 18, name: "Mary", full_name: "佐藤 花子", email: "Mary@example.com", birthday: "1981-12-01", gender: 1, administrator: false, created_at: "2017-12-06 02:02:40", updated_at: "2017-12-06 02:02:40">]> 
2.4.0 :017 > exit


```