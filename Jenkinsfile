properties([
    parameters([
        choice(choices: ['IL', 'CA', 'MI', 'NY'].join("\n"), description: 'select state', name: 'State'), 
        string(defaultValue: 'Chinny', description: 'enter name', name: 'name', trim: false)]
        )])
        
if(State=='CA')
{
j_node='master'
    }
    else
    {
        j_node='w4'
    }

node(j_node) {
        stage('Build and generate .war file') {
            echo 'generated .war file'
            powershell 'date'
            sleep 10
            echo "Choice: ${params.State}"
            echo "Choice: ${params.name}"
        }
        stage('Deploy code to QA'){
            echo 'deploying .war file to QA'
            echo 'QA will test and follow the process'
        }
        stage('Deploy to production'){
            echo '.war file successfully deployed to prod'
        }
}
