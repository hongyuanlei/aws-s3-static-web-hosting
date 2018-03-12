# s3_static_web_hosting

### Run and create s3 with static web hosting

```
ansible-playbook -i inventory/dev/singapore/inentory s3_static_web_hosting.yml
```

If you want to create your own, you need to change the inventory under inventory/dev/singapore/group_vars/s3_static_web_hosting

### Run and create https + cloudfront + s3 static web hosting stack

```
ansible-playbook -i inventory/dev/singapore/inentory https_cloudfront_static_web_hosting.yml
```

If you want to create your own, you need to change the inventory under inventory/dev/singapore/group_vars/https_cloudfront_static_web_hosting

### Upload static file into s3 bucket

```Shell
npm install -g hexo-cli
hexo init site
cd site
hexo -s
hexo generate

# upload file to bucket blog.hongsuanni.com
aws s3 cp  public/ s3://blog.hongsuanni.com/ --region ap-southeast-1 --recursive
```
