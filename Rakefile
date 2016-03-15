require "bundler/gem_tasks"

task :default => :test

desc "Run Unit Tests"
task :test do
  $: << File.expand_path(File.dirname(__FILE__) + "/test")
  Dir.glob('./test/**/*_test.rb').each { |file| require file }
end


desc "IRB with this gem required" 
task :console do
  require 'irb'
  require 'irb/completion'
  require 'scout_apm'
  ARGV.clear
  IRB.start
end
