### Container tags and page structure HTML

HTML provides a set of container tags. Those tags can contain an unspecified set of other tags. 

We have:

 - `article`
 - `section`
 - `div`

The `article` tag identifies a thing that can be independent from other things in a page. For example a list of blog posts in the homepage.

The `section` tag represents a section of a document. Each section has a heading tag ( h1 - h6 ), then the section body.

It’s useful to break a long article into different sections. Shouldn’t be used as a generic container element.

`div` is a generic container element.

#### Page structure tags

The `nav` tag: - This tag is used to create the markup that defines the page navigation. Into this we typically add an `ul` list.

The `aside` tag: -  is used to add a piece of content that is related to the main content. A box where to add a quote, for example. Or a sidebar.

The `header` tag: - represents a part of the page that is the introduction. It can for example contain one or more heading tag ( h1 - h6 ), the tagline for the article, an image.

The `main` tag: - represents the main part of a page.

The `footer` tag: - is used to determine the footer of an article, or the footer of the page.

#### Multimedia Tags

Here we'll learn about `audio` and `video` tags.

The `audio` tag: - This tag allows you to embed audio content in your HTML pages.

This element can stream audio, maybe using a microphone via `getUserMedia()` , or it can play an audio source which you reference using the `src` attribute:

    <audio src="file.mp3"></audio>

By default the browser does not show any controls for this element. Which means the audio will play only if set to `autoplay`.

To show the built-in controls, you can add the `controls` attribute.

Controls can have a custom skin. You can specify the MIME type of the audio file using the type attribute. If not set, the browser will try to automatically determine it.

    <audio src="file.mp3" controls autoplay></audio>

The `loop` attribute restarts the audio playing at 0:00 if set; otherwise, if not present, the audio stops at the end of the file.

Using JavaScript you can listen for various events happening on an audio element, the most basic of which are:

`play` when the file starts playing 
`pause` when the audio playing was 
`paused` playing when the audio is resumed from a pause 
`ended` when the end of the audio file was reached


The `video` tag: - This tag allows you to embed video content in your HTML pages. This element can stream video, using a webcam via `getUserMedia()` or WebRTC, or it can play a video source which you reference using the `src` attribute.

    <video src="file.mp4"></video>

By default the browser does not show any controls for this element, just the video. 

Which means the video will play only if set to `autoplay` and the user can’t see how to stop it, pause it, control the volume or skip to a specific position in the video.

To show the built-in controls, you can add the controls attribute:

    <video src="file.mp4" controls></video>

You can specify the MIME type of the video file using the type attribute. If not set, the browser will try to automatically determine it.

A video file by default does not play automatically. Add the `autoplay` attribute to play the video automatically.

The loop attribute restarts the video playing at 0:00 if set; otherwise, if not present, the video stops at the end of the file.

You can set an image to be the poster image.

    <video src="file.mp4" poster="picture.png"></video>

If not present, the browser will display the first frame of the video as soon as it’s available. 

You can set the `width` and `height` attributes to set the space that the element will take so that the browser can account for it and it does not change the layout when it’s finally loaded. It takes a numeric value, expressed in pixels. 

Using JavaScript you can listen for various events happening on an video element, the most basic of which are:

`play` when the file starts playing 
`pause` when the video was paused 
`playing` when the video is resumed from a pause 
`ended` when the end of the video file was reached

#### iframes

The `iframe` tag allows us to embed content coming from other origins (other sites) into our web page.

    <iframe src="page.html" width="800" height="400"></iframe>

The `srcdoc` attribute lets you specify some inline HTML to show. It’s an alternative to `src` , but recent.

    <iframe srcdoc="<p>My dog is a good dog</p>"></iframe>

