# coding: utf-8
#
# das ist für org-mode system
require 'jekyll'
require 'rubygems'
require 'time'
require 'rake'
require 'yaml'

# config # {{{
SOURCE = "."
CONFIG = {
  'orgposts' => File.join(SOURCE, "org/posts/"),
  'orgmurmured' => File.join(SOURCE, "org/murmured/"),
  'orgideas' => File.join(SOURCE, "org/ideas/"),
  'orgmemo' => File.join(SOURCE, "org/memo/"),
  'orgpost_ext' => "org"
}
# }}}

# create a new org-mode doc# {{{
# useage: "rake orgpost"
desc "Create a new org-mode doc in #{CONFIG['org-mode-posts']}"
task :orgpost, :title do |t, args|
  abort("rake aborted: '#{CONFIG['orgposts']}' directory not found.") unless FileTest.directory?(CONFIG['orgposts'])
  if args.title
    title = args.title
  else
    title = get_stdin("Enter a title for your org-mode post: ")
  end
#  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  end
  filename = File.join(CONFIG['orgposts'], "#{date}-#{slug}.#{CONFIG['orgpost_ext']}")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?", ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "\#\+TITLE:#{title.gsub(/-/, ' ')}"
    post.puts "\#\+OPTIONS: toc:nil"
    post.puts "\#\+STARTUP: showall indent"
    post.puts "\#\+STARTUP: hidestars"
    post.puts "\#\+BEGIN_HTML"
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: #{title}"
    post.puts "subtitle: #{title}"
    post.puts "date: #{date}"
    post.puts "author: huwhoover"
    post.puts "categories: Blog"
    post.puts "excerpt: #{title}"
    post.puts "tags:"
    post.puts "---"
    post.puts "\#\+END_HTML"

  end
end # task :orgpost
# }}}

# create a new org-murmured doc# {{{
# useage: "rake orgpost"
desc "Create a new org-murmured doc in #{CONFIG['orgmurmured']}"
task :orgmurmured, :title do |t, args|
  abort("rake aborted: '#{CONFIG['orgmurmured']}' directory not found.") unless FileTest.directory?(CONFIG['orgmurmured'])
  if args.title
    title = args.title
  else
    title = get_stdin("Enter a title for your org-mode post: ")
  end
#  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  end
  filename = File.join(CONFIG['orgmurmured'], "#{date}-#{slug}.#{CONFIG['orgpost_ext']}")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?", ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "\#\+TITLE:#{title.gsub(/-/, ' ')}"
    post.puts "\#\+OPTIONS: toc:nil"
    post.puts "\#\+STARTUP: showall indent"
    post.puts "\#\+STARTUP: hidestars"
    post.puts "\#\+BEGIN_HTML"
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: #{title}"
    post.puts "subtitle: #{title}"
    post.puts "date: #{date}"
    post.puts "categories: Murmured"
    post.puts "author: huwhoover"
    post.puts "excerpt: #{title}"
    post.puts "tags:"
    post.puts "---"
    post.puts "\#\+END_HTML"

  end
end # task :orgpost
# }}}

# create a new org-ideas doc# {{{
# useage: "rake orgpost"
desc "Create a new org-ideas doc in #{CONFIG['orgideas']}"
task :orgideas, :title do |t, args|
  abort("rake aborted: '#{CONFIG['orgideas']}' directory not found.") unless FileTest.directory?(CONFIG['orgideas'])
  if args.title
    title = args.title
  else
    title = get_stdin("Enter a title for your org-mode post: ")
  end
#  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  end
  filename = File.join(CONFIG['orgideas'], "#{date}-#{slug}.#{CONFIG['orgpost_ext']}")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?", ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "\#\+TITLE:#{title.gsub(/-/, ' ')}"
    post.puts "\#\+OPTIONS: toc:nil"
    post.puts "\#\+STARTUP: showall indent"
    post.puts "\#\+STARTUP: hidestars"
    post.puts "\#\+BEGIN_HTML"
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: #{title}"
    post.puts "subtitle: #{title}"
    post.puts "date: #{date}"
    post.puts "categories: ideas"
    post.puts "author: huwhoover"
    post.puts "excerpt: "
    post.puts "tags:"
    post.puts "---"
    post.puts "\#\+END_HTML"

  end
end # task :orgpost
# }}}

# create a new org-memo doc# {{{
# useage: "rake orgpost"
desc "Create a new org-memo doc in #{CONFIG['orgmemo']}"
task :orgmemo, :title do |t, args|
  abort("rake aborted: '#{CONFIG['orgmemo']}' directory not found.") unless FileTest.directory?(CONFIG['orgmemo'])
  if args.title
    title = args.title
  else
    title = get_stdin("Enter a title for your org-mode post: ")
  end
#  title = ENV["title"] || "new-post"
  slug = title.downcase.strip.gsub(' ', '-').gsub(/[^\w-]/, '')
  begin
    date = (ENV['date'] ? Time.parse(ENV['date']) : Time.now).strftime('%Y-%m-%d')
  end
  filename = File.join(CONFIG['orgmemo'], "#{date}-#{slug}.#{CONFIG['orgpost_ext']}")
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?", ['y', 'n']) == 'n'
  end

  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "\#\+TITLE:#{title.gsub(/-/, ' ')}"
    post.puts "\#\+OPTIONS: toc:nil"
    post.puts "\#\+STARTUP: showall indent"
    post.puts "\#\+STARTUP: hidestars"
    post.puts "\#\+BEGIN_HTML"
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: #{title}"
    post.puts "subtitle: #{title}"
    post.puts "date: #{date}"
    post.puts "categories: memo"
    post.puts "author: huwhoover"
    post.puts "excerpt: #{title}"
    post.puts "tags:"
    post.puts "---"
    post.puts "\#\+END_HTML"

  end
end # task :orgpost
# }}}

# definitions # {{{
def ask(message, valid_options)
  if valid_options
    answer = get_stdin("#{message} #{valid_options.to_s.gsub(/"/, '').gsub(/,/, '/')}") while !valid_options.include?(answer)
  else
    answer = get_stdin(message)
  end
  answer
end

def get_stdin(message)
  print message
  STDIN.gets.chomp
end
# }}}

#Load custom rake scripts
Dir['_rake/*.rake'].each { |r| load r }
