node('SPRING-PET')
{
      stage('vcs')
      {
            git 'https://github.com/laxmandevopsMarch23/spring-petclinic-script.git'
      }
      stage('package')
      {
            sh 'export PATH="/usr/lib/jvm/java-1.8.0-openjdk-amd64/bim:$PATH" && mvn package'
      }
      stage('build')
      {
             archiveArtifacts artifacts: '**/*.txt', followSymlinks: false
             junit '**/surefire-reports/TEST-*.xml'
      }
}