gleanindia
==========

Clean India
Setup in ubuntu 12.10:

Create a VirtualENV:

      pip install virtualenv
      virtualenv gleanindia
      git clone git://github.com/kennethreitz/autoenv.git ~/.autoenv
      echo 'source ~/.autoenv/activate.sh' >> ~/.bashrc
      pip install -r requirements.txt
      
Download GAE:

      cd ~
      mkdir google_projects
      cd google_projects
      wget -O gae.zip http://googleappengine.googlecode.com/files/google_appengine_1.7.5.zip
      unzip gae.zip
      rm gae.zip


Add to System Path: 

      vi ~/.bashrc

add the following(****change to your directory)

      PATH=$PATH:/home/your_user_name/your_project_folder/google_appengine/

Clone the repo:

      cd ~/google_projects
      git clone https://github.com/tabraiz12/gleanindia.git

if path is added properly this will work:

      dev_appserver.py ~/google_projects/gleanindia/Gleanindia/
else:

      python ~/google_projects/google_appengine/dev_appserver.py ~/google_projects/gleanindia/Gleanindia/
      
Run in:

      http://localhost:8080

to deploy to gleanindia.appspot.com:

      ~/google_projects/google_appengine/appcfg.py update ~/google_projects/gleanindia/Gleanindia/
