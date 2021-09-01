This repo provides a reproduction of a bug in Active Storage. When creating an AVIF variant of an image, the new blob is assigned the wrong content type. This can be seen in the Network tab of devtools when viewing the image variant.

Note: You will need ImageMagick with the HEIF module installed on your system. To check if you have this installed, run `identify -list format` and look for AVIF in the first column of output.

1. `git clone https://github.com/brian-kephart/avif.git`
1. `cd avif`
1. `bundle install`
1. `rails db:migrate`
1. `rails s`
1. [http://localhost:3000](http://localhost:3000)
