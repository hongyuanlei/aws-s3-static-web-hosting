# s3_static_web_hosting

### Run and create s3 with static web hosting

```
ansible-playbook -i inventory/dev/singapore/inentory s3_static_web_hosting.yml
```

### Upload static file into s3 bucket

```Shell
npm install -g hexo-cli
hexo init site
cd site
hexo -s
hexo generate

# upload file to bucket www.hongsuanni.com
aws s3 cp  public/ s3://www.hongsuanni.com/ --region ap-southeast-1 --recursive
```
