# frozen_string_literal: true

require 'bundler'
require 'puppet_litmus/rake_tasks' if Gem.loaded_specs.key? 'puppet_litmus'
require 'puppetlabs_spec_helper/rake_tasks'
require 'puppet-syntax/tasks/puppet-syntax'
require 'puppet-strings/tasks' if Gem.loaded_specs.key? 'puppet-strings'

PuppetLint.configuration.send('disable_relative')

desc "Run PowerShell unit tests"
task :spec_pester do
  exec ("powershell -NoProfile -NoLogo -NonInteractive -Command \". spec/run_pester.ps1 -EnableExit\"")
end
