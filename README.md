# Vikas-shell-example-project
shell scripting example project

Porject
=======
Monitoring Free Ram space
=========================
mkdir project
cd project
vi ram_status.sh

bash
#!/bin/bash

FREE_SPACE=$(free -mt | grep "Total" | awk '{print $4}')
TH=1000

if [[ $FREE_SPACE -lt $TH ]]; then
    echo "WARNING: RAM is low"
else
    echo "RAM Space is sufficient - $FREE_SPACE M"
fi
