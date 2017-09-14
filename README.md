# build_python_modules

some ref I found: 

https://github.com/jordansissel/fpm/wiki/ConvertingPython
https://media.readthedocs.org/pdf/fpm/latest/fpm.pdf

if you want to go pp route then 

https://pypi.python.org/pypi/bandersnatch#installation

$ virtualenv --python=python3.5 bandersnatch
$ cd bandersnatch
$ bin/pip install -r https://bitbucket.org/pypa/bandersnatch/raw/stable/requirements.txt

Configuration

1. Run bandersnatch mirror - it will create an empty configuration file for you in /etc/bandersnatch.conf.
2. Review /etc/bandersnatch.conf and adapt to your needs.
3. Run bandersnatch mirror again. It will populate your mirror with the current status of all PyPI packages - roughly 500GiB (2017-02-12). Expect this to grow substantially over time.
4. Run bandersnatch mirror regularly to update your mirror with any intermediate changes.



Ubuntu: 

Python2 pip:
apt-get install python-pip


Install pip3 for python3: 
apt-get -y install python3-pip

Upgrade pip for python3: 
pip3 install --upgrade pip

Upgrade pip for python2:
pip install --upgrade pip

=======

CentOS 7: 

Python 2 pip: 
yum -y install python-pip gcc python-devel python34-devel 

Upgrade pip for python2: 
&& pip install --upgrade pip 

Python 3 pip:
yum -y install python-pip gcc python-devel python34-devel 

pip install --upgrade pip && python3 -m pip install psutil

Python34 installation: 
yum install python34 python34-devel 

CentOS 6: 

pip3 installation: 
curl https://bootstrap.pypa.io/get-pip.py | python3.4

Python34 installation: 
yum install python34 python34-devel 

========

root@prn-testubuntu1601:~# cat .pip/pip.conf
[global]
index-url = http://package.thefacebook.com/python/pypi/web/simple

[install]
trusted-host=package.thefacebook.com

[list]
format=(legacy|columns)

=========================================================================================


Specific version using pip: pip install -Iv MySQL_python==1.2.2

-I - -I, --ignore-installed ignores already installed packages.


