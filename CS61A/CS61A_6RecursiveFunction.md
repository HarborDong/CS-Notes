# 递归

自己调用自己  
**function 在被调用时除了 return 前都不会离开这个 function**

步骤：
- 计算 base cases (不用递归)
- 计算 recursive cases (用递归)

## 环境图中的递归
- 相同的 function 被多次调用
- 不同的 frames 每次跟踪不同的 arguments
- arguments 的值取决于当前的环境
- 每次调用解决一个比之前调用时的更简单的问题

## 循环 vs 递归
- 循环是递归的特殊形式
- 运用的公式有区别

## 对待递归的方法
- 检验 base case
- 把递归的方法视为一个方法上的抽象
- 假设递归 f(n-1) 是正确的，检验 f(n) 是否正确

## 相互递归 (mutual recursion)
function A 调用 function B，function B 调用 function A
应用：
- 信用卡校验和
- 检验一个数奇数还是偶数
- 两个人互相玩游戏

## 把递归转化为迭代
- 会很 tricky
  - 因为迭代是递归的特殊形式
- 要知道迭代需要保持什么状态

## 把迭代转化为递归
- 更加直接，更泛用化
  - 因为迭代是递归的特殊形式
- 迭代时候的状态可以被作为 arguments 传递至递归方法

## 树递归
树递归函数视为探索各种可能性的方法
- 一个函数多次调用自身
- 如果两个递归相同，更短的会更好
- 但有些时候，更长的会更好(有清楚的递归递终止条件)
- 当写递归时，把 base cases 放在最上面