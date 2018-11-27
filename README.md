# work-on-RDS
copy data from one RDS server(ex:mariadb) to another RDS server


> sudo mysqldump -h mydbserver.amazonaws.com -u <username> \
>     --databases <databasename> \
>     --single-transaction \
>     --compress \
>     --order-by-primary  \
>     -ppassword | mysql -h my2dbserver.rds.amazonaws.com -u <username for second server> -ppassword
