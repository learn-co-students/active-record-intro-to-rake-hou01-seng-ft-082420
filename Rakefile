require 'pry'

task :environment do
  require_relative './config/environment'
end

desc 'outputs hello to the terminal'
namespace :greeting do
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end
