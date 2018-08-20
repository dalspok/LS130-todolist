require "rake/testtask"
require "find"
require "bundler/gem_tasks"

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Print files'
task :print_files do
  Find.find('.') do |path|
    puts path if File.file?(path) && !path.match('/\.')
  end
end