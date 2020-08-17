# Hands on with OpenShift on IBM Cloud

This is the repository for the OpenShift 101 workshop presented by IBM

To deploy this workshop:

```bash
kubectl create -k "github.com/jjasghar/openshift101?ref=master"
```

## Other IBM Workshops

Many people and groups worked on the following workshops and classes, parts of which have ended up here.

* https://github.com/beemarie/kube-code-camp
* https://gitlab.com/ibm/kube101
* https://github.com/ibm/kube101
* https://github.com/ibm/istio101

## Developing/Local Running

```bash
docker run -ti --rm -p 10080:10080 -e ENABLE_EDITOR=true -v \
  $(pwd):/home/eduk8s quay.io/eduk8s/workshop-dashboard:master
```

If you want to build the image:
```bash
docker build -t quay.io/ibm/openshift101-workshop:master .
docker push quay.io/ibm/openshift101-workshop:master
```

## License & Authors

If you would like to see the detailed LICENSE click [here](LICENSE).

- Author: Sai Vennam <svennam@us.ibm.com>, IBM Cloud Offering Manager
- Maintainers: Developer Advocates from IBM Cloud

```text
Copyright:: 2019- IBM, Inc

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```


Sample workshop content using Markdown formatting for pages.

For more detailed information on how to create and deploy workshops, consult
the documentation for eduk8s at:

* https://docs.eduk8s.io

If you already have the eduk8s operator installed and configured, to deploy
and view this sample workshop, run:

```
kubectl apply -f https://raw.githubusercontent.com/eduk8s/lab-markdown-sample/master/resources/workshop.yaml
kubectl apply -f https://raw.githubusercontent.com/eduk8s/lab-markdown-sample/master/resources/training-portal.yaml
```

This will deploy a training portal hosting just this workshop. To get the
URL for accessing the training portal run:

```
kubectl get trainingportal/lab-markdown-sample
```

The training portal is configured to allow anonymous access. For your own
workshop content you should consider removing anonymous access.
