node{
   stage('SCM Checkout'){
      git https://github.com/l00143533/HelloRepo
   }
   stage('Compile-Package'){
    def mvnHome = tool name: 'maven-3.6.3', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
   }
}
