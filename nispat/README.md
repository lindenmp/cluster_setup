# nispat
Simple repository that describes my nispat installation and usage on HPCs

# Environment build (m3)

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

# Environment build (cubic, home)

	# Make environment
    conda create -n nispat python=3.7
    conda activate nispat

	# Essentials
	pip install --upgrade pip
	pip install ipython pandas scipy nibabel sklearn torch glob3

	# Nispat
	cd /cbica/home/parkesl/miniconda3/envs/nispat/
	git clone https://github.com/lindenmp/nispat.git
	cd /cbica/home/parkesl/miniconda3/envs/nispat/nispat
	python setup.py install

	cd /cbica/home/parkesl/miniconda3/envs/nispat/
	pip freeze > requirements_cubica.txt
