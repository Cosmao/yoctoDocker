### Docker container to build yocto
Probably has way too much installed but it worked for me

## Step 1
`docker-compose up` \
This step takes a minute or so, give it time to download everything

## Step 2
SSH into the container \
`ssh yocto@localhost -p 2222` \
Password is yocto

## Step 3
Clone poky \
`git clone git://git.yoctoproject.org/poky && cd poky`

## Step 4
init the build env \
`source oe-init-build-env`

## Step 5
Bake the bits \
`bitbake -k core-image-minimal`
