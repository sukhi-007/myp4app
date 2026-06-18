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
