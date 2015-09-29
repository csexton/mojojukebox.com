namespace :deploy do
  desc "Deploy to production"
  task :production do
    sh <<-EOF
      rsync --progress --stats --verbose --recursive --times --perms --links \
      --exclude ".*" \
      --exclude "Rakefile" \
      --exclude "gruntfile.js" \
      --exclude "package.json" \
      ./ \
      mojojukebox@mojojukebox.com:mojojukebox.com/
    EOF

  end
end

