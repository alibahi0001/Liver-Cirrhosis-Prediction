# Copyright 2024 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

ARG NODE_VERSION=22.9.0-alpine3.20
FROM node:${NODE_VERSION}

LABEL maintainers="Marcelo Parisi <parisim@google.com>" \
      description="Gerador de Scripts de Testes Playwright" \
      version="1.0.0" 

WORKDIR /app

COPY config config/
COPY lib lib/
COPY package.json .
COPY index.js .

RUN npm install

ENTRYPOINT ["npm", "start"]