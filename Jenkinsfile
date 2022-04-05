pipeline{
    agent{label 'master'}
    tools{maven 'M3'}
    stages{
        stage('checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/ashish02081999/SpringPetClinic.git'
            }
        
        }
        stage('build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh "mvn package"
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar/var/lib/jenkins/workspace/PetCLinicDeclarativePipline/target/*.jar'
            }
        }
    
    }
}
