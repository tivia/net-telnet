# frozen_string_literal: true

require 'bundler/gem_tasks'
require 'rubygems'
require 'rubygems/package_task'
require 'rdoc/task'

task :build do
  puts `gem build net-telnet.gemspec`
end

task :install do
  puts `gem build net-telnet.gemspec`
  puts `gem install ./net-telnet-#{File.open('VERSION.txt','r').to_a.join.strip}.gem`
end

RDoc::Task.new do |rdoc|
  rdoc.name     = 'rdoc'
  rdoc.main     = 'README.txt'
  rdoc.rdoc_dir = 'doc'
  rdoc.rdoc_files.include('README.txt', 'LICENSE.txt', 'lib/**/*.rb')
end

task default: %i[build rdoc]
