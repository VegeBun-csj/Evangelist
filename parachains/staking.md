# Staking
波卡使用NPOS(Nominated proof-of-stake)作为其共识机制。系统鼓励DOT持有者去参与成为提名人。提名人最多可以选择16个验证人作为受信任的验证人候选者。验证人和提名人都会将他们的代币锁定作为抵押，并接收质押奖励。

整个质押系统基本上在不考虑质押的情况会平等地向所有验证人支付奖励。在一个验证人上投入更多质押并不会影响它收到的块奖励的数量。然而，奖励计算存在概率成分，所以在特定时间段，奖励对于所有的验证人可能不完全相同。

在扣除验证人的基本质押金额后，奖励会按比例分配给所有的质押参与者。通过这种方式，网络为具有较低质押金额的验证人创造了提名激励，从而创建一个平等质押的验证人集合。

## 波卡中的质押是如何工作的？
### 1.确定你是哪种角色
在质押中，你可以是[提名人或者是验证人](https://wiki.polkadot.network/zh-CN/docs/learn-staking#validators-and-nominators)   
作为一个提名人，你可以提名验证人候选者，也就是你信任可以帮助你赚取链的原生代币的一个角色。赚取的奖励可以立即绑定(锁定)在您的帐户进行质押，也就是说随着时间的推移，你可以有效地复用你所获得的奖励。你也可以选择将奖励存储到你的账户，或者是另一个账户作为可用(可转移)余额。你可以参考[提名人指南](https://wiki.polkadot.network/zh-CN/docs/learn-nominator)来理解作为一个提名人的职责，以及[验证人文档](https://wiki.polkadot.network/zh-CN/docs/learn-validator)来了解需要做什么才能成为一个验证人。

如果你是一个新手并且想要通过Polkadpt JS APP安全地质押你的代币，可以看下面的视频
<iframe width="560" height="315" src="https://www.youtube.com/embed/FCXC0CDhyS4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### 2.质押系统概述
任何一个潜在的验证人都会想他们成为一个验证人候选者。系统中的候选人会向所有提名人公开，而提名人则提交其支持的最多16名候选人的名单。在下一个阶段，一定数量的拥有最多DOT支持的验证人会被选中并活跃起来。作为一个提名人，最少需要10个DOT来提交提名意向。提名意向被放在一个半排序的列表中，称为[“包列表”](https://github.com/paritytech/substrate/pull/9507)。包列表有两个主要组件，包和节点。列表由包组成，每个包都描述了一系列活跃的绑定的资产(例如，第一个包会有0->10 DOT的提名人，第二个包会有11->20DOT的提名人，等等)。每个包中是一个节点列表，对应于一个提名人以及他们的质押资产。




















