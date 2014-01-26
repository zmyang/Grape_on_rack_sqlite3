require_relative 'app'

namespace :db do

	desc "Creates the database"
	task :create do
		puts "Creating database..."
		UserDB.setup
	end

	desc "Seeds the DB with the data from the csv file"
	task :seed  do
		puts "Seeding database..."
		UserDB.seed(Parser.parser('db/people.csv'))
	end

	desc "drop the database"
	task :drop do
		puts "Deleting database..."
		rm_f 'user.db'
	end
end

desc 'Start IRB with application environment loaded'
task :console do
  exec "irb -r./app"
end