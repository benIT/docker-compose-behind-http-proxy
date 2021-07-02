# About

This project has been created to debug errors encountered with docker-compose and our corporate http proxy server.

Source: [original discussion on `stackoverflow.com`.](https://stackoverflow.com/questions/68197663/curl-is-working-on-host-machine-but-not-in-container)

NB: `*.crt` files have been voluntarily ignored from this git repo.

# Test

Check curl request runs on host machine:

    curl -s https://example.com/ > /dev/null
    
Check curl request runs in docker container :

    docker-compose build --no-cache
    
And check if there are SSL errors like `SSL certificate problem: unable to get issuer certificate`.