pipeline {
  agent any
  
  stages {
   
   stage('Checkout Scm') {
      steps {
        git(url: 'https://github.com/pasi2695/myCodeMulesoft.git', credentialsId: '46629a15-baa9-441f-8962-bb31f99517ea')
      }
    }
    
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
 triggers {
    pollSCM('* * * * *')
  }
 }