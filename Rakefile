task :hello do
  puts "hello from Rake!"
end

task :environment do
  require_relative './config/environment'
end

desc 'starts Pry'
task console: :environment do
  Pry.start
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end