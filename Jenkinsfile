stages{
      stage('deploy to S3'){
          steps{
              sh 'aws s3 cp public/index.html s3://<dichajenkinsbucket>'
              sh 'aws s3api put-object-acl --bucket <dichajenkinsbucket> --key index.html --acl public-read'
              sh 'aws s3 cp public/error.html s3://<dichajenkinsbucket>'
              sh 'aws s3api put-object-acl --bucket <dichajenkinsbucket> --key error.html --acl public-read'
          }
      }
  }