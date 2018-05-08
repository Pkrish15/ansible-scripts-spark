# ansible-scripts-spark
Ansible Playbook Scripts for Apache Spark Configuration

0) login using oc utility - oc login -u prakrish-redhat.com -p XXXXXXX https://master.dev39.openshift.opentlc.com/
1) ansible-galaxy init ./roles/spark/tasks
2) tree /roles/spark/tasks/
3) Navigate to the Spark-WEB-UI Configuration URL. 
   Please apply your project namespace configuration <br>
    http://spark-master-webui-{your-project-namespace}.apps.dev39.openshift.opentlc.com/
4) To run this playbook, please execute the below command.<br>
    
   $ [root@localhost ansible-scripts-spark] ansible-playbook -v ocp.yml

5) To use oshinko Cluster Configuration,Please use the below url. pk is your openshift project namespace <br>
 
   http://oshinko-web-pk.apps.dev39.openshift.opentlc.com/webui/#/clusters

6) Click Deploy Button and add your either artifact id or project id. <br>
   http://pmml-ui-route-pk.apps.dev39.openshift.opentlc.com/
   
# Spark-Submit Jobs
7)  ./bin/spark-submit \
  --class com.redhat.gpte.CsvToDataset \
  --master spark://pmml:7077 \
  --executor-memory 20G \
  --total-executor-cores 100 \
  /path/to/pmml-export.jar \
  
8) More Format of Deployment is described in this below url.<br>
   https://spark.apache.org/docs/2.2.0/submitting-applications.html
 

# Pre-Requisites for Spark-submit
    a) You should install local spark (preferrably latest version 2.3) in your desktop from this url (https://spark.apache.org/downloads.html)
    b) You should have github or any version control installed in your local desktop
    c) Github url for above examples https://github.com/Pkrish15/pmml-export.git
    
   
