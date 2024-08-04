FROM mysql:8.0.39
# Tags
LABEL PROJECT="VProfile"
LABEL AUTHOR="AnNgo"

# Create password
ENV MYSQL_ROOT_PASSWORD="admin123"
ENV MYSQL_ROOT_DATABASSE="accounts"

# Backup db
ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
