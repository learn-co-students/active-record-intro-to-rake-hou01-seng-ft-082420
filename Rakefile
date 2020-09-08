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

  desc 'opens console'
      task console: :environment do
        Pry.start
  end

  desc 'environments'
  task :environment do
    require_relative './config/environment.rb'
  end

  namespace :db do
    desc 'migrates'
    task migrate: :environment do
      Student.create_table
    end

    desc 'seeds'
    task :seed do
      require_relative './db/seeds.rb'
    end
  end
