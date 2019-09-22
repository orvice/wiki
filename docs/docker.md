# Docker

## Install



## Clean

```
docker rmi $(docker images -q -f dangling=true)
```