FROM ubuntu:18.04


RUN apt-get update && apt-get install -y python3.6
RUN apt-get install -y python3-venv
RUN apt-get install -y git
RUN apt-get install -y python3-pip
RUN git clone https://github.com/ArttuJanhunen/Kasvikanta
WORKDIR /Kasvikanta
RUN rm runPlants.py
COPY runPlants.py .
RUN python3 -m venv venv
RUN . venv/bin/activate
RUN pip3 install Flask
RUN pip3 install -r requirements.txt

EXPOSE 5000
ENTRYPOINT python3 runPlants.py
