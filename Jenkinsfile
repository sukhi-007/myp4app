pipeline {
agent any
tools{
 maven 'Maven'
 jdk 'JDK'
}
stages{
 stage('Checkout'){
 steps{
  git branch: 'master', url: 'https://github.com/sukhi-007/myp4app.git'
}
}
stage('Build'){
 steps{
 sh 'mvn clean package'
}
}

stage('Test'){
 steps{
  sh 'mvn test'
}
}

stage('Run application'){
  steps{
   sh 'java -jar target/myp4app-1.0-SNAPSHOT.jar'
}

}
}
post{
success{
 echo "build successful"
}
failure {
echo "build failure"
}
}
}
