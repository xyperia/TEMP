#!/bin/sh
echo -e '* - memlock unlimited\n* - nofile 100000\n* - nproc 32768\n* - as unlimited' | sudo tee -a /etc/security/limits.conf
echo -e 'vm.max_map_count=262145' | sudo tee /etc/sysctl.conf
echo -e '172.28.200.242 dc-master-elastic-01' | sudo tee /etc/hosts
echo -e '172.28.200.243 dc-master-elastic-02' | sudo tee /etc/hosts
echo -e '172.28.200.244 dc-master-elastic-03' | sudo tee /etc/hosts
echo -e '172.28.200.245 dc-data-elastic-01' | sudo tee /etc/hosts
echo -e '172.28.200.246 dc-data-elastic-02' | sudo tee /etc/hosts
echo -e '172.28.200.247 dc-data-elastic-03' | sudo tee /etc/hosts
echo -e '172.28.200.248 dc-data-elastic-04' | sudo tee /etc/hosts
