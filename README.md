# rails-sample-app

This is an accompanying repository for [Efficient Rails DevOps](https://efficientrailsdevops.com), my book about provisioning Rails servers and deploying applications with Ansible.

It holds basic Ruby on Rails applications for educational and testing purposes.

Every branch of this repository contains two commits (and is named after the Rails version that was used to create it):

* The first commit is a basic Rails application created with the `rails new .` command (tagged as `x.x.x-base`).
* The second commit adds a basic customer scaffold created with `rails generate scaffold customer name:string:uniq` (because my book needs something to deploy after the initial application has been setup).

There are only two small differences to a "real" repository:

* The `master.key` file is included (by editing the app's `.gitignore` file) to allow editing of the `credentials.yml.enc` file.
* I adjusted the `Gemfile` by moving the `sqlite3` gem into the `group :development, :test do` block and added a `:production` group to require the `mysql2` or `pg` gem (depending on whether you use the `*-mariadb` or `*-postgresql` branch).

Only future versions of Rails will be added if a new version is available when I update the book. Of course you are welcome to use this repository for other purposes, whenever you need a basic Rails app (no branches will be removed).
