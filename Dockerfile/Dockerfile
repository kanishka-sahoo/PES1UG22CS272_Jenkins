FROM jenkins/jenkins:lts
USER root
RUN apt-get update -o Acquire::ForceIPv4=true \
    && apt-get install -y make \
    && until apt-get install -y g++ g++-12 --fix-missing; do \
           echo "Retrying g++ installation..."; \
           sleep 5; \
       done
USER jenkins

