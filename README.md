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
