 1905  cd monitoring/
 1906  sudo cp -r statsd/ /usr/share/
 1907  cd /usr/share/statsd/
 1908  sudo mkdir -p /etc/statsd
 1909  sudo cp localConfig.js /etc/statsd
 1910  sudo cp -r debian/scripts .
 1911  sudo mkdir -p /var/log/statsd
 1912  sudo chown root.nogroup /var/log/statsd
 1913  sudo chmod 770 /var/log/statsd
 1914  sudo cp debian/statsd.upstart /etc/init/statsd.conf
 1915  sudo ln -s /lib/init/upstart-job /etc/init.d/statsd
 1916  sudo update-rc.d statsd defaults
 1917  screen -x
 1918  screen -x 2626.pts-0.ip-10-145-150-66 
 1919  sudo start statsd
 1920  ps aux | grep 7393
