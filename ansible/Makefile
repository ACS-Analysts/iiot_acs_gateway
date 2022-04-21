install:
	ansible-playbook -i hosts.yml setup.yml
lint:
	docker run --rm -v ${PWD}:/data cytopia/ansible-lint setup.yml
setup-debian-repo:
	echo "deb http://ppa.launchpad.net/ansible/ansible/ubuntu trusty main" | sudo tee -a /etc/apt/sources.list
setup-ansible:
	sudo apt install dirmngr -y ;\
	sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 93C4A3FD7BB9C367 ;\
	sudo apt update -y ;\
	sudo apt install -y unzip python3 python3-pip ansible ;\
	ansible-galaxy collection install ansible.posix


