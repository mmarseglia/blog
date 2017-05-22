require 'jekyll-import'

desc 'Default task'
task default: %w[blog:build]

namespace :blog do
  desc 'Build blog'
  task :build do
    puts 'Building blog.'
    JekyllImport::Importers::Blogger.run({
      "source"                => "import/*.xml",
      "no-blogger-info"       => false, # not to leave blogger-URL info (id and old URL) in the front matter
      "replace-internal-link" => false, # replace internal links using the post_url liquid tag.
    })
  end
end
