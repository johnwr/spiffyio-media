# spiffyio-media
A slice out of the spiffyio repository, in particular for processing media.

There are a lot of private libraries (and services) which help power this code base, but without opening spiffyio's entire organization up to the public (~250K lines of code) then there would always be another missing section of code. This code base is done in Java with Spring Framework, Hibernate and backed by MySQL, SNS, SQS, S3 with a CloudFront distribution. It was deployed via AWS ElasticBeanstalk application on a Tomcat server.

Generally, this microservice powered taking the raw uploads from users, and scrubbing the data and storing them for later retrieval; i.e. uploading a video and processing the WebM and MP4 versions (with reasonable compression), or taking images and removing exif data.

The contents was then publicly accessible via `https://cdn.spiffy.io/media/**`
