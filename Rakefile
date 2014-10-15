require 'rubygems'
require 'bundler'
require 'bundler/setup'



require 'cucumber/rake/task'
Cucumber::Rake::Task.new(:features) do |features|
  features.cucumber_opts = "features -p selenium --format progress"
end
Cucumber::Rake::Task.new(:features_ci) do |task|
  task.cucumber_opts = ["-p poltergeist -f pretty -f junit --out target/ -f html --out target/report.html"]
end




task :cuke_sniffer do 
	sh 'cd features'
	sh 'bundle exec cuke_sniffer'
end



require 'rubocop/rake_task'

#desc "Run Rubocop"

#Rubocop::RakeTask.new(:rubocop_rake) do |task|
#	task.patterns = ['features/**/*.rb']
#end

task :rubocop do 
  sh 'bundle exec rubocop'
end
	

