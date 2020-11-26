pipeline {
        agent any
        stages {
                stage("clone code"){
                        steps{
                            git 'https://github.com/bijleengr/maven-web-application.git'

                        }
                }
                stage("build code") {
                        steps{
                                sh "mvn clean install"
                        }
                }
                stage("deploy to tomcat"){
                    steps{
                        sshagent(['user']) {
   sh "scp -o StrictHostKeyChecking=no target/*.war  ec2-user@3.137.202.83:/var/lib/tomcat/webapps"
  }
        }
}
}
