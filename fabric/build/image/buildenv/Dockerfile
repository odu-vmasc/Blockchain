# Copyright Greg Haskins All Rights Reserved
#
# SPDX-License-Identifier: Apache-2.0
#
FROM hyperledger/fabric-baseimage:x86_64-0.4.6
COPY payload/protoc-gen-go /usr/local/bin/
ADD payload/gotools.tar.bz2 /usr/local/bin/
# temporary fix for https://github.com/golang/go/issues/21373
RUN go install -a std
LABEL org.hyperledger.fabric.version=1.1.1-snapshot-301c302 \
      org.hyperledger.fabric.base.version=0.4.6
