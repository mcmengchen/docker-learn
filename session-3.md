+ Node
 - 一台物理机或者一台虚拟机
 - 

+ Pod
 - 代表一个应用 由一个或者多个 container 组成
 - 一个Pod 内多个 container 共享存储和网络

+ 组成结构
 - Node
        - Pod
            - container
            - container
            - container
        - Pod
            - container
            - container
        - ...

+ 为什么要有 pod：
 - 有一些服务的 container 之间要有协同服务的需求，一个 pod 中的两个contaner 永远不会跑在两个 node 上。


+ ReplicaSet
- 包含了一组固定数量的pods
- 使用template来创建声明数量的pods
- 保证pods数量恒定


+ Deployment
- 包含了一组ReplicaSet
- 通过控制ReplicaSet，完成版本更新、回滚、扩容
- 一个 Deployment 只能使用一种模板，模板是一组镜像的组合

+ Service
 - 包含一组pods
 - 创建虚拟ip port，通过访问service的ip port可以访问到pods
 - 采用随机负载均衡算法访问pods
 - 通过selector动态选择访问的pods
 

