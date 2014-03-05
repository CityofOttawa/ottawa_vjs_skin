### Video JS player settings:

id: Must be a distinct machine readable name.
classes: For the City of Ottawa default, make sure vjs-ottawa-skin remains as a class.

The following settings are added to the `<video>` tag. If the setting is a boolean (on/off),
only add the setting's name to the tag to turn it on.
See https://github.com/videojs/video.js/blob/v4.3.0/docs/guides/options.md for more details.

* controls: Allows for the player to have controls (play/pause/scrub/fullscreen/etc...).
* autoplay: Starts the video on page load.
* preload:  Informs the browser on whether or not the video should begin loading on page load. Options: auto, metadata, and none.
* poster:   A preview image to display before the video begins playing.
* loop:     Causes the video to play again as soon as it ends.
* width:    The width of the video player. Make sure it is set to auto for responsiveness.
* height:   The height of the video player. Make sure it is set to auto for responsiveness.

### Source settings:

The following settings are added to the `<source>` tag.

* src:      The path to the live video file.
* type:     The format that the video has been encoded in. It is recommended to have different types to fallback on.
            Recommended types are: 'video/mp4', 'video/webm', 'video/ogg'.

### Track settings:

The following settings are added to the `<track>` tag.
Remove this tag if no track is needed.
See https://github.com/videojs/video.js/blob/v4.3.0/docs/guides/tracks.md for more details.

* kind:     One of the following track types: subtitles, captions, chapters, descriptions, metadata. Defaults to subtitles if nothing is entered.
* src:      The path to the live track file (.vtt format).
* label:    The label that will be displayed to the user. ie: In a menu that will list different subtitles based on language.
* default:  Used to have a track default to showing. For chapters, default is required.
* srclang:  A valid BCP 47 language tag for the language of the track.

### The following is an example videojs embed:

    <video id="example_video_1" class="video-js vjs-default-skin vjs-ottawa-skin vjs-big-play-centered" controls preload="none" width="auto" height="auto" data-setup="{}" poster="http://video-js.zencoder.com/oceans-clip.png">
    <source src="http://video-js.zencoder.com/oceans-clip.mp4" type='video/mp4' />
    <source src="http://video-js.zencoder.com/oceans-clip.webm" type='video/webm' />
    <source src="http://video-js.zencoder.com/oceans-clip.ogv" type='video/ogg' />

    <track kind="captions" src="http://example.com/path/to/captions.vtt" srclang="en" label="English" default>
    </video>