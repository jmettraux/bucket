
= bucket

Place the file bucket.html in an S3 bucket and it will list the content of the bucket.


== rake upload

There is a Rakefile helper

  BUCKET=my-bucket rake upload

to upload bucket.html into the my-bucket. It's limited to US buckets. To place bucket.html in Europe or Asia, you have to upload it manually.


== TODO

[o] over 1000 keys
[ ] column sorting
[ ] thumbnails ?


== author

John Mettraux - http://github.com/jmettraux


== LICENSE

MIT

