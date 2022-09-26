# Reversi - Reverse Internet Monitor App

I wanted a way to monitor my home Internet connection from _outside_ my home. That way, I can not only check up on the status from outside (without relying on my home Internet connection being up), but also alert on changes externally (internal alerting tools won't help me if I'm not at home...).

Informal task list:

  - [ ] Endpoint that receives an IP address and writes timestamp + IP to a database table.
  - [ ] Cron job that runs every 5 minutes or so, and if there is no new record in the past 5 minutes, and alert has not been sent, sends alert (ideally SMS, but email okay for starters). Also, if IP address has changed between the last record and n-1, alert on that.
  - [ ] Endpoint that is password-protected (e.g. index.php) to see last timestamp of up, and last IP address (and maybe show table of last n results from database table).

## Local development

This project includes a Dockerfile to build a Docker container inside which you can develop and test the application.

To run it, make sure you have Docker installed, then run:

    docker-compose up -d

TODO.