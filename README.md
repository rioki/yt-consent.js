# YouTube GDPR Compliant Embed Code

## Usage

### YouTube Link

The safest thing to do, regarding GDPR and friends, is to never 
embed anything ever. This gives your users the highest level of 
privacy as just talking to other servers can be used to track users.

The code to get the link with preview is the following:

  <div class="yt-link" data-video="dFCbJmgeHmA"></div>;

This widget makes it clear that you will be sent to YouTube and 
once they are there, it's YouTube's problem to comply with privacy 
standards.

### YouTube Embed

Embedding is generally not a problem, as long as you ensure that
informed and explicit consent can be given before any tracking data
is installed. 

The code to get the embed is the following:

  <div class="yt-embed" data-video="-O5kNPlUV7w"></div>

You can set which consent text to show, by specifying the option 
consentText.

### Running the Conversion

At the bottom of you file you want to add the following code:

    <script src="js/yt-consent.js"></script>
    <script>
      ytConsent({
        imagePrefix: '/yt-cache',
        consentText: 'By clicking the play button you consent to <a href="https://policies.google.com/privacy?hl=en">Gogle\'s Privacy Policy.</a>'
      })
    </script>

### Local Thumbnails or YouTube Thumbnails

You can do the 110% thing and pull all thumbnails you need locally and serve them
with your site. They need to be in the format YouTube serves them as:

    <videoid>/sddefault.webp

Then you need to specify the imagePrefix option to tell ytConsent where to look
for the files.

Or you can just use the thumbnails directly from YouTube. There is half an 
argument to be had that this may already violate GDPR, but to get a definite 
answer ask your favorite lawyer or wait for a nicely worded cease and 
desist letter.

### Consent Text

You can change the consent text for embedded videos, by setting consentText 
option. I don't know why you would want to do that, but your lawyer may have
a good reason.

## Example 

See [example.html](example.html)

## License

Copyright 2021 Sean Farrell <sean.farrell@rioki.org>

Permission is hereby granted, free of charge, to any person obtaining a copy of 
this software and associated documentation files (the "Software"), to deal in 
the Software without restriction, including without limitation the rights to 
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies 
of the Software, and to permit persons to whom the Software is furnished to do 
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all 
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, 
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN 
THE SOFTWARE.

## This Party Software

The example contains nomalize.css by Nicolas Gallagher and skeleton.css 
by Dave Gamache. They are only required for the example and not to run 
yt-consent.js.
