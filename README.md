# SubSync
Automatically download subtitles for your movies

I hope this little tool comes to help you out as much as it did for me. My girlfriend and I both struggled with using the VLC Sub addon for downloading subtitles, a tool that we previously been using lots! And when that tool stopped working on later days, keep being unresponsive and continuesly crashing VLC, we had to manually look for those darn subtitles on the web and if you have a lot of shows to watch then its a huge pain in the ass.

SubSync is a tool that will keep your movies folder synchronized with subtitles. That means, if you add a video file to the folder or its subfolders being watched a subtitle will automatically be downloaded for that movie.

It works by using the filename of the movie to determine the name and use that to do a search on subscene.com to find the "first best" subtitle to download. It will then extract the file (if its an archive) and rename it to have the same name as the movie file so it can be quickly recognized as a subtitle using VLC. 

SubSync will also prefer a chosen language over the other, so for me I prefer Swedish but if that one does not exist I want English, you can set this as a startup argument.

## Building SubSync
Load up Visual Studio 2017, open SubSync.sln and hit CTRL+SHIFT+B like your life depends on it!

## Running SubSync
```batch
SubSync.exe <input folder> [<languages>] [<video extensions>]

<input folder>: So this is the folder you want to watch, it will also watch all its subfolders.
                As an example: 'D:\Movies'

<languages>: A list of languages separated by a semi-colon. Example: swedish;english
             The priority of the languages is from left to right, so in this example if 
             a swedish translation subtitle is available it will take that one rather 
             than the english one.

             The value is just English per default.

<video extensions>: A list of video extensions to watch seperated by a semi-colon, just add
                    all you can think of. But this is an optional and default value is:
                    *.avi;*.mp4;*.mkv;*.mpeg;*.flv;*.webm
```

Now keep it running in the background. Its not going to hog up your cpu. Its pretty friendly, and you can be sure to have subtitles available for you whenever you need it!

## Tips and tricks
Press 'q' at any time to exit SubSync

Press 'a' to try and re-sync any previously unsyced subtitles. Yes the subtitle downloads can randomly fail some times when subscene.com decides you shouldnt be downloading their subtitles too often.

Oh, and be sure to bring popcorns or your favorite snacks when watching your movies!