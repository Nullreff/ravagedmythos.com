task :default => :server

task :clean do
  sh 'rm -rf build/*'
end

task :server do
  middleman 'server'
end

task :build do
  middleman 'build'
end

task :deploy => :build do
  sh 'rsync -rtzh --progress --delete build/ webfaction:~/webapps/ravaged_mythos/'
end


def middleman(args)
  sh "bundle exec middleman #{args}"
end
