# FAQ & TROUBLESHOOTING
##  Litmus Portal
- Can we host Mongodb outside the cluster? What connection string is supported? Is SSL connection supported?
   Yes we can host Mongodb outside the cluster,  the mongo string can be updated accordingly DataBaseServer: "mongodb://mongo-service:27017"
   We use the same connection string for both authentication server and graphql server containers in litmus portal-server deployment, also there are the db user and db password    keys that can tune in the configmap like DB_USER: "admin" and DB_PASSWORD: "1234".
   We can connect with SSL if certificate is optional.If our requirement is ca.cert auth for the SSL connection, then this is not available on portal. 




















