require "bundler/gem_tasks"
require "rake/testtask"

JRuby.objectspace = true if RUBY_PLATFORM == 'java'

Rake::TestTask.new(:test) do |t|
  t.libs << "test/lib"
  t.ruby_opts << "-rhelper"
  t.test_files = FileList["test/**/test_*.rb"]
end

task :default => :test
