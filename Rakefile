namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrates changes to your database'
  task :migrate => :environment do
      Student.create_table
  end

  desc 'seeds dummy data into our database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into Pry console'
task :console => :environment do
  Pry.start
end

desc 'sets up access to environment files'
task :environment do
  require_relative './config/environment'
end