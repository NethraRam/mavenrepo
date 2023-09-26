pipeline{
  
agent {
  label 'slave'
}

triggers {
  pollSCM '* * * * *'
}
stages{
stage('git'){
steps{
checkout scmGit(branches: [[name: '*/feat01']], extensions: [], userRemoteConfigs: [[credentialsId: 'c7cd5a45-3362-43c5-ae14-44d38dee3413', url: 'https://github.com/NethraRam/mavenrepo.git']])
}
}

stage('build'){
steps{
sh 'mvn test'
}
}


}
}
