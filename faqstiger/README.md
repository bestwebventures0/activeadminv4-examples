# Readme

Faqstiger uses Rails 8, ActiveAdmin v4, and Actiontext.

## Highlights

- No use of Nodejs
- Uses a task to build CSS (TailwindCSS and Flowbite) for ActiveAdmin v4
- Adds trix related pins to ActiveAdmin v4

## Configuration steps

### 1. Install ActiveAdmin v4 gem on your terminal (or console)
```bash
gem install activeadmin --pre
```

### 2. Install required gems configured in Gemfile
```bash
$ bundle install
```

### 3. Run migrations and add seed data (admin@example.com/password) for activeadmin
```bash
$ rails db:migrate
$ rails db:seed
```

### 4. Which files do the magic?

```
- tailwind-active_admin.config.js
- config/initializers/active_admin.rb
- app/javascript/active_admin_custom.js
- lib/tasks/active_admin.rake
- app/views/active_admin/_html_head.html.erb
```

### How can I use ActiveAdmin v4 in my project?
- ```$ rails action_text:install```
- ```$ rails g active_admin:install```
- ```$ rails db:migrate```
- ```$ rails db:seed```
- copy all the files doing magic listed in point 4 above
- do NOT use node or webpacker or yarn. I haven't tested but using those might break activeadmin4 funtionality in your project.
