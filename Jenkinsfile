pipeline{
  def label = "centos"
  podTemplate(label:label,clode:"kubernetes")    
     node(label) {
	stage("checkout git") {
		git 'https://github.com/sixiaojie/shell.git'
		sh "ls -al"
        }
     }
}

