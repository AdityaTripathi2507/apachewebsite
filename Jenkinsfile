pipeline{
agent any
stages{
stage(){
steps{
git 'https://github.com/AdityaTripathi2507/apachewebsite.git'
}
}
stage(){
steps{
script{
sh '''
sudo rm -rf /var/www/html*
sudo cp -r* /var/www/html/
sudo chown -R www-data:www-data /var/www/html/
sudo chmod -R 755 /var/www/html/
'''
}
}
}
stage(){
steps{
script{
sh 'sudo systemctl restart apache2'
}
}
}
}
post{
success{
echo 'Deployment Successfull! Website is live on Apache.'
}
failure{
echo 'Deployment failed'
}
}
}
