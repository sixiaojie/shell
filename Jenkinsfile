pipeline{
      agent{
        node{
          label 'slave-pipeline'
        }
      }
      stages{
        // 定义第一个stage， 完成克隆源码的任务
        stage('Git'){
          steps{
		sh "echo git"
          }
        }
        
        stage('composer php') {
            steps {
                container('composer'){
                    sh 'echo composer'
                }
              }
             }
        stage("ssh permission change") {
            steps {
                container('composer'){
                }
            }
        }
        stage('git clone'){
            steps {
                container('composer'){
                    
                }
            }
        }
        // 添加第四个stage, 运行容器镜像构建和推送命令， 用到了environment中定义的groovy环境变量
        stage('Image Build And Publish'){
          steps{
              container("kaniko") {
		 sh "echo kaniko"
              }
          }
        }

        stage('Deploy to Kubernetes') {
                    steps {
                        container('kubectl') {
                            sh "echo kubelet"
                            
                        }
                    }
        	}
        }
    }

