Налаштування Vagrant машини:

Створив Vagrantfile для віртуальної машини на базі Ubuntu 20.04.
Включив портфорвардинг для Nginx (гостьовий порт 80 до хостового порту 8080).
Додав Host-only мережевий інтерфейс для доступу до машини по локальній мережі.
Основні команди:
config.vm.network "forwarded_port", guest: 80, host: 8080
config.vm.network "private_network", type: "dhcp"

Встановлення та налаштування Nginx:

Встановив Nginx для веб-сервера.
Налаштував автоматичний запуск Nginx при завантаженні системи.
Основні команди:
sudo apt install nginx
sudo systemctl start nginx
sudo systemctl enable nginx

Встановлення та налаштування Fail2Ban для SSH:

Встановив Fail2Ban для захисту від підбору паролів на SSH.
Налаштував максимальну кількість спроб для підключення до SSH (5 спроб з блокуванням на 10 хвилин).
sudo apt install fail2ban
sudo systemctl restart fail2ban

Налаштування брандмауера (UFW):

Встановив та налаштував UFW для контролю мережевого доступу.
Дозволив доступ до портів 80 (HTTP) та 22 (SSH).
Заблокував доступ до SSH з певних IP-адрес і дозволив з інших.
Основні команди:
sudo ufw allow 80/tcp
sudo ufw allow 22/tcp
sudo ufw deny from бла-бла to any port 22
sudo ufw allow from бла-бла to any port 22

Створення нового розділу на диску:

Використав fdisk для створення нового розділу на додатковому диску.
Форматував розділ у файлову систему ext4.
Створив точку монтування та змонтував розділ у директорію /mnt/newdisk.
основні команди:
sudo fdisk /dev/sdb
sudo mkfs.ext4 /dev/sdb1
sudo mkdir /mnt/newdisk
sudo mount /dev/sdb1 /mnt/newdisk

Налаштування автоматичного монтування розділу при завантаженні:

Отримав UUID нового розділу і налаштував автоматичне монтування через /etc/fstab.
Основні команди:
sudo blkid /dev/sdb1
sudo nano /etc/fstab
UUID=<UUID> /mnt/newdisk ext4 defaults 0 2
sudo mount -a


