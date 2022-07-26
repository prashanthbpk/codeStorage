pipeline
 {
  agent any
  stages{
   stage('Build Application'){
   steps{
   bat 'mvn clean install'
   }
   }
   
   stage('Deploy Application to Mulesoft CloudHub'){
   steps{
   bat 'mvn package deploy -DmuleDeploy'
   }
   }
   
   stage('Perform Regression Testing'){
   steps{
   bat 'newman run D:\\newmann\\WORLD_TIMEZONE.postman_collection.json --disable-unicode'
   }
   } 
  }
 }