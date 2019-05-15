pipeline{
	environment {
		label = "centos"
	}	
	agent {
		node {
		    label 'centos'
		}
	}
	podTemplate(label:label,clode:"kubernetes") {   
		    stage("checkout git") {
		        git 'https://github.com/sixiaojie/shell.git'
		        sh "ls -al"
	}
     }
}

