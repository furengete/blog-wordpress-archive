---
title: "youtube-dl"
date: "2020-04-07"
---

[youtube-dl](https://github.com/ytdl-org/youtube-dl) is a Command-line program to download videos from YouTube.com and other video sites.

[Here](https://ytdl-org.github.io/youtube-dl/supportedsites.html)'s is the list of all the supported sites, ordered alphabetically.

* * *

Today, I am going to talk about which codec I prefer to download from YouTube. But one thing I am still confusing: should I download video and audio then merge them into a container like mp4/mkv/webm or just leave them as it is? at the moment, I would not to merge them if the resolution of the original video is above 720p.

First of all, what is codec?

https://www.youtube.com/watch?v=Tk8ehIY8\_2A

https://www.youtube.com/watch?v=sisvOeZItb0

To be clear, the defination of codec is compressor and decompressor.

once you type in the command line as follow

```
youtube-dl --list-format https://www.youtube.com/watch?v=***********
```

you will see the following

```
[youtube] ***********: Downloading webpage
[info] Available formats for ***********:
format code  extension  resolution note
249          webm       audio only tiny   58k , opus @ 50k (48000Hz), 2.01MiB
250          webm       audio only tiny   78k , opus @ 70k (48000Hz), 2.68MiB
140          m4a        audio only tiny  130k , m4a_dash container, mp4a.40.2@128k (44100Hz), 5.21MiB
251          webm       audio only tiny  150k , opus @160k (48000Hz), 5.29MiB
394          mp4        256x144    144p   83k , av01.0.00M.10.0.110.09.16.09.0, 30fps, video only, 2.77MiB
278          webm       256x144    144p   98k , webm container, vp9, 30fps, video only, 3.65MiB
160          mp4        256x144    144p  111k , avc1.4d400c, 30fps, video only, 2.67MiB
395          mp4        426x240    240p  191k , av01.0.00M.10.0.110.09.16.09.0, 30fps, video only, 5.68MiB
242          webm       426x240    240p  228k , vp9, 30fps, video only, 7.59MiB
133          mp4        426x240    240p  245k , avc1.4d4015, 30fps, video only, 5.69MiB
330          webm       256x144    144p60 HDR  245k , vp9.2, 60fps, video only, 8.72MiB
396          mp4        640x360    360p  347k , av01.0.01M.10.0.110.09.16.09.0, 30fps, video only, 10.59MiB
243          webm       640x360    360p  422k , vp9, 30fps, video only, 14.19MiB
331          webm       426x240    240p60 HDR  517k , vp9.2, 60fps, video only, 18.91MiB
134          mp4        640x360    360p  633k , avc1.4d401e, 30fps, video only, 17.17MiB
397          mp4        854x480    480p  651k , av01.0.04M.10.0.110.09.16.09.0, 30fps, video only, 20.00MiB
244          webm       854x480    480p  785k , vp9, 30fps, video only, 26.42MiB
332          webm       640x360    360p60 HDR 1064k , vp9.2, 60fps, video only, 40.80MiB
398          mp4        1280x720   720p60 1295k , av01.0.08M.10.0.110.09.16.09.0, 60fps, video only, 41.41MiB
135          mp4        854x480    480p 1351k , avc1.4d401f, 30fps, video only, 35.59MiB
247          webm       1280x720   720p 1588k , vp9, 30fps, video only, 53.74MiB
333          webm       854x480    480p60 HDR 1988k , vp9.2, 60fps, video only, 77.26MiB
399          mp4        1920x1080  1080p60 2237k , av01.0.09M.10.0.110.09.16.09.0, 60fps, video only, 74.32MiB
302          webm       1280x720   720p60 2667k , vp9, 60fps, video only, 89.04MiB
136          mp4        1280x720   720p 2698k , avc1.4d401f, 30fps, video only, 70.39MiB
248          webm       1920x1080  1080p 2772k , vp9, 30fps, video only, 94.90MiB
298          mp4        1280x720   720p60 4201k , avc1.4d4020, 60fps, video only, 115.83MiB
303          webm       1920x1080  1080p60 4486k , vp9, 60fps, video only, 154.48MiB
334          webm       1280x720   720p60 HDR 4529k , vp9.2, 60fps, video only, 176.99MiB
137          mp4        1920x1080  1080p 5065k , avc1.640028, 30fps, video only, 130.39MiB
335          webm       1920x1080  1080p60 HDR 6923k , vp9.2, 60fps, video only, 271.72MiB
299          mp4        1920x1080  1080p60 7007k , avc1.64002a, 60fps, video only, 204.42MiB
400          mp4        2560x1440  1440p60 7651k , av01.0.12M.10.0.110.09.16.09.0, 60fps, video only, 249.32MiB
271          webm       2560x1440  1440p 8977k , vp9, 30fps, video only, 297.43MiB
308          webm       2560x1440  1440p60 13368k , vp9, 60fps, video only, 448.85MiB
401          mp4        3840x2160  2160p60 15790k , av01.0.13M.10.0.110.09.16.09.0, 60fps, video only, 501.33MiB
336          webm       2560x1440  1440p60 HDR 16746k , vp9.2, 60fps, video only, 651.85MiB
313          webm       3840x2160  2160p 17965k , vp9, 30fps, video only, 644.01MiB
402          mp4        7680x4320  4320p60 23104k , av01.0.17M.10.0.110.09.16.09.0, 60fps, video only, 599.29MiB
315          webm       3840x2160  2160p60 26684k , vp9, 60fps, video only, 988.10MiB
337          webm       3840x2160  2160p60 HDR 30553k , vp9.2, 60fps, video only, 1.13GiB
272          webm       7680x4320  4320p60 31980k , vp9, 60fps, video only, 830.57MiB
571          mp4        7680x4320  4320p60 34531k , av01.0.17M.10.0.110.09.16.09.0, 60fps, video only, 918.43MiB
18           mp4        640x360    360p  667k , avc1.42001E, mp4a.40.2@ 96k (44100Hz), 26.87MiB
22           mp4        1280x720   720p 1877k , avc1.64001F, mp4a.40.2@192k (44100Hz) (best)
```

the available audio codec including opus, m4a  
the available video codec including avc1, vp9, av01

you choose which one you prefer then type the code.  
I like mp4 container, I will choose to download the best quality with avc1+m4a codec.

```
# merge
youtube-dl -f 137+140 https://www.youtube.com/watch?v=***********

# don't merge
youtube-dl -f 137/136/135,140 https://www.youtube.com/watch?v=***********

# if it doesn't work, type

youtube-dl -f best http://www.youtube.com/watch?v=***********
# or
youtube-dl -f 22/18 http://www.youtube.com/watch?v=***********
```

If the video resolution is higher than 1080p, I have to choose vp9 codec due to [youtube settings](https://motovlog.com/threads/making-1080p60-look-like-4k-by-getting-youtubes-bigger-bit-rate.17619/#post-153441), I will type as following, because mkv doesn't hurt.

```
youtube-dl --merge-output-format mkv https://www.youtube.com/watch?v=***********

# hate webm? use
-f bestvideo[ext!=webm]‌​+bestaudio[ext!=webm]‌​/best[ext!=webm]
```

* * *

merge or not, is a question still remains, at the moment, I don't care at all.  
But one thing that crucial, I never download meaningless videos, I only download educational videos.  
If it's a lecture, I would merge.  
If it's a vlog, I don't care the container but the content and resolution.

what is container?

https://www.youtube.com/watch?v=O9qvIfJRH3s

Honestly, if I had enough storege I would back up all of the channels that I subscribed.  
lectures and vlogs are two huge parts on youtube right now, it is also a trend on other video site.

* * *

more [discussion](https://stackoverflow.com/questions/31631535/youtube-dl-dash-video-and-audio-in-highest-quality-without-human-intervention) on stackoverflow.com
