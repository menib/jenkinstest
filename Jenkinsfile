
node('node') {
    currentBuild.result = "SUCCESS"

    try {
       stage 'Checkout'
            echo 'Checkout'
           # checkout scm

       stage 'Build'
             echo 'Build'

       stage 'Test'
             echo 'Test'

       stage 'Cleanup'
            echo 'Cleanup'
        }


    catch (err) {
        currentBuild.result = "FAILURE"
            mail body: "project build error is here: ${env.BUILD_URL}" ,
            from: 'meni.b@quali.com',
            replyTo: '',
            subject: 'project build failed',
            to: 'meni.b@quali.com'

        throw err
    }

}
