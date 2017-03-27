
I was unable to recreate a working Javascript-jasmine image.
For now I am working around this...

Make sure I have the original image
$ docker pull cyberdojofoundation/javascript-node_jasmine

Rename it
$ docker tag cyberdojofoundation/javascript-node_jasmine  cyberdojofoundation/javascript-node_jasmine_original

Push to dockerhub
$ docker push cyberdojofoundation/javascript-node_jasmine_original

Update the Dockerfile to build FROM cyberdojofoundation/javascript-node_jasmine_original
