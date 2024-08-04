FROM nginx
LABEL PROJECT="VProfile"
LABEL AUTHOR="AnNgo"

# Remove default configuration
RUN rm -rf /etc/nginx/conf.d/default.conf
# Copy new config
COPY nginvproapp.conf /etc/nginx/conf.d/default.conf
