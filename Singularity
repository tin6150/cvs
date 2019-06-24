# Singularity container definition cvs (concurrent version control, client)
# https://github.com/tin6150/cvs/Singularity
# https://www.singularity-hub.org/collections/3206

# usage:
# singularity pull shub://tin6150/cvs
# ln -s tin6150-cvs-master-latest.simg cvs
# export PATH=$PATH:/global/scratch/tin/singularity-repo
# cvs help

# expect to be using Singularity 2.6
# singularity-hub seems to be using Singularity 2.5
BootStrap: docker
From: alpine:3.6

%runscript
#--echo "running cvs client from the container:"
cvs "$@"

%post
echo "installing cvs using apk inside the container"
apk update
apk upgrade
apk add cvs

touch /singularity-`date +%Y%m%d-%H%M`

# used https://singularity-hub.org/containers/405 as example/reference


# n0062.lr6 has singularity 2.6-dist
# lrc-viz   has singularity 2.4-dist :(
# lrc-login, n0000.scs00 ... ??

