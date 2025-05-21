### Dria
Dria is the universal execution layer for AI: optimizing every model, on any engine, across all hardware.

### Daftar Vikey

Daftar vikey

https://vikey.ai/user/api/keys

### Setup vikey
```
git clone https://github.com/Dwentzart/Dria
cd dria
```
```
chmod +× vikey-inference-linux
```
* nano .env
```
VIKEY_API_KEY=
NODE_PORT=11434
```
```
nano /etc/systemd/system/vikey.service
```
* masukan ini
```
[Unit]
Description=Vikey Inference Server
After=network.target
[Service]
ExecStart=/root/dria/vikey-inference-linux
WorkingDirectory=/root/dria
Restart=always
User=root
Environment=NODE_ENV=production
[Install]
WantedBy=multi-user.target
```
### Runing menggunakan Vikey

Berikan izin eksekusi pada script dria.sh:

```
chmod +x ./dria-setup.sh
```
* Jalankan script dengan akses sudo:
```
sudo ./dria-setup.sh setup --count 1
```
* Upgrade
```
docker-compose down --remove-orphans
```
```
docker system prune -a
```
```
docker network create --subnet=10.173.1.0/24 dria-network

```
```
docker-compose up -d
```
