
#To Build
docker build -t sfgroups/docker-ansible:0.1 .

# To Run

docker run --rm -it \
    -v ~/.ssh/id_rsa:/root/.ssh/id_rsa \
    -v ~/.ssh/id_rsa.pub:/root/.ssh/id_rsa.pub \
    -v $(pwd):/ansible/playbooks \
    sfgroups/docker-ansible:0.1 site.yml

