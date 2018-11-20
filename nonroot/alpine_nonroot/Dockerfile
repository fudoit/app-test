FROM alpine

#create our new user
RUN adduser -S tester

#set the workdir
WORKDIR /home/tester

#switch to user "tester"
USER tester

#run main process
ENTRYPOINT ["top"]

