---
layout: post
title: A-Very-Basic-Rails-Blog
---

Though I have done some basic ruby coding in the past, I have not prior to now done anything with the Rails framework, so I am going to post 
what I do in this exercise as I go. The following is my terminal dialog followed by a screenshot of the application output as it appears in the web browser.

dbeatt4:~/workspace $ rails generate scaffold Post title:string body:text
Running via Spring preloader in process 2568
      invoke  active_record
      create    db/migrate/20181002210516_create_posts.rb
      create    app/models/post.rb
      invoke    test_unit
      create      test/models/post_test.rb
      create      test/fixtures/posts.yml
      invoke  resource_route
       route    resources :posts
      invoke  scaffold_controller
      create    app/controllers/posts_controller.rb
      invoke    erb
      create      app/views/posts
      create      app/views/posts/index.html.erb
      create      app/views/posts/edit.html.erb
      create      app/views/posts/show.html.erb
      create      app/views/posts/new.html.erb
      create      app/views/posts/_form.html.erb
      invoke    test_unit
      create      test/controllers/posts_controller_test.rb
      invoke    helper
      create      app/helpers/posts_helper.rb
      invoke      test_unit
      invoke    jbuilder
      create      app/views/posts/index.json.jbuilder
      create      app/views/posts/show.json.jbuilder
      create      app/views/posts/_post.json.jbuilder
      invoke  assets
      invoke    coffee
      create      app/assets/javascripts/posts.coffee
      invoke    scss
      create      app/assets/stylesheets/posts.scss
      invoke  scss
      create    app/assets/stylesheets/scaffolds.scss
dbeatt4:~/workspace $ rake db:migrate
== 20181002210516 CreatePosts: migrating ======================================
-- create_table(:posts)
   -> 0.0014s
== 20181002210516 CreatePosts: migrated (0.0015s) =============================

dbeatt4:~/workspace $ rails s -b $IP -p $PORT
=> Booting WEBrick
=> Rails 4.2.5 application starting in development on http://0.0.0.0:8080
=> Run `rails server -h` for more startup options
=> Ctrl-C to shutdown server
[2018-10-02 21:07:25] INFO  WEBrick 1.3.1
[2018-10-02 21:07:25] INFO  ruby 2.3.4 (2017-03-30) [x86_64-linux]
[2018-10-02 21:07:25] INFO  WEBrick::HTTPServer#start: pid=2585 port=8080


Started GET "/" for 108.185.231.255 at 2018-10-02 21:08:17 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
  ActiveRecord::SchemaMigration Load (0.2ms)  SELECT "schema_migrations".* FROM "schema_migrations"
Processing by Rails::WelcomeController#index as HTML
  Rendered /usr/local/rvm/gems/ruby-2.3.4/gems/railties-4.2.5/lib/rails/templates/rails/welcome/index.html.erb (2.3ms)
Completed 200 OK in 26ms (Views: 16.8ms | ActiveRecord: 0.0ms)


Started GET "/posts" for 108.185.231.255 at 2018-10-02 21:09:19 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#index as HTML
  Post Load (0.4ms)  SELECT "posts".* FROM "posts"
  Rendered posts/index.html.erb within layouts/application (3.7ms)
Completed 200 OK in 1048ms (Views: 1044.6ms | ActiveRecord: 0.6ms)


Started GET "/assets/scaffolds.self-d2e5ccad1506299feea3a35bfb7c525e101bb3b214303715deb675fdc539948b.css?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/posts.self-e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855.css?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/application.self-e80e8f2318043e8af94dddc2adad5a4f09739a8ebb323b3ab31cd71d45fd9113.css?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/jquery.self-bd7ddd393353a8d2480a622e80342adf488fb6006d667e8b42e4c0073393abee.js?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/turbolinks.self-1d1fddf91adc38ac2045c51f0a3e05ca97d07d24d15a4dcbf705009106489e69.js?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/jquery_ujs.self-784a997f6726036b1993eb2217c9cb558e1cbb801c6da88105588c56f13b466a.js?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/posts.self-877aef30ae1b040ab8a3aba4e3e309a11d7f2612f44dde450b5c157aa5f95c05.js?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/assets/application.self-3b8dabdc891efe46b9a144b400ad69e37d7e5876bdc39dee783419a69d7ca819.js?body=1" for 108.185.231.255 at 2018-10-02 21:09:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255


Started GET "/posts/new" for 108.185.231.255 at 2018-10-02 21:09:28 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#new as HTML
  Rendered posts/_form.html.erb (71.8ms)
  Rendered posts/new.html.erb within layouts/application (84.0ms)
Completed 200 OK in 157ms (Views: 151.5ms | ActiveRecord: 0.5ms)


