# pde-gpdb5-ansible
ansible for bds
Prepare AWS
#create aws keypair and download the pem



#install vagrant
~>mkdir -p vagrant/ansible
~>cd vagrant/ansible
ansible>vagrant box list
ansible>vagrant box add bento/centos-7.3
ansible>vagrant init bento/centos-7.3
ansible>vi Vagrantfile
#modify data dir mapping
ansible>vagrant up
ansible>vagrant ssh
#ssh-agent bash
#ssh-add <pem>

#install ansible
vagrant>sudo yum -y install epel-release
vagrant>sudo yum -y install python-pip
vagrant>sudo pip install pip --upgrade
vagrant>sudo pip install ansible --upgradge
vagrant>sudo pip install boto
vagrant>cd /etc/ansible
vagrant> vi ~/.bash_profile
export AWS_ACCESS_KEY_ID='x'
export AWS_SECRET_ACCESS_KEY='x'
export ANSIBLE_HOSTS=/etc/ansible/ec2.py
export EC2_INI_PATH=/etc/ansible/ec2.ini
#test ansible
vagrant>sudo chmod a+x /etc/ansible/ec2.py
vagrant>ansible ec2 -m ping -u ec2-user

vagrant> ansible-playbook -vvvvv -s svn.yml



