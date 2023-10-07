task :default => [:server]

# Remove all generated files
task :clean do
  puts "cleaning _site directory..."
  system "rm -rf _site stylesheets"
end

# Install bundle
task :setup  => [:clean] do
  system "bundle install"
end

# Generate site
task :build  => [:setup] do
  system "bundle exec jekyll build"
end

task :server => [:build] do
  system "bundle exec jekyll serve"
end
