# Kali Console

## What is kali-console?

Kali Console is a container that has common KaliLinux tools installed to use from the command line.

- https://www.kali.org/

## How to use this image

For download image:

```sh
    docker pull fcch/kali-console:latest
```

Run container:

```sh
    docker run --name kali -it fcch/kali-console:latest bash
```

## How to use this image with volumes

Create volume:

```sh
    docker volume create kali-rootdir
```

Run container + volume:

```sh
    docker run --name kali -v kali-rootdir:/root:rw -it fcch/kali-console:latest bash
```

## Return container created

List containers: 

```sh 
    docker ps -a
```

Start container: 

```sh
    docker start kali
```

Enter to container: 

```sh 
    docker exec -it kali bash
```
