##### Best Practices:

- Image size not more than `200MB`
- deployment not more than `15mins`
- Use ahpine images are its very `lightweight`
- Effective `docker layer` usage
- Container should be `self contained`. Should not have external dependancies
- Consistance & repeative. One build - more deployment by `sharing images`
- Log should sent to stdout & stderr. Not to a file. To console. `Built-in log driver`
- Donot use root always. use always specific user with lease privilliges
- Dont use latest tag to avoid confusion when you have multiple versions
- Enable `Docker Content Trust` by enabling its flag
- Keep lesser build files inside the docker. Use `.dockerignore`
- After using apt install command, ensure to clean `"/var/lib/apt/lists/"` downloaded packages. Image size will be reduced by this

