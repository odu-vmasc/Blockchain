# Copyright Greg Haskins All Rights Reserved
#
# SPDX-License-Identifier: Apache-2.0
#
FROM hyperledger/fabric-baseimage:x86_64-0.4.6
ENV FABRIC_CFG_PATH /etc/hyperledger/fabric
VOLUME /etc/hyperledger/fabric
ADD  payload/sampleconfig.tar.bz2 $FABRIC_CFG_PATH
COPY payload/cryptogen /usr/local/bin
COPY payload/configtxgen /usr/local/bin
COPY payload/configtxlator /usr/local/bin
COPY payload/peer /usr/local/bin
LABEL org.hyperledger.fabric.version=1.1.1-snapshot-301c302 \
      org.hyperledger.fabric.base.version=0.4.6
