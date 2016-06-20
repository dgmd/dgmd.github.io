task :default => [:serve]

task :serve do
	system('jekyll serve')
end

task :update do
	require 'yaml'
	currentDirectory = File.dirname(__FILE__)
	partialRoot = File.join(currentDirectory, '_snippets')
	snippetRoot = File.join(currentDirectory, 'snippets')
	delimiter = '---'

	Dir.foreach(partialRoot) do |snippetFile|
		next if snippetFile == '.' or snippetFile == '..'
		partialPath = File.join(partialRoot, snippetFile)
		snippetFrontMatter = File.read(partialPath).split(delimiter)[1]
		snippet = YAML.load(snippetFrontMatter)

		snippetPath = File.join(snippetRoot, snippet['slug'])
		snippetURL = snippet['url']

		puts "git subtree pull --prefix #{snippetPath} #{snippetURL} master --squash"
	end
end