FROM k8s.gcr.io/pause as pause
FROM r.j3ss.co/amicontained as amicontained
FROM gliderlabs/alpine:latest
COPY --from=pause /pause /pause
COPY --from=amicontained /usr/bin/amicontained /usr/bin/amicontained
RUN apk-install openssl bash bash-completion ca-certificates
CMD ["/pause"]
