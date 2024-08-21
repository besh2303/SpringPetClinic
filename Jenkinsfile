node{
    stage('Checkout'){
        git branch: 'main', url: 'https://github.com/AnjuMeleth/SpringPetClinic.git'
    }
    stage('Build'){
        withMaven(maven: 'M3'){
            sh 'mvn compile'
        }
    }
    stage('Test'){
        steps{
            sh 'mvn '
        }
    }
  stage('Package'){
    steps{
      sh 'mvn package'
    }
  }
  stage('Deploy'){
    steps{
      sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
    }
  }
}
