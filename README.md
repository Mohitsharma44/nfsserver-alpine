## NFSServer-alpine

NFS v4 server on top of Alpine container image.


### To run:

** docker-compose **:

- Create a directory that you want to share
- Add the path to the directory in the docker-compose.yml file
  ``` bash
  volume:
      - <directory you want to share>:/nfsshare
  ```
- docker-compose up

** docker run **:
`docker run -d --name nfs --privileged -v <directory you want to share>:/nfsshare -e SHARED_DIRECTORY=/nfsshare -p 2049:2049 --restart always mohitsharma44/nfsserver-alpine:latest`


### Credits
The repo is adapted from Steven Iveson's [nfs-server-alpine](https://github.com/sjiveson/nfs-server-alpine)


### License
MIT License

Copyright (c) 2019 Mohit

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
