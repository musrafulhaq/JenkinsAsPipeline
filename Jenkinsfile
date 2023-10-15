// pipeline {
//     agent any 
//     stages {
//         stage("Init") {
//             steps{
//                 echo "Initialize"
//             }
//         }
//         stage ("Build"){
//             steps{
//                 echo "Build the job"
//             }
//         }
//         stage ("Deployement"){
//             steps {
//                 echo "Deploy the application on cloud platform"
//             }
//         }
//     }
// }


pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                sh 'mvn clean package'
            }
            post {
                success {
                    echo "Now Archiving"
                    archiveArtifact artifact: '**/*.war'
                }
            }
        }
    }
}