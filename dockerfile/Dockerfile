FROM debian:latest

RUN apt-get update
RUN apt-get install -y gnuplot
RUN apt-get install -y octave
RUN apt-get install -y maxima

# also bit's for my convenience

# like to have x functions to test display
RUN apt-get install -y x11-apps

# my editor
RUN apt-get install -y emacs-nox

# some cli utils & my .emacs file
RUN apt-get install -y git
RUN git clone https://github.com/ehb54/convenience
RUN cd convenience && bash -x installcont.sh
RUN rm -fr convenience

# trying to get octave plotting to work, these might help:

RUN apt-get install -y mesa-utils libgl1-mesa-glx
# RUN apt-get install -y mesa-*

# plot display for octave seems problematic
# using gnuplot for it

RUN echo 'graphics_toolkit("gnuplot");' > ~/.octaverc

# setup /work

RUN mkdir /work
WORKDIR /work
