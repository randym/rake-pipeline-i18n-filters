#!/usr/bin/env rake
require "bundler/gem_tasks"
require "bundler/setup"

desc "run the specs"
task :spec do
  sh "rspec -cfs spec"
end

task :default => :spec

desc "build the gem"
task :build do
  system "gem build rake-pipeline-i18n-filters.gemspec"
end
desc "build and release the gem"
task :release => :build do
  system "gem push rake-pipeline-i18n-filters-#{Rake::Pipeline::I18n::Filters::VERSION}.gem"
end
