# termux




## SSH into phone 

pkg install openssh


username
whoami     

local ip
ifconfig

set new password
passwd


sshd -D -p 8822 -d


### from computer on same network

ssh -p 8822 username@localip



ssh-keygen -t ed25519 -f ~/.ssh/phone-erl -N "" && ssh-copy-id -i ~/.ssh/phone-erl.pub phone-erl



## files

termux-setup-storage


cd ~/storage

ncdu
find ~/storage -type f -exec du -h {} + | sort -hr | head -n 20

TOTAL=$(wc -l < music_files.txt)

pv -l -s "$TOTAL" music_files.txt | zip -@ music_collection.zip


cd ~/storage/music

find . -type f \( \
  -iname "*.mp3" -o \
  -iname "*.flac" -o \
  -iname "*.ogg" -o \
  -iname "*.m4a" -o \
  -iname "*.wav" \
\) > music_files.txt



# in termux

pkg install openssh
sshd
ifconfig
whoami
passwd


# laptop 
ssh -p 8022 u0_a287@192.168.43.108 Tablet
ssh -p 8022 u0_a164@192.168.43.116 Redmi 7
ssh -p 8022 u0_a215@192.168.43.215 Redmi 13c


# then docker in termux 

https://github.com/cyberkernelofficial/docker-in-termux

pkg install qemu-utils qemu-common qemu-system-x86_64-headless wget -y
mkdir alpine && cd alpine
wget http://dl-cdn.alpinelinux.org/alpine/v3.20/releases/x86_64/alpine-virt-3.20.2-x86_64.iso
qemu-img create -f qcow2 alpine.img 5G
qemu-system-x86_64 -machine q35 -m 1024 -smp cpus=2 -cpu qemu64 -drive if=pflash,format=raw,read-only=on,file=$PREFIX/share/qemu/edk2-x86_64-code.fd -netdev user,id=n1,dns=8.8.8.8,hostfwd=tcp::2222-:22 -device virtio-net,netdev=n1 -cdrom alpine-virt-3.20.2-x86_64.iso -nographic alpine.img


