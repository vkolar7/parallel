pipeline{
  agent any;
  stages{
    stage ('Build'){
      parallel {
       stage ('BUILD_1'){
         steps {
           echo "Build_1 is running"
           sh 'sleep 4'
         }
       }
        stage ('Build_2'){
          stages {
            stage ('Build_2.1'){
              steps {
                echo "Build_2.1 is running"
                sh 'sleep 2'
              }
            }
            stage ('Build_2.2'){
              steps {
                echo "Build_2.2 is running"
                sh 'sleep 2'
              }
            }
          }
        }
      }
    }
    stage ('Test'){
      parallel {
        stage ('Test_1'){
          steps {
            echo "Testing Build_1"
            sh 'sleep 4'
          }
        }
        stage ('Test_2'){
          stages {
            stage ('Test_2.1'){
              steps {
                echo "Testing Build_2.1"
                sh 'sleep 2'
              }
            }
            stage ('Test_2.2'){
              steps {
                echo "Testing Build_2.2"
                sh 'sleep 2'
              }
            }
          }
        }
      }
    }
  }     
}
