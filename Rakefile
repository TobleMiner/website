require "mini_magick"

task :default => 'build'

desc "Build the site using Jekyll (including assets)"
task :build => [:setup, :scale_images] do
	puts "Building Jekyll site using config in _config.yml...\n\n"
	sh "bundle exec jekyll build"
end

desc "Build the site using Jekyll (including assets), with automatic re-build on save."
task :watch do
	puts "Building Jekyll site with watch-mode enabled..."
	sh "bundle exec jekyll build -w"
end

desc "Scale all images wider than 860px down to 860px (width)"
task :scale_images do
	FileList.new(["img/*.png", "img/*.jpg", "img/*.jpeg"]).each do |i|
		image = MiniMagick::Image.open i
		if image[:width] > 860
			puts "Resizing #{i.gsub("img/", "")}..."
			image.resize "860"
			FileUtils.cp i, "#{i}.~" # Backup existing image
			image.write i
		end
	end
end

desc "Setup dependencies"
task :setup do
	unless File.directory?(File.expand_path("css/bourbon/"))
		sh "bundle exec bourbon install --path=css/"
	end
end
