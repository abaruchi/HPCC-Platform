##############################################################################
#
#    HPCC SYSTEMS software Copyright (C) 2020 HPCC Systems®.
#
#    Licensed under the Apache License, Version 2.0 (the "License");
#    you may not use this file except in compliance with the License.
#    You may obtain a copy of the License at
#
#       http://www.apache.org/licenses/LICENSE-2.0
#
#    Unless required by applicable law or agreed to in writing, software
#    distributed under the License is distributed on an "AS IS" BASIS,
#    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
#    See the License for the specific language governing permissions and
#    limitations under the License.
##############################################################################

# Build container image for a single ESP server

ARG BUILD_LABEL
ARG DOCKER_REPO
FROM ${DOCKER_REPO}/platform-core:${BUILD_LABEL}

USER hpcc
RUN mkdir -p /var/lib/HPCCSystems/esp
WORKDIR /var/lib/HPCCSystems/esp
COPY --chown=hpcc:hpcc esp.xml /var/lib/HPCCSystems/esp
#RUN esp --init
ENTRYPOINT ["esp"]

