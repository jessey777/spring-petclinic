pipeline {
    agent {
        label 'jio'
    }
   stages {
       stage('git-hub') {
           steps{
             git 'https://github.com/jessey777/spring-petclinic.git'
           }
       }
       stage('build code') {
           steps{
               sh 'mvn clean package'
           }
       }
       
       stage('archive artifacts') {
           steps{
               archiveArtifacts 'target/*.jar'
           }
       }
       stage('junit test reports') {
           steps{
               junit 'target/surefire-reports/*.xml'
           }
       }
       
     }
  }
    
    
    
    
    
    
    
    
    
    
