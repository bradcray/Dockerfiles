
[Take me to the cyber-dojo home page](https://github.com/cyber-dojo/cyber-dojo).

- - - -

[![Build Status](https://travis-ci.org/cyber-dojo/Dockerfiles.svg?branch=master)](https://travis-ci.org/cyber-dojo/Dockerfiles)

<img src="https://raw.githubusercontent.com/cyber-dojo/nginx/master/images/home_page_logo.png" alt="cyber-dojo yin/yang logo" width="50px" height="50px"/>

Separated out from start-points-languages repo to keep the later's size down
to decrease the time it takes to do a

```
$ ./cyber-dojo start-point create ... --git=https://github.com/cyber-dojo/start-point-languages.git
```

command from a cyber-dojo server.

- - - -

Once all the docker images now have a working embedded red_amber_green.rb file.
I plan to start splitting up this repo.
Each language+testFramework will
- have a dedicated repo which will
combine the two parts currently split between this repo and the
[start-points-languages](https://github.com/cyber-dojo/start-points-languages) repo.
- have a .travis.yml file which will build and test the image and push it to dockerhub

