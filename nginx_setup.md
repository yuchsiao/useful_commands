# nginx setup

+ Check port listening
  ```bash
  sudo netstat -peanut
  ```

+ Totally reinstall nginx
  ```bash
  sudo apt-get autoremove nginx
  sudo apt-get --purge remove nginx
  sudo apt-get autoremove && sudo apt-get autoclean
  sudo find / | grep nginx | sudo xargs rm -rf
  
  # Add ppa
  sudo add-apt-repository ppa:nginx/stable
  
  # Install
  sudo apt-get update && sudo apt-get -f install nginx
  ```
  
+ Configure nginx
  ```bash
  cd /etc/nginx
  vi sites-available/default
  ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/default
  service nginx restart
  ```
  
