node{
   stage('Cloning Git'){
       git 'https://github.com/anwarfaisal320/manheim.git''
   }
   stage('Mvn Package'){
     
      sh "mvn clean package"
   }
   stage('Build Docker Image'){
     sh 'docker build -t afaisal320/docker-spring-boot .'
   }
   stage('Push Docker Image'){
     sh 'docker push afaisal320/docker-spring-boot'
   }
   stage('Run Container on Dev Server'){
       sh "docker run -p 8085:8085 -d afaisal320/docker-spring-boot}"
   }
   
}
