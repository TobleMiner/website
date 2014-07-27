task :default => 'build'

desc "Build the site using Jekyll"
task :build do
	puts "Building Jekyll site using config in _config.yml...\n\n"
	sh "bundle exec jekyll build"
end

desc "Publish the site via SSH/SCP"
task :publish => :build do
	puts "Cleaning up remote directories via SSH..."
	sh "ssh elomatreb@elomatreb.eu -p 5190 './cleanup_jekyll.sh'"
	# @TODO: Finish publishing
end

desc "Build the site using Jekyll, with automatic re-build on save."
task :watch do
	puts "Building Jekyll site with watch-mode enabled..."
	sh "bundle exec jekyll build -w"
end
