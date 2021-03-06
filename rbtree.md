# 红黑树讲解

## 红黑树的性质
1. 每个节点不是红色就是黑色

2. 不可能有连在一起的红色节点
    - 如果某个节点是红色的，那么它的子节点一定都是黑色的
    - 如果某个节点是红色的，那么它的父节点一定是黑色的
    - 两个黑色连在一起是可以的

3. 根节点 root 是黑色的

4. 每个红色节点的两个子节点都是黑色。叶子节点（NULL节点）都是黑色：出度为0满足了性质就可以近似的平衡

## 红黑树的操作
1. 改变颜色

2. 旋转

## 红黑树变换规则

旋转和颜色变换规则：**所有插入的点默认为红色**

1. **变颜色的情况**：当前节点的父亲是红色，且它的祖父节点的另一个子节（叔叔节点）点也是红色
    - （1）把父亲节点设置为黑色
    - （2）把叔叔也设为黑色
    - （3）把祖父节点（爷爷节点）设置为红色
    - （4）把指针定义到祖父节点，设为当前要操作的（爷爷），分析的点变换的规则
2. **左旋**：当前父节点是红色，叔叔是黑色的时候，且当前的节点是右子树。
    - 左旋，以父节点作为左旋转
3. **右旋**：当前父节点是红色，叔叔节点是黑色的时候，且当前的节点是左子树。
    - 右旋
    - （1） 把父节点变为黑色
    - （2） 把祖父节点变为红色（爷爷）
    - （3） 以祖父节点旋转（爷爷）