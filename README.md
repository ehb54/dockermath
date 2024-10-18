## dockermath

A container to run various math & plot related programs
currently gnuplot, octave & maxima

Build dockerfile

`$ cd dockerfile && docker build -t math .`

run osx

`$ docker run -it --rm -e DISPLAY=docker.for.mac.host.internal:0 -v `pwd`:/work math bash`

see [sorny's gist](https://gist.github.com/sorny/969fe55d85c9b0035b0109a31cbcb088) for OSX env setup instructions

run linux

`$ docker run -it --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v `pwd`:/work math bash`

## notes
 - octave is using gnuplot for plotting
    - not ideal, perhaps drivers matching display driver needed or additional libs needed
   
