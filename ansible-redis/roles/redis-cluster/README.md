## 全新安裝

    ```bash
    ansible-playbook -i roles/redis-cluster/inventories/host -e "action=install" main.yml
    ```