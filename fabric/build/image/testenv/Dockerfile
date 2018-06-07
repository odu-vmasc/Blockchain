# Copyright Greg Haskins All Rights Reserved
#
# SPDX-License-Identifier: Apache-2.0
#
FROM hyperledger/fabric-buildenv:x86_64-1.1.1-snapshot-301c302

# fabric configuration locations
ENV FABRIC_CFG_PATH /etc/hyperledger/fabric

# create needed directories
RUN mkdir -p \
  $FABRIC_CFG_PATH \
  /var/hyperledger/production

# fabric configuration files
ADD payload/sampleconfig.tar.bz2 $FABRIC_CFG_PATH

# fabric binaries
COPY payload/orderer /usr/local/bin
COPY payload/peer /usr/local/bin

# softhsm2
COPY payload/install-softhsm2.sh /tmp
RUN bash /tmp/install-softhsm2.sh && rm -f install-softhsm2.sh

# typically, this is mapped to a developer's dev environment
WORKDIR /opt/gopath/src/github.com/hyperledger/fabric
LABEL org.hyperledger.fabric.version=1.1.1-snapshot-301c302 \
      org.hyperledger.fabric.base.version=0.4.6
