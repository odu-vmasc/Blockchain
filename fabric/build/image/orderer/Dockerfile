# Copyright Greg Haskins All Rights Reserved
#
# SPDX-License-Identifier: Apache-2.0
#
FROM hyperledger/fabric-baseos:x86_64-0.4.6
ENV FABRIC_CFG_PATH /etc/hyperledger/fabric
RUN mkdir -p /var/hyperledger/production $FABRIC_CFG_PATH
COPY payload/orderer /usr/local/bin
ADD payload/sampleconfig.tar.bz2 $FABRIC_CFG_PATH/
EXPOSE 7050
CMD ["orderer"]
LABEL org.hyperledger.fabric.version=1.1.1-snapshot-301c302 \
      org.hyperledger.fabric.base.version=0.4.6
