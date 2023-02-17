pipeline {
agent any
stages {
 stage ('Clone reposiory'){
 steps{
  git branch : 'main',
  url : 'https://github.com/garagveena/PES1UG20CS492_jenkins.git'
}
 }



stage( 'Build application') {
steps {
sh 'g++ pes1ug20cs492.cpp'
}
}
stage( 'Test application') {
steps{
sh './a.out'
sh 'failure ' 
}
}

}
post {
    failure {
         echo "pipeline failed "
    }
}
}
