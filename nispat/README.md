# nispat
Simple repository that describes my nispat installation and usage on HPCs

# Environment build (cluster)

	# Make environment
	module load python/3.7.3-system
	cd /home/lindenmp/virtual_env
	virtualenv nispat
	source /home/lindenmp/virtual_env/nispat/bin/activate

	# Essentials
	pip install --upgrade pip
	pip install ipython pandas scipy nibabel sklearn torch glob3

	# Nispat
	cd /home/lindenmp/virtual_env/nispat/
	git clone https://github.com/lindenmp/nispat.git
	cd /home/lindenmp/virtual_env/nispat/nispat
	python setup.py install

	cd /home/lindenmp/virtual_env/nispat/
	pip freeze > requirements_m3.txt
