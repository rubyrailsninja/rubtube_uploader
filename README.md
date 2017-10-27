== rutube

Uploads video files into site http://rutube.ru

Make sure you have an account on that site.
You can sign up on http://rutube.ru/accounts/register/


== Usage

  require 'rubygems'
  require 'rutube'

  uploader = Rutube::Uploader.new('username@example.com', 'p455w0rd')
  uploader.login  # returns true on success
  result = uploader.upload :title => 'my winter holidays',
                           :description => 'wonderful memories',
                           :path => '/tmp/my_video.avi',
                           :privacy => 'public'

  # find URL of your video by the title
  uploader.find_video_url('my winter holidays')
  # find URL of your last uploaded and processed video file
  uploader.latest_video_url


== Requirements

* json (tested with json-1.7.4 gem)
* mechanize (tested with mechanize-2.5.1 gem)


== Installation

  gem install rutube


== Author

Iwakura Taro, taro@mail333.com


== License

Application is released under the terms of the BSD License.
See the License file for details.
