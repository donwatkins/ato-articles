# Saving vintage recordings with Linux

Learn how to convert media files with FFmpeg

**By Don Watkins**  
**Published:** May 2, 2024  
**Source:** [https://allthingsopen.org/articles/save-recordings-ffmpeg](https://allthingsopen.org/articles/save-recordings-ffmpeg)

<figure class="featured">
<img src="https://allthingsopen.org/wp-content/uploads/2024/04/editing-video-sound-e1713888379286.jpg" class="featured" alt="Person editing video and audio with various speakers on a desk" />
<figcaption>Image by <a href="https://pixabay.com/users/popmelon-15508150/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=8622087">Amore Seymour</a> from <a href="https://pixabay.com//?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=8622087">Pixabay</a></figcaption>
</figure>

Recently, a customer asked me to create compact discs of priceless family recordings. My client insisted that the media be delivered as compact discs and not as digital files in an MP3 player or other similar device. One of the source recordings was on a compact disc and in *AIFF* format. As such my client could not play this media that contained her husband’s voice. I was able to convert it using <a href="https://www.audacityteam.org/" target="_blank" rel="noreferrer noopener nofollow">Audacity</a>, and then was able to burn it to a compact disc with Brasero, which has been my go to CD creation tool.

The balance of the audio files were in MP3 format. I was able to create compact discs with Brasero very quickly. However, one file was so large that it exceeded the capacity of the compact disc medium. This large file contained nearly two hours of audio. The capacity of compact discs is 72 minutes.

This presented a problem. How could I split the large file into smaller segments that would allow me to create media and fit on media that my client could use? I decided to use a DVD instead of a compact disc. Using a DVD provided me with a much larger capacity disc, but how could I convert the MP3 files to a format that would allow me to create a DVD? I tried using HandBrake, but was unable to convert MP3 to MP4 format because MP4 expected a video stream, and I had no video. Then I discovered that I could use <a href="https://ffmpeg.org/" target="_blank" rel="noreferrer noopener nofollow">FFmpeg</a> to convert the files.

## **How to convert media files with FFmpeg**

If you’re looking for a powerful tool to help you with your audio and video files, look no further than `FFmpeg`. `FFmpeg` is highly versatile and able to support an impressive range of popular formats like MP3, MP4, and AVI. You can also use it to convert files between different formats, which was very useful in my case.

You can easily install `FFmpeg` on your Linux system in a terminal on Fedora and similar distributions:

``` wp-block-prismatic-blocks
$ sudo dnf install ffmpeg
```

On Debian and similar distributions:

``` wp-block-prismatic-blocks
$ sudo apt install ffmpeg
```

According to its man page, “`FFmpeg` is a very fast video and audio converter that can also grab from a live audio and video source. It can also convert between arbitrary sample rates and resize video on the fly with a high-quality polyphase filter.” `FFmpeg` has excellent [documentation](https://ffmpeg.org/ffmpeg.html) and an extensive man page.

The command-line interface of this tool might seem daunting for newcomers, but this feature is what makes it so powerful. Developers and system administrators can easily write scripts to automate complex tasks. If you make the most of this feature you can streamline your workflow like a pro.

Using the command-line interface, I was able to convert the MP3 file to the required MP4 format using the following command:

``` wp-block-prismatic-blocks
$ ffmpeg -f lavfi -i color=c=black:s=1280x720:r=5 -i audio.mp3 -crf 0 -c:a copy -shortest output.mp4
```

The `-f lavfi` option sets a virtual input device as the source of the video stream. Essentially, this creates a video file (which a video DVD requires) instead of an audio file. The audio file I actually care about gets included thanks to the `-i audio.mp3` option. The video that gets created is a black screen, as defined by `-i`:

``` wp-block-prismatic-blocks
color=c=black:s=1280x720:r=5
```

I ran into a snag using Brasero with this new MP4 file. Brasero would not create a DVD without the addition of a couple of `cstreamer` codec. From some quick research, I found another open source DVD creation program called [DevedeNG](https://www.rastersoft.com/programas/devede.html) that had everything I needed built-in. Upon installing the DevedeNG program, I was able to create the DVD media in 20 minutes. Your time may vary, depending on your computer system.

## **Solving problems with open source**

[DevedeNG](https://gitlab.com/rastersoft/devedeng) is licensed under [GPLv3](https://www.gnu.org/licenses/gpl-3.0-standalone.html), while `FFmpeg` is licensed under the [GNU Lesser Public License (LGPLv2)](http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html). `FFmpeg` is always evolving. The project is actively maintained and updated regularly, giving you the latest features, improvements, and bug fixes so you can rest easy knowing your audio and video formats are supported.

Another way I could have resolved the space issue was by burning the MP3 audio as data files onto the DVD, leveraging the 4 GB of space available on the DVD for just the audio data. The DVD would have basically been, in that scenario, a hard drive. You’d insert it into your computer and listen to the MP3 file through music player software.

The way I ended up burning the audio DVD created a media DVD, which is recognized by either a computer or a DVD player. Because there’s an “empty” video stream (it’s actually not empty, it has black pixels in it), DVD players recognize the media as a movie. This means that when you listen to the audio track, you’re actually watching a blank video with accompanying audio.

There’s no right or wrong way to solve these puzzles. What’s important is that you know how to get to the place you need to be. The goal was to preserve audio that was of particular importance to my client, and open source made it possible.

</div>

---

<div class="cc-license">

<a href="https://creativecommons.org/licenses/by-sa/4.0/" rel="license"><img src="https://allthingsopen.org/wp-content/themes/ato-main-2024/img/cc/by-sa.png" title="This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License." alt="Creative Commons License" /></a>

This work is licensed under a Creative Commons Attribution-Share Alike 4.0 International License.

