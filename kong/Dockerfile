FROM kong:alpine

RUN apk update && \
    apk add git && \
    luarocks install kong-spec-expose && \
    luarocks install kong-error-log && \
    luarocks install kong-path-based-routing && \
    luarocks install kong-upstream-jwt && \
    luarocks install kong-splunk-log && \
    luarocks install kong-plugin-jwt-keycloak && \
    luarocks install kong-oidc && \
    luarocks install kong-oidc-auth

ENV KONG_PLUGINS=bundled,kong-splunk-log,kong-spec-expose,jwt-keycloak,kong-error-log,kong-path-based-routing,oidc,kong-oidc-auth
