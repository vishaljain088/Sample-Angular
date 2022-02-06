pipeline {
    agent any
    parameters {
        choice(
            choices: ['frontend','backend'],
            description: '',
            name: 'REQUESTED_ACTION')
    }

    stages {
        stage ('Build1') {
            when {
                // Only say hello if a "greeting" is requested
                expression { params.repochoices == 'frontend' }
            }
            steps {
               
               echo "Hello"
                
            }
            stage ('Build2') {
            when {
                // Only say hello if a "greeting" is requested
                expression { params.repochoices == 'backend' }
            }
            steps {
               
               echo "backend"
                
            }
            }
        }
    }
}
/*node{
    stage('Indentify branch'){
        script {
          commit = checkout scm
          println commit.GIT_BRANCH
          a = commit.GIT_BRANCH
          bname = sh ( script: "echo $a | grep -oP '(?<=origin/).*' ",returnStdout: true ).trim()
          cname = sh ( script: "echo $bname | tr -dc '[:alnum:]\n\r' | tr '[:upper:]' '[:lower:]'",returnStdout: true ).trim()
        }
    }*/
    /*stage('clone'){
    git credentialsId: 'vishaljain088', url: 'https://github.com/vishaljain088/Sample-Angular}*/
    /*stage('update buildnumber and date in packagejson'){
      sh """
      sed -i "s/JENKINS_BUILD_NO/"${BUILD_NUMBER}"/g" package.json
      """
      }*/
    /*stage ('Build Docker Image') {
      sh "docker build  --tag ${env.JOB_NAME}_${cname}:$BUILD_NUMBER ." }*/

      /*stage('push image to docker hub'){
        withCredentials([string(credentialsId: 'Docker_HUB_pwd', variable: 'docker_hub')]) {
         sh "docker login -u vishaljain088 -p ${docker_hub}"
}*/
      
     /*sh "docker push ${env.JOB_NAME}_${cname}:$BUILD_NUMBER"
      }*/

    /*stage('push image to Harbor'){
   withCredentials([string(credentialsId: 'vishaljain088', variable: 'private_repo')]) {
  sh "docker login -u admin -p ${private_repo} https://hub.docker.com/"}
    }

   sh """
     docker image tag ${env.JOB_NAME}_${cname} https://hub.docker.com/repository/docker/vishaljain088/trivy-sample/angular_image_${env.JOB_NAME}_${cname}:${BUILD_NUMBER}
     docker push https://hub.docker.com/repository/docker/vishaljain088/trivy-sample/angular_image_${env.JOB_NAME}_${cname}:${BUILD_NUMBER}
     """*/
     /*stage ('deployment to other server as a containter'){
     sshagent(['Docker']) {
    sh "ssh -o StrictHostKeyChecking=no ubuntu@18.237.166.89 sudo docker rm -f angularapp || true"
    sh "ssh -o StrictHostKeyChecking=no ubuntu@18.237.166.89 sudo docker run -d -p 8080:8080 --name angularapp ${env.JOB_NAME}_${cname}:$BUILD_NUMBER"
}
     }
}*/
