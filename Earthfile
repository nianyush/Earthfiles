VERSION 0.6

FROM scratch

fs:
    ARG image=fs:latest
    FROM scratch
    COPY . /
    SAVE IMAGE --push ${image}
