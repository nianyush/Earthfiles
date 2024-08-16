VERSION 0.8

FROM scratch

fs:
    ARG image=fs:latest
    FROM scratch
    COPY . /
    SAVE IMAGE --push ${image}
