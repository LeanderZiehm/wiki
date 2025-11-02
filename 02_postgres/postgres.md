sudo -i -u postgres
psql



psql -U postgres -h your_host -p 5432 > full_cluster_backup.sql
psql -h 127.0.0.1 -p 5432 -U postgres -d postgres

pg_dumpall -U postgres -h your_host -p 5432 > full_cluster_backup.sql


pg_dump -U your_db_user -h your_db_host -p 5432 -F c -b -v -f backup_file.dump your_database_name


# Change Password
sudo -u postgres psql
ALTER ROLE your_db_user WITH PASSWORD 'new_secure_password';
\q




---

### 1. Edit `postgresql.conf` to listen on all addresses

```bash
sudo -i -u postgres
vim /etc/postgresql/14/main/postgresql.conf
```

In `vim`:

1. Press `/` then type `listen_addresses` and hit `Enter` (search).
2. Once on the line, press `i` to enter **insert mode**.
3. Change it to:

```
listen_addresses = '*'
```

4. Press `Esc` to exit insert mode.
5. Type `:wq` and hit `Enter` to save and quit.

---

### 2. Edit `pg_hba.conf` to allow any IP

```bash
vim /etc/postgresql/14/main/pg_hba.conf
```

In `vim`:

1. Scroll to the bottom using `G`.
2. Press `o` to open a new line below.
3. Add this line:

```
host    bookmarkdb    bookmarkapp    0.0.0.0/0    md5
```

* `bookmarkdb` → your database
* `bookmarkapp` → your role
* `0.0.0.0/0` → allows any IPv4
* `md5` → password authentication

4. Press `Esc` and type `:wq` to save and quit.

---

### 3. Restart Postgres to apply

```bash
sudo systemctl restart postgresql
```

---

After this, you can connect from anywhere using:

```bash
psql -h <YOUR_SERVER_IP> -p 5432 -U bookmarkapp -d bookmarkdb
```

It will prompt for the password of `bookmarkapp`.

If you want, I can give a **one-liner vim trick** to do both edits without scrolling manually—super fast for cloud instances. Do you want that?
