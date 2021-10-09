# 🌐 Get Internet Speed

A sample Ruby Cloud function to check your network's download and upload speed. 

## 🚀 Building and Packaging

To package this example as a cloud function, follow these steps.

```bash
$ cd demos-for-functions/ruby/get-internet-speed
$ docker run --rm -v $(pwd):/app -w /app --env GEM_HOME=./.appwrite appwrite/env-ruby-3.0:1.0.0 bundle install
```

- Ensure that your folder structure looks like this

```
.
├── .appwrite/
├── Gemfile
├── Gemfile.lock
├── main.rb
└── README.md
```

- Create a tarfile

```bash
$ cd ..
$ tar -zcvf code.tar.gz get-internet-speed
```

- Navigate to the Overview Tab of your Cloud Function > Deploy Tag
- Input the command that will run your function (in this case "ruby main.rb") as your entrypoint command
- Upload your tarfile
- Click 'Activate'

## 🎯 Trigger

Trigger the cloud function using the SDK or HTTP API or the Appwrite Console.

- Sample Output:

```ruby
Your IP: 97.126.32.16
Your coordinates: [47.4356, -122.1141]
Automatically selected server: http://lg.sea-z.fdcservers.net - 32.985 ms
Server http://lg.sea-z.fdcservers.net

starting download tests:
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random1500x1500.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random750x750.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random1500x1500.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random750x750.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random750x750.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random750x750.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random1500x1500.jpg
  downloading: http://lg.sea-z.fdcservers.net/speedtest/random1500x1500.jpg
Took 6.10022 seconds to download 22345012 bytes in 8 threads
Download: 27.95 Mbps

starting upload tests:
  uploading size 10000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 10000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 10000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 10000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 400000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 400000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 400000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
  uploading size 400000: http://lg.sea-z.fdcservers.net/speedtest/upload.php
Took 3.437126 seconds to upload 1644080 bytes in 8 threads
Upload: 3.65 Mbps
```
