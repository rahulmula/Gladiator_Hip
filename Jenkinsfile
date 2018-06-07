node {
  
    stage('checkouts') {

       
        sh 'id'
        stage('Jenkinsfile utility')
        git credentialsId: '8c1bf1d6-da10-49c0-89ed-0165f97d10d4', url: 'https://github.com/rahulmula/Gladiator_Hip.git'
       
      }

    stage('Build') {
    	        sh 'cd ${WORKSPACE}'
                sh 'mkdir build'
                sh 'cd build'
                sh 'cmake -DCMAKE_INSTALL_PREFIX=$PWD ..'
                sh 'make -j16'
                sh 'make install'

                }

    stage('Unit Test') {

                sh 'make check'
                sh 'make package'
                
    	        }

    }

