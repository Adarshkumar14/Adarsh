# FAQ & TROUBLESHOOTING
##  Litmus Portal
### Can we host Mongodb outside the cluster? What connection string is supported? Is SSL connection supported?
Yes we can host Mongodb outside the cluster,  the mongo string can be updated accordingly `DataBaseServer: "mongodb://mongo-service:27017"`
We use the same connection string for both authentication server and graphql server containers in litmus portal-server deployment, also there are the db user and db            password keys that can tune in the configmap like `DB_USER: "admin"` and `DB_PASSWORD: "1234"`.
We can connect with SSL if certificate is optional.If our requirement is ca.cert auth for the SSL connection, then this is not available on portal. 

### Is there any way to use Litmus within github? Basically when someone submits a k8s deployment for a PR , We want to run chaos Experiment on that to see whether it passes or not.
We can use it with the help of  github-chaos-action.Using github-chaos-action we can automate the chaos execution on an application in the same place where the code is stored. We can write individual tasks along with chaos actions and combine them to create a custom GitHub workflow. GitHub Workflows are custom automated processes that we can set up in our repository to build, test, package, or deploy any code project on GitHub. Including the Github chaos actions in our workflow YAML, We can test the performance/resiliency of our application in a much simpler and better way. To know more please visit  our Github chaos action [repository](https://github.com/litmuschaos/github-chaos-actions).




















