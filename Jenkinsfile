node('SPRING-PET')
{
    stage('vcs')
    {
        git url: 'https://github.com/laxmandevopsMarch23/spring-petclinic-script.git',
            branch: 'scripted'
    }
    stage('package')
    {
        sh 'mvn package'
    }
    stage('build')
    {
        archiveArtifacts artifacts: '**/*.txt',
                         fingerprint: true,
                         onlyIfSuccessful: true,
                         allowEmptyArchive: true
        junit '**/surefire-reports/TEST-*.xml'
    }
}