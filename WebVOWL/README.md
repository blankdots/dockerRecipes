## DockerRecipe for WebVOWL

Docker recipe for WebVOWL.

Author: http://blankdots.com

### Build Instructions

In the WebVOWL after docker has been installed and configured run on separately:

```
docker build -t blankdots/webvowl .
docker images
docker run -p dockerip:49159:8000 -i -t blankdots/webvowl
```
In your browser go to:
```
dockerip:49159
```

Cleaning all the containers and images:
```
docker rm $(docker ps -a -q)
docker rmi $(docker images -q)
```

Using bash inside the container:
```
docker run -i -t blankdots/webvowl bash
```

### Licenses

The MIT License (MIT)

Copyright (c) 2015 blankdots@gmail.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.