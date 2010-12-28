
require 'aws/s3'


task :connect do

  AWS::S3::Base.establish_connection!(
    :access_key_id => ENV['AMAZON_ACCESS_KEY_ID'],
    :secret_access_key => ENV['AMAZON_SECRET_ACCESS_KEY'])
end

task :buckets => :connect do

  AWS::S3::Service.buckets.each do |bucket|
    puts " / "
    p bucket
  end
end

task :upload => :connect do

  raise ArgumentError.new("missing env var BUCKET") unless ENV['BUCKET']

  AWS::S3::S3Object.store(
    'bucket.html',
    File.read('bucket.html'),
    ENV['BUCKET'],
    :access => :public_read)

  puts "bucket.html uploaded to '#{ENV['BUCKET']}'"
end

