
# Minima 简单项目分析





### 背景：
Minima创立于2018年，其创建的主要目的是考虑到以比特币为主的虚拟货币在去中心化的运作时，挖矿者负责打包交易记录上链，而打包上链的这个环节在Minima看来是一种“中心化”的行为且存在被攻击的安全隐患。特别是在项目还没有足够大时，如果挖矿者控制足够多的上链任务有可能会篡改交易内容。

### 解决方案：
“去挖矿化”，项目中没有像比特币里传统意义上的“矿工”，每个认证的移动端和PC端用户在认证后都会成为一个节点（node），每个节点都运行同一个并且完整的上链code，对比比特币——以谁能依靠算力拿到上链的资格（PoW），谁才能把交易打包上链的方式，Minima实现了竞争打包上链这个环节的“去中心化”——所有用户同时上链，以此来减少单一用户才有资格上链所带来的安全隐患。

### 运行原理：
Minima的主要运作方式是通过用户在移动端和PC端来创建node（简单教程后面会介绍），由每个node同时接收上链任务，接收到任务后，每个node只运行一部分代码，然后整合成完整的代码并且验证通过最终形成一个block并且上链。这种被称为Tx-PoW的运作模式使得Minima可以实现安全且有效的交易上链目的。

### 优势：
- a. 投入少，门槛低。比特币之类的挖矿项目，十分依赖矿工的7×24小时高强度、高能耗且竞争极其激烈的特征，Minima选择了挖矿“去中心化”和平等化。每个用户（node）不需要投入巨额挖矿设备，只需将用户自己的node（可以是手机或者PC端）接入minima network，然后通过后台运行minima来保证node运行任务
- b. 挖矿“移动化”。与其他移动挖矿项目类似，Minima 用户可以随时随地接网挖矿，设备配置和网络方面没有苛刻的要求，对于一些初学矿工甚至于日常做单做外快的用户来说十分友好。
- c. 竞争小。 由于Minima以构建node为目标，并且同一个上链任务会分散到各个node里共同执行，所以得到上链任务的用户不会存在谁先完成谁得利更多的情况，也就减少了来自于运行node设备的竞争压力，从而保障了基本的收益平均。

### 缺点：
- a. 收益扁平化。比特币等挖矿项目依靠支付挖矿奖励来刺激用户投入更多更强更贵的矿机入场，投入越多收入越多（理论上）以算力取胜，但Minima没有类似的竞争挖矿奖励，只有以接入network的node数来获得收益。所以收益最终与能接入的node数量挂钩且无法实现单一node的收益提升。
- b. 缺少作弊监控。由于Minima以用户所持node数量奖励收益，而个人批量创建新node在技术上来说是可行的。所以如何维护Minima提出的“公平化“原则，即如何避免单一用户批量创建node来获得巨额“非公平”收益，是项目做更大推广活动时需要额外考虑的。
- c. 单一用户/群体巨量持有node所带来的安全风险。由于目前创建node的低门槛特征，单一用户/群体在技术层面是可以实现操控巨量node，这种node“巨鲸“对于Minima项目的安全性和稳定性带来一定的风险。

---

### 总结：
Minima推行的移动化“挖矿”收益模式将入场门槛降到最低，足够吸引很多投资少、入行时间短的大众化用户。一定程度上可以促进更多用户加入进而提升整个chain的运行效率。以次基本层面协议构建的另外3层协议（Maxima，Omnia，MiniDPPs）可以很好的得到稳定的交易支持。随着Minima项目的推广以及node的增多，单一node的奖励会使得交易成本升高，单一用户/群体持有巨量node也会带来一定的项目安全和稳定性风险。
