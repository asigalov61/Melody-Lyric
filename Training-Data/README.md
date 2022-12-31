# Melody Lyric Training Data

***

## Based upon ~ 2400 English Karaoke MIDIs

***

## Decode as follows:

```
out2 = SONG

if len(out2) != 0:
    
    song = out2
    song_f = []
    time = 0
    dur = 0
    vel = 0
    pitch = 0
    channel = 0
                    
    for ss in song:

      time += ss[1] * 20

      dur = ss[2] * 20
      vel = 90
   
      channel = 0
      pitch = ss[0]
                      
      song_f.append(['note', time, dur, channel, pitch, vel ])

    detailed_stats = TMIDIX.Tegridy_SONG_to_MIDI_Converter(song_f,
                                                        output_signature = 'Melody Lyric',  
                                                        output_file_name = '/content/Melody-Lyric-Music-Composition', 
                                                        track_name='Project Los Angeles',
                                                        list_of_MIDI_patches=[0, 24, 32, 40, 42, 46, 56, 71, 73, 0, 53, 19, 0, 0, 0, 0],
                                                        number_of_ticks_per_quarter=500)

    print('Done!')
```

***

### Project Los Angeles
### Tegridy Code 2022