Started POST "/posts" for 108.185.231.255 at 2018-10-02 21:10:19 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#create as HTML
  Parameters: {"utf8"=>"✓", "authenticity_token"=>"u/OagyQOTYhWZ/4UT1ZUjWefUZkRTN1z6JBofC9gneppn2+K7xhO8AILpdYDBXv06l/eSuCCXPemZJ1ym3g8+w==", "post"=>{"title"=>"Ruby on Rails Blog Post #1", "body"=>"My first ruby on rails application..."}, "commit"=>"Create Post"}
   (0.2ms)  begin transaction
  SQL (0.7ms)  INSERT INTO "posts" ("title", "body", "created_at", "updated_at") VALUES (?, ?, ?, ?)  [["title", "Ruby on Rails Blog Post #1"], ["body", "My first ruby on rails application..."], ["created_at", "2018-10-02 21:10:19.958269"], ["updated_at", "2018-10-02 21:10:19.958269"]]
   (16.6ms)  commit transaction
Redirected to https://rails-blog-dbeatt4.c9users.io/posts/1
Completed 302 Found in 32ms (ActiveRecord: 17.5ms)


Started GET "/posts/1" for 108.185.231.255 at 2018-10-02 21:10:20 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#show as HTML
  Parameters: {"id"=>"1"}
  Post Load (0.4ms)  SELECT  "posts".* FROM "posts" WHERE "posts"."id" = ? LIMIT 1  [["id", 1]]
  Rendered posts/show.html.erb within layouts/application (2.2ms)
Completed 200 OK in 65ms (Views: 41.1ms | ActiveRecord: 0.4ms)


Started GET "/posts" for 108.185.231.255 at 2018-10-02 21:10:54 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#index as HTML
  Post Load (0.3ms)  SELECT "posts".* FROM "posts"
  Rendered posts/index.html.erb within layouts/application (1.8ms)
Completed 200 OK in 29ms (Views: 27.9ms | ActiveRecord: 0.3ms)


Started GET "/posts/new" for 108.185.231.255 at 2018-10-02 21:11:06 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#new as HTML
  Rendered posts/_form.html.erb (2.2ms)
  Rendered posts/new.html.erb within layouts/application (3.5ms)
Completed 200 OK in 24ms (Views: 22.9ms | ActiveRecord: 0.0ms)


Started POST "/posts" for 108.185.231.255 at 2018-10-02 21:11:58 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#create as HTML
  Parameters: {"utf8"=>"✓", "authenticity_token"=>"tU0v6khi6ii8oDaWl8yfoH0lwlZuYpSCLwXpjUccxmxnIdrjg3TpUOjMbVTbn7DZ8OVNhZ+sFQZh8RyD8wRnfQ==", "post"=>{"title"=>"Ruby on Rails Blog Post #2", "body"=>"This is my second post on my first ruby on rails app."}, "commit"=>"Create Post"}
   (0.1ms)  begin transaction
  SQL (0.4ms)  INSERT INTO "posts" ("title", "body", "created_at", "updated_at") VALUES (?, ?, ?, ?)  [["title", "Ruby on Rails Blog Post #2"], ["body", "This is my second post on my first ruby on rails app."], ["created_at", "2018-10-02 21:11:58.066695"], ["updated_at", "2018-10-02 21:11:58.066695"]]
   (12.7ms)  commit transaction
Redirected to https://rails-blog-dbeatt4.c9users.io/posts/2
Completed 302 Found in 18ms (ActiveRecord: 13.3ms)


Started GET "/posts/2" for 108.185.231.255 at 2018-10-02 21:11:58 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#show as HTML
  Parameters: {"id"=>"2"}
  Post Load (0.3ms)  SELECT  "posts".* FROM "posts" WHERE "posts"."id" = ? LIMIT 1  [["id", 2]]
  Rendered posts/show.html.erb within layouts/application (0.6ms)
Completed 200 OK in 21ms (Views: 19.2ms | ActiveRecord: 0.3ms)


Started GET "/posts" for 108.185.231.255 at 2018-10-02 21:12:02 +0000
Cannot render console from 108.185.231.255! Allowed networks: 127.0.0.1, ::1, 127.0.0.0/127.255.255.255
Processing by PostsController#index as HTML
  Post Load (0.3ms)  SELECT "posts".* FROM "posts"
  Rendered posts/index.html.erb within layouts/application (2.0ms)
Completed 200 OK in 24ms (Views: 23.2ms | ActiveRecord: 0.3ms)

![alt](https://www.keepandshare.com/userpics/h/e/a/r/tnhandstraining/2018-10/sb/ruby_on_ratls-75798012.jpg?ts=1538516801)

**Code to have the application run from the posts page (as above):**
![al](http://www.keepandshare.com/userpics/h/e/a/r/tnhandstraining/2018-10/sb/root_routs-62848630.jpg?ts=1538517541)
