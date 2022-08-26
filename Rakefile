namespace :greeting do 
  desc "output hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "output holla to the terminal"
  task :holla do
    puts "holla de Rake!"
  end
end

namespace :db do
  desc "migrate changes to the database"
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end

task :environment do
  require_relative "./config/environment"
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end