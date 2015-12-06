require 'sprockets'

gem_spec = Gem::Specification.find_by_name 'sprockets'
require "#{gem_spec.gem_dir}/lib/rake/sprocketstask"

MANIFEST_FILES = %w( javascripts/application.js stylesheets/application.css )
ASSET_INPUT_PATH = 'assets'

# create rake tasks asset build, clean, clobber.
Rake::SprocketsTask.new do |t|
  t.environment = Sprockets::Environment.new
  t.output      = "./public/assets"
  t.assets      = MANIFEST_FILES

  t.environment.append_path ASSET_INPUT_PATH
end



desc "Empty test for travis example"
task :test do
  puts "** Running test"
end

task :compile_assets do
  Rake::Task["assets"].invoke("assets")
end

desc "By default, run rake test"
  task :default => [ :compile_assets ] do
end
