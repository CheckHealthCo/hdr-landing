# Rake tasks

desc "Build the site"
task :build do
  puts "Building site"
  sh "rsync -art src/ site/"
end

desc "Test the build"
task :test => [:build] do
  sh "bundle exec htmlproofer --url-ignore \"/#.*/,/linkedin.com/\" ./site"
end

desc "Publish to S3"
task :publish do
  puts "Publishing to S3"
  sh "bundle exec s3_website push"
  puts "Published"
end

task :default => [:test]
