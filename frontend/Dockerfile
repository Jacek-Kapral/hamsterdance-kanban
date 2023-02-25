# syntax=docker/dockerfile:1.4
FROM --platform=$BUILDPLATFORM node:18.3.0-alpine AS development

RUN mkdir /project
WORKDIR /project

COPY . .

RUN npm -g add @vue/cli
RUN npm install
ENV HOST=0.0.0.0
CMD ["npm", "run", "serve"]

FROM development as dev-envs
RUN <<EOF
apk update
apk add git
EOF

RUN <<EOF
addgroup -S docker
adduser -S --shell /bin/bash --ingroup docker vscode
EOF

COPY --from=gloursdocker/docker / /
ENTRYPOINT ["npm", "run", "serve"]
