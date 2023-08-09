FROM alpine:3.18.3 AS phase1
ENV A=1
RUN cp /tmp/test.txt /done.txt #!COMMIT


FROM alpine:3.18.3 AS phase2
ENV A=1
RUN cp /tmp/test.txt /done.txt #!COMMIT
RUN rm /done.txt


FROM alpine:3.18.3 AS phase3

# Generate a few empty layers.
RUN mkdir /test #!COMMIT
WORKDIR /test #!COMMIT
RUN ls /test #!COMMIT

COPY --from=phase1 /done.txt /done.txt
ENTRYPOINT ["/bin/sh", "-c", "cat /done.txt"]
