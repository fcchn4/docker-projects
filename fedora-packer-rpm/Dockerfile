FROM fedora:35

RUN dnf update -y -q \
    && dnf groupinstall -q -y "RPM Development Tools" \
    && dnf install -q -y fedora-packager \
    && dnf clean all

