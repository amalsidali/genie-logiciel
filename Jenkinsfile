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
              def gv = load 'script.groovy'
              gv.call_build()
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
