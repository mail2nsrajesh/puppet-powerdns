require 'rake'

require 'puppet-lint/tasks/puppet-lint'
require 'rspec/core/rake_task'

PuppetLint.configuration.send("disable_80chars")

task :default => [:lint, :spec]

RSpec::Core::RakeTask.new(:spec) do |t|
  t.pattern     = 'spec/*/*_spec.rb'
  t.rspec_opts  = '--color'
end
