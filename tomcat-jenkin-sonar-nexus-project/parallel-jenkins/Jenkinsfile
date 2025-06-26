pipeline {
agent any 
tools {
maven 'maven'
}
stages {
stage (' git checkout') {
steps {
checkout scm 
}
}
stage ('build the test in parallel') {
parallel {
stage ('build the code') {
steps {
sh 'mvn clean package'
}
}

stage ('static analysis') {
steps {
echo ' static code analysis..... '
sh 'echo " code analyssis is done" '
}
}
}
}
}
}

