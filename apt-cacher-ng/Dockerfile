FROM zhusj/apt-cacher-ng:202210191826
LABEL Add gpg KEY: 871920D1991BC93C 3B4FE6ACC0B21F32
RUN apt-get update && apt-get install gnupg gnupg2 -y \
    && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv 3B4FE6ACC0B21F32 \
    && gpg --export --armor 3B4FE6ACC0B21F32 | apt-key add - \
    && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv 871920D1991BC93C \
    && gpg --export --armor 871920D1991BC93C | apt-key add -
#CMD ["/bin/bash"]