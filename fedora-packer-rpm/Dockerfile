FROM fedora:35

RUN dnf update -y -q \
    && dnf groupinstall -q -y "RPM Development Tools" \
    && dnf install -q -y fedora-packager rpmdevtools gcc sudo \
    && dnf clean all \
    && adduser freddy \
    && echo "freddy ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/freddy \
    && chmod 0440 /etc/sudoers.d/freddy

#RUN su - freddy -c "touch mine"

#CMD ["su", "-", "freddy", "-c", "/bin/bash"]
CMD ["su", "-", "freddy"]