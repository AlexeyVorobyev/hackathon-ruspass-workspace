FROM nginx:latest

COPY nginx.template.conf /nginx.template.conf

ENV GEOAPIFY_NEST_ADAPTER_ADDRESS 10.5.0.3

CMD ["/bin/sh" , "-c" , "envsubst '${GEOAPIFY_NEST_ADAPTER_ADDRESS}' < /nginx.template.conf > /etc/nginx/nginx.conf && exec nginx -g 'daemon off;'"]
