# au

A thin wrapper around [ffmpeg](http://www.ffmpeg.org/) to make it easier to perform common audio manipulations like cutting to a specific number of beats at a set BPM, volume adjustments, joining files together, and converting between file formats or between mono and stereo.

### Setup

1. install ffmpeg
2. save the `au` file to your `~/bin` folder
3. chmod the file to be executable:

         chmod u+x ~/bin/au

You're all set.

### Available commands

    au cut    input.wav 120 16 ouput.wav                     # cut file to specified bpm*beats for making loops
    au join   file1.wav file2.wav [...file3.wav] output.wav  # join files together to make one audio file
    au vol    input.wav 0.5 output.wav                       # adjust the volume of a file
    au mp3    input.wav output.mp3                           # convert to an mp3 of the same name
    au wav    input.aif output.wav                           # convert to a wav of the same name
    au mono   stereo.wav mono.wav                            # convert stereo to mono
    au stereo mono.wav stereo.wav                            # convert mono to stereo

### Exampes

    # cut verses.wav to 4 bars at 132bpm
    au cut verses.wav 132 16 verses-cut.wav
    
    # convert aif to wav (saves to verses.wav)
    au wav verses.aif
    
    # halve the volume of a clip (overwrites verses.aif)
    au vol verses.aif 0.5
    
    # join some files together as song.wav
    au join verse.wav chorus.wav verse.wav song.wav
