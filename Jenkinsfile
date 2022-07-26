pipeline {
  agent any
  
  stages {
   stage('Build Application') {
    steps {
         https://github.com/pasi2695/myCodeMulesoft.git
         bat 'mvn clean install'
   }
   }
   
   stage('Deploy Application to Mulesoft CloudHub') {
    steps {
         https://github.com/pasi2695/myCodeMulesoft.git
         bat 'mvn package deploy -DmuleDeploy'
   }
   }
   
   stage('Perform Regression Testing') {
    steps {
         https://github.com/pasi2695/myCodeMulesoft.git
         bat 'newman run D:\\newmann\\WORLD_TIMEZONE.postman_collection.json --disable-unicode'
   }
   } 
  }
 }