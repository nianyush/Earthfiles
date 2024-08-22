VERSION 0.8

FROM scratch

ARG image=fs:latest

fs:
    FROM scratch
    COPY . /
    SAVE IMAGE --push ${image}

disk:
    ARG file
    FROM scratch
    COPY ${file} /disk/
    SAVE IMAGE --push ${image}
