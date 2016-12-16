##### 需求方: 刘海滨   
##### 基本诉求:
对Container进行cpu和内存限制，具体如下:

- cpu_shares : int类型，默认1024， 建议设置1024的倍数
- cpuset: str类型， 无默认值， 与cgroup设置方式一致
- mem_limit: str类型，默认 4g， 格式为数字单位， 支持b, k, m ， g 的单位。
- memswap_limit : str类型，默认 4g， 格式为数字单位， 支持b, k, m ， g 的单位

##### 使用方法: 

1. 默认设定: 默认将会进行cpushare 1024 和 mem_limit 4g 限制
   *ps: 代码升级后，重新deploy因为默认值的设定，导致与原始设定不同，将会导致重新部署*
2. 主动设定: 找到需要设定的项目的palybook，然后找调用kolla_docker模块的start_container, 添加参数。

##### Example
kolla/ansible/roles/glance/tasks/start.yml

原始内容
```yaml
- name: Starting glance-registry container
  kolla_docker:
    action: "start_container"
    common_options: "{{ docker_common_options }}"
    image: "{{ glance_registry_image_full }}"
    name: "glance_registry"
    volumes:
      - "{{ node_config_directory }}/glance-registry/:{{ container_config_directory }}/:ro"
      - "kolla_logs:/var/log/kolla/"
  when: inventory_hostname in groups['glance-registry']
```

修改后内容
```yaml
- name: Starting glance-registry container
  kolla_docker:
    action: "start_container"
    common_options: "{{ docker_common_options }}"
    image: "{{ glance_registry_image_full }}"
    name: "glance_registry"
    volumes:
      - "{{ node_config_directory }}/glance-registry/:{{ container_config_directory }}/:ro"
      - "kolla_logs:/var/log/kolla/"
    cpuset: "0-1"
    mem_limit: "2g"
  when: inventory_hostname in groups['glance-registry']
```
