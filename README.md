```
docker push gcr.io/<IMAGE_NAME>
<PATH>/Downloads/google-cloud-sdk/bin/docker-credential-gcloud: line 193: <PATH>/Downloads/google-cloud-sdk/bin/gcloud: No such file or directory
The push refers to repository [gcr.io/<IMAGE_NAME>]
4ab3f41421fd: Preparing
10176f12ba3a: Preparing
39cfbc5a6990: Preparing
9441f099178b: Preparing
f66ed577df6e: Preparing
unauthorized: You don't have the needed permissions to perform this operation, and you may have invalid credentials. To authenticate your request, follow the steps in: https://cloud.google.com/container-registry/docs/advanced-authentication
``` 

gcloud command works. But the docker push command was looking for the gcloud file in the ```<PATH>/Downloads/google-cloud-sdk/bin/``` directory.

So I removed the existing google-cloud-sdk folder from Downloads directory and downloaded the latest google-cloud-sdk.

Then I ran 
```gcloud auth login```





