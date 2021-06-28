qcore
=====

A script to create a podman RHEL8 container to run gdb against RHEL8 userspace core

# usage

    qcore [-h] [-n] -c CORE -i INSTALLED_RPMS [--container-name CONTAINER_NAME] [--remove-container]

# optional arguments

    -h, --help            show this help message and exit
    -c CORE, --core CORE  target core file to analyze
    -i INSTALLED_RPMS, --installed-rpms INSTALLED_RPMS
                          text file which contains the list of the installed packages, i.e., the output of `rpm -qa`
    --container-name CONTAINER_NAME
                          name of container faking up the customer's environment
    --remove-container    remove the container at the end
    --enable-repository ENABLE_REPOSITORY
                          enable dnf repository

# Example

    ./qcore -c ./core.4866 -i ./sosreport/installed-rpms --container-name qcore-bzXXXXXXXX --enable-repository jb-coreservices-1-for-rhel-8-x86_64-rpms

# Author

Hisanobu Okuda hisanobu.okuda@gmail.com
