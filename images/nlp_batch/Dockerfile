FROM ubuntu:latest
MAINTAINER docker@ekito.fr

#copy the nlp batch file in the container 
COPY ./nlp_batch_resources/ /home/nlp_batch/

#create a new floder for log4j logging
RUN mkdir -p /home/nlp_batch/logs/

# Add crontab file in the cron directory
ADD my-crontab /etc/cron.d/nlp-batch-cron

# Give execution rights on the cron job
RUN chmod 0644 /etc/cron.d/nlp-batch-cron

#update package index
RUN apt-get update

#install cron
RUN apt-get -y install cron

#install java jre
RUN apt-get -y install default-jre

# Run the command on container startup
CMD cron -f