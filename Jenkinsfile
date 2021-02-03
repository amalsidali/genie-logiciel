pipeline
{
agent any
      tools {
      maven 'apache-mvn-3.6.3'
      jdk 'jdk11'
      }
      stages {
          stage('build')
          {
              steps {
              sh 'mvn compiler:compile'
              }
              post {
                  success {
                      echo 'Compliation terminé avec success'
                  }

                  failure {
                      echo 'Erreur de compilation'
                  }
              }
          }
      }
}
