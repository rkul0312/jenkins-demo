pipeline{
    agent any 
    
        
    parameters {
 choice (choices: ['VAR1', 'VAR2', 'VAR3'], description: 'Select any of the parameter', name: 'Options')
    //   choice (choices: ['1', '2', '3'], description: 'Select any one', name: 'Select')
  booleanParam(defaultValue: true, name: 'Version')

}
    environment{
        VAR1 = "Mani"
         VAR2 = "Rahul"
          VAR3 = "Virat"
    
        
    }
    stages{
        stage("first"){
            steps{
                 echo "Hello this is first stage"
                 echo "${VAR1}"
            }
    
         }
        stage("second"){
            when{
                expression{
                     params.Options == "VAR2"
                }
            }
            steps{
                 echo "Hello this is Second stage"
                echo "${VAR2}"
            }
        }
    }
    
}
