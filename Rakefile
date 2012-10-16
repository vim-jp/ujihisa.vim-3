desc :default
task :default do
  # sh 'pandoc -s --from=markdown --to=html README.md -o index.html'
  body = `pandoc README.md`
  require 'erb'
  File.open('index.html', 'w') do |io|
    io.print ERB.new(File.read 'index.erb').result(binding)
  end
end
