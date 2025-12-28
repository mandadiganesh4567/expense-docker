

FROM nginx

# 1. Clean out all defaults
RUN rm -rf /usr/share/nginx/html/*
RUN rm -rf /etc/nginx/conf.d/default.conf
RUN rm -rf /etc/nginx/nginx.conf

# 2. Copy the MAIN nginx config (the one starting with 'user nginx;')
COPY nginx.conf /etc/nginx/nginx.conf

# 3. Copy your APP specific config to conf.d
# This is where Nginx looks for server blocks
COPY expense.conf /etc/nginx/conf.d/expense.conf

# 4. Copy your code
COPY code/ /usr/share/nginx/html/

# 5. Ensure permissions are correct
RUN chmod -R 755 /usr/share/nginx/html