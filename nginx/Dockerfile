FROM nginx:latest

COPY nginx.template.conf /nginx.template.conf

ENV GEOAPIFY_NEST_ADAPTER_ADDRESS 10.6.0.3
ENV SEARCH_IMAGE_NEST_ADAPTER_ADDRESS 10.6.0.4
ENV RUSPASS_NEXTJS_FRONTEND_ADDRESS 10.6.0.5

CMD ["/bin/sh" , "-c" , "envsubst '${GEOAPIFY_NEST_ADAPTER_ADDRESS},${SEARCH_IMAGE_NEST_ADAPTER_ADDRESS},${RUSPASS_NEXTJS_FRONTEND_ADDRESS}' < /nginx.template.conf > /etc/nginx/nginx.conf && exec nginx -g 'daemon off;'"]
