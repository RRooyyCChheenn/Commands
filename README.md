# Compressed file
## 1. zip file
"""
for file in /data/NFS_rawzip/*.zip; do
    unzip "$file" -d /data/NFS_rawzip/
done
"""

# Environmental migration
## 1. Conda Environment
### Steps:
scp -r /data/xiangru/anaconda3/envs/raft xiangru@166.111.54.115:/data/xiangru/anaconda3/envs/
Note: 1. "/data/xiangru/anaconda3/envs/raft", this whole raft folder will be transfered
2. "/data/xiangru/anaconda3/envs/": no need to create raft manually, the whole raft folder will be stored in the envs/
