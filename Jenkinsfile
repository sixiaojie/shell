pipeline{
  def label = "cebtos-test"
  podTemplate(label:label,clode:"kubernetes")    
     node(label) {
	stage("checkout git") {
	git 'https://github.com/sixiaojie/shell.git'
        }
     }
}

