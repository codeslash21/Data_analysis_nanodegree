
# Gathering Data:


### HTTP (Hypertext Transfer Protocol):

HTTP, the Hypertext Transfer Protocol, is the language that web browsers (like Chrome or Safari) and web servers (basically computers where the contents of a website are stored) speak to each other. Every time you open a web page, or download a file, or watch a video, it's HTTP that makes it possible.

HTTP is a request/response protocol:

- Your computer, a.k.a. the client, sends a request to a server for some file. For this lesson: "Get me the file 1-the-wizard-of-oz-1939-film.txt", for example. GET is the name of the HTTP request method (of which there are multiple) used for retrieving data.
- The web server sends back a response. If the request is valid: "Here is the file you asked for:", then followed by the contents of the 1-the-wizard-of-oz-1939-film.txt file itself.

</br>

<img src="../Images/client-server.png" />


### Create Image:
To create an Image from binary data returned by a request -

```
import requests
from PIL import Image
from io import BytesIO
r = requests.get(url)
i = Image.open(BytesIO(r.content))
```
