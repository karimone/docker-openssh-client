# docker-ssh-rsync

This docker image based on alpine linux with installed openssh client and rsync.

This is image is quite useful on the CI to deploy. 
I personally use it with blog static generator like [Hugo](https://gohugo.io/) and [Pelican](https://blog.getpelican.com/)

### Details
The ssh is configured in the docker using the optional env variable `SSH_DEPLOY_KEY` as private key. Check the file `bin/entrypoint.sh` for the details.

Also the ssh client is configured with the following options:

- Strict host key checking is disabled.
- Agent forwarding is enabled.
