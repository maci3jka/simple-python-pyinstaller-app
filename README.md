# Jenkins 101

Based on[Build a Python app with PyInstaller](https://jenkins.io/doc/tutorials/build-a-python-app-with-pyinstaller/)
tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/).

`mkdir ~/meetup_jenkins`

Start jenkins with
```
docker run \
  --rm \
  --name jenkins \
  -u root \
  -p 8080:8080 \
  -v "${HOME}"/meetup_jenkins/jenkins-data:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v "${HOME}"/meetup_jenkins/home:/home \
  jenkinsci/blueocean
```
Setup ssh key in `/root/.ssh` and `chmod 600 b` test connection to server
