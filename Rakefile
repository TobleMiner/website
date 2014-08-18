task :default => 'build'

desc "Build the site using Jekyll (including assets)"
task :build do
	puts "Building Jekyll site using config in _config.yml...\n\n"
	sh "bundle exec jekyll build"
end

desc "Build the site using Jekyll (including assets), with automatic re-build on save."
task :watch do
	puts "Building Jekyll site with watch-mode enabled..."
	sh "bundle exec jekyll build -w"
end
