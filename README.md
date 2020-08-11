# EC2-Tutorial

## Create Environment
1. Create EC2 instance.
2. Get pem file.
```console
chmod 400 twitter_streamlit_key.pem
ssh -i twitter_streamlit_key.pem ec2-user@ec2-54-65-87-232.ap-northeast-1.compute.amazonaws.com
```
3. Create config file in .ssh folder. (IPv4 Public IP)
```console
Host twitterstreamlit
	HostName 54.65.87.232
	User ubuntu
	IdentityFile C:\Users\jimmy\Desktop\awskey\twitter_streamlit_key.pem
```
4. SSH into our instance.
```console
ssh twitterstreamlit
```
5. Run the following command to install Git.
```console
sudo apt install git
```

## Clone Repository
```console
git clone https://github.com/penguinwang96825/Made-with-ML-Incubator-Project.git
```
## Keep Running Python Script
```console
tmux new -s mywindow
```
Once the new window starts, run your script. Once the script is running, you can close your ssh client or shut down your local computer. When you want to see the results, log in to your ec2 through ssh again, and type this:
```console
tmux a -t mywindow
```
