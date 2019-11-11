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
  desc 'add environment dependency'
  task :environment do
    require './config/environment.rb'
  end

  desc 'invokes env task as a dependence'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the db'
  task :seed do 
    require './db/seeds.rb'
  end
end
