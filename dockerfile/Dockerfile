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
