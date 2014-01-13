# au

A thin wrapper around [ffmpeg](http://www.ffmpeg.org/) to make it easier to perform common audio manipulations like cutting to a specific number of beats at a set BPM, volume adjustments, joining files together, and converting between file formats or between mono and stereo.

### Setup

1. install ffmpeg
2. save the `au` file to your `~/bin` folder
3. chmod the file to be executable:

         chmod u+x ~/bin/au

You're all set.

### Available commands

    cut       cut file to specified bpm*beats for making loops
    join      join files together to make one audio file
    vol       adjust the volume of a file
    mp3       convert to an mp3 of the same name
    wav       convert to a wav of the same name
    mono      convert stereo to mono
    stereo    convert mono to stereo

### Exampes

    # cut verses.wav to 4 bars at 132bpm
    au cut verses.wav 132 16 verses-cut.wav
    
    # convert aif to wav
    au wav verses.aif
    
    # halve the volume of a clip
    au vol verses.aif 0.5
    
    # join some files
    au join verse.wav chorus.wav verse.wav song.wav
