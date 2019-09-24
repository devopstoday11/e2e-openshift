### Cassandra pod failure.

#### Description

This job will induce failure in one of the  Cassandra pods in the statefulset. 

#### Prerequisites

- OpenShift cluster should be ready.
- Cassandra pods should be running. 

#### Procedure

- The job should trigger the litmusbook which is capable of inducing cassandra pod failure.
- The inputs such as application label, application namespace should be provided as environmental variable to the ansible-runner pod which executes the test.
- Check the impact of application when one of the application replica is lost.
- Check the status of statefulset application after recovering from the failure. All the application replicas should be running.
- Check if the cassandra statefulset is created successfully using kubectl command `kubectl get sts -n <application namespace>`

#### Test Result


| Job ID |   Test Description         | Execution Time |Test Result   |
 |---------|---------------------------| --------------|--------|
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/89152">89152</a>           |  Induce Cassandra pod failure and check if it can be recovered successfully.           | Tue Sep 24 15:28:11 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:593b3cdff67b25b3cbdcfd35a1a86924e6d73efa,type:phrase),type:phrase,value:593b3cdff67b25b3cbdcfd35a1a86924e6d73efa),query:(match:(commit_id:(query:593b3cdff67b25b3cbdcfd35a1a86924e6d73efa,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:3333,type:phrase),type:phrase,value:3333),query:(match:(pipeline_id:(query:3333,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/88755">88755</a>           |  Induce Cassandra pod failure and check if it can be recovered successfully.           | Mon Sep 23 13:35:32 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:f7b08f10bd3fbe5b1afd6c46b9016bdd32ffcf2b,type:phrase),type:phrase,value:f7b08f10bd3fbe5b1afd6c46b9016bdd32ffcf2b),query:(match:(commit_id:(query:f7b08f10bd3fbe5b1afd6c46b9016bdd32ffcf2b,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:3316,type:phrase),type:phrase,value:3316),query:(match:(pipeline_id:(query:3316,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a> |
|     <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/85237">85237</a>           |  Induce Cassandra pod failure and check if it can be recovered successfully.           | Thu Sep 12 13:52:58 IST 2019  | <a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:c23611c68a3fca19762820946c944263a28d15c2,type:phrase),type:phrase,value:c23611c68a3fca19762820946c944263a28d15c2),query:(match:(commit_id:(query:c23611c68a3fca19762820946c944263a28d15c2,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:3220,type:phrase),type:phrase,value:3220),query:(match:(pipeline_id:(query:3220,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Fail</a> |
 |    <a href="https://gitlab.openebs.ci/openebs/e2e-openshift/-/jobs/36769">36769</a>   |  Induce Cassandra pod failure and check if it can be recovered successfully.           |  Fri May 31 15:35:36 IST 2019     |<a href="https://e2e-logs.openebs100.io/app/kibana#/discover?_g=(refreshInterval:(pause:!t,value:0),time:(from:now-7d,mode:quick,to:now))&_a=(columns:!(_source),filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:commit_id,negate:!f,params:(query:37e38528aadce8ca5770803a70648152b0f43656,type:phrase),type:phrase,value:37e38528aadce8ca5770803a70648152b0f43656),query:(match:(commit_id:(query:37e38528aadce8ca5770803a70648152b0f43656,type:phrase)))),('$state':(store:appState),meta:(alias:!n,disabled:!f,index:cluster-logs,key:pipeline_id,negate:!f,params:(query:1571,type:phrase),type:phrase,value:1571),query:(match:(pipeline_id:(query:1571,type:phrase))))),index:cluster-logs,interval:auto,query:(language:lucene,query:''),sort:!('@timestamp',desc))">Pass</a>  |
