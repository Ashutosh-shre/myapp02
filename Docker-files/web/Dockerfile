FROM nginx:latest
LABEL Project="vprofile" Version="2.0" OWner="Ashu"
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]