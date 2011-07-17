source :rubygems

gem "rails", "2.3.12"

gem "coderay", "~> 0.9.7"
gem "i18n", "~> 0.4.2"
gem "rubytree", "~> 0.5.2", :require => 'tree'
gem "rdoc", ">= 2.4.2"
gem 'giternal' 
gem 'heroku' 



group :test do
  gem 'shoulda', '~> 2.10.3'
  gem 'edavis10-object_daddy', :require => 'object_daddy'
  gem 'mocha'
end

group :openid do
  gem "ruby-openid", '~> 2.1.4', :require => 'openid'
end


gem "rmagick"


# Use the commented pure ruby gems, if you have not the needed prerequisites on
# board to compile the native ones.  Note, that their use is discouraged, since
# their integration is propbably not that well tested and their are slower in
# orders of magnitude compared to their native counterparts. You have been
# warned.
#

gem "pg", "~> 0.9.0"


platforms :jruby do
  gem "jruby-openssl"

  group :mysql do
    gem "activerecord-jdbcmysql-adapter"
  end
  
  group :postgres do
    gem "activerecord-jdbcpostgresql-adapter"
  end
  
  group :sqlite do
    gem "activerecord-jdbcsqlite3-adapter"
  end
end

# Load plugins' Gemfiles
Dir.glob File.expand_path("../vendor/plugins/*/Gemfile", __FILE__) do |file|
  puts "Loading #{file} ..." if $DEBUG # `ruby -d` or `bundle -v`
  instance_eval File.read(file)
end
