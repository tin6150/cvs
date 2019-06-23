# Singularity container definition cvs (concurrent version control, client)
# https://github.com/tin6150/cvs/Singularity
#


# trying to get cvs for lrc (to install cmaq)
# need container to run as command cvs, or cmaq build scripts would break

# plan 1: build as docker container, then convert to singularity container.

# n0062.lr6 has singularity 2.6-dist
# lrc-viz   has singularity 2.4-dist :(
# lrc-login, n0000.scs00 ... ??



# new plan: singularity def, but use docker as source, which should be supported in 2.6
# need singularity installed first...


# expect to be using Singularity 2.6
BootStrap: docker
From: alpine:3.6

%runscript
echo "running cvs client from the container:"
cvs "$@"

%post
echo "installing cvs using apk inside the container"
apk update
apk upgrade
apk add cvs

touch /singularity-`date +%Y%m%d-%H%M`

# used https://singularity-hub.org/containers/405 as example/reference


