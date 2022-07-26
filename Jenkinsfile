pipeline {
  agent any
  
  stages {
   stage('Build Application') {
    steps {
         dir('D:\\git_Checkout_code') {         
         bat 'mvn clean install'
   }
   }
   }
   
   stage('Deploy Application to Mulesoft CloudHub') {
    steps {
         dir('D:\\git_Checkout_code') {
         bat 'mvn package deploy -DmuleDeploy'
   }
   }
   }
   
   stage('Perform Regression Testing') {
    steps {
         dir('C:\\Users\\ADMIN\\AppData\\Roaming\\npm') {
         bat 'newman run D:\\newmann\\WORLD_TIMEZONE.postman_collection.json --disable-unicode'
   }
   } 
  }
 }
 }