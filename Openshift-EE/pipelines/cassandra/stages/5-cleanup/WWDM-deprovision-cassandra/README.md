#### Deprovision Cassandra

This job will delete the cassandra statefulset installed in OpenShift cluster.

#### Prerequisites

- OpenShift cluster should be ready.
- OpenEBS should be deployed.
- Cassandra should be deployed

#### Procedure

- The job should trigger the litmusbook which is capable of deleting Cassandra specific components in the cluster.

- This should delete all the components in the respective namespace.

- This can be verified using kubectl command `kubectl get ns`


#### Test Result


| Job ID |   Test Description         | Execution Time |Test Result   |
 |---------|---------------------------| --------------|--------|
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/89166">89166</a>           |  Check if the cassandra ring is deleted successfully           | Tue Sep 24 16:11:59 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:593b3cdff67b25b3cbdcfd35a1a86924e6d73efa,type:phrase),type:phrase,value:593b3cdff67b25b3cbdcfd35a1a86924e6d73efa),query:(match:(commit_id:(query:593b3cdff67b25b3cbdcfd35a1a86924e6d73efa,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:3333,type:phrase),type:phrase,value:3333),query:(match:(pipeline_id:(query:3333,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/85482">85482</a>           |  Check if the cassandra ring is deleted successfully           | Thu Sep 12 18:14:23 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:d70f47dfe44655b09ce4b83b8a66e43c8c4c130f,type:phrase),type:phrase,value:d70f47dfe44655b09ce4b83b8a66e43c8c4c130f),query:(match:(commit_id:(query:d70f47dfe44655b09ce4b83b8a66e43c8c4c130f,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:3226,type:phrase),type:phrase,value:3226),query:(match:(pipeline_id:(query:3226,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/85255">85255</a>           |  Check if the cassandra ring is deleted successfully           | Thu Sep 12 14:30:54 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:c23611c68a3fca19762820946c944263a28d15c2,type:phrase),type:phrase,value:c23611c68a3fca19762820946c944263a28d15c2),query:(match:(commit_id:(query:c23611c68a3fca19762820946c944263a28d15c2,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:3220,type:phrase),type:phrase,value:3220),query:(match:(pipeline_id:(query:3220,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/36774">36774</a>           |  Check if the cassandra ring is deleted successfully           | Sat Jun  1 03:35:56 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:37e38528aadce8ca5770803a70648152b0f43656,type:phrase),type:phrase,value:37e38528aadce8ca5770803a70648152b0f43656),query:(match:(commit_id:(query:37e38528aadce8ca5770803a70648152b0f43656,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:1571,type:phrase),type:phrase,value:1571),query:(match:(pipeline_id:(query:1571,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a> |
 |    <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/36145">36145</a>   |  Check if the cassandra ring is deleted successfully           |  Fri May 31 07:32:03 IST 2019     |<a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:cb476f8e715fb374877c31b699863b56dd3c5ded,type:phrase),type:phrase,value:cb476f8e715fb374877c31b699863b56dd3c5ded),query:(match:(commit_id:(query:cb476f8e715fb374877c31b699863b56dd3c5ded,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:1551,type:phrase),type:phrase,value:1551),query:(match:(pipeline_id:(query:1551,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a>  |
