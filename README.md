# Readme
A note about Roy Thomas Fielding's PhD dissertation.

### PhD Dissertation of Roy Thomas Fielding

建筑 vs 软件：
- 建筑是由建筑元素组成的，而软件是由软件元素组成的。
- 建筑有建筑结构，而软件有软件结构。
- 建筑中有水、电和燃气等介质的流动，而软件中有数据的流动。

结构 vs 架构：
- 系统一定有结构，而只有当一个系统中的元素之间存在物料的输入和输出的时候，才称这个系统有架构。
- 为了描述一个系统的架构，不仅需要描述这个系统的结构，还需要描述这个系统在每一个运行阶段时的元素和物料的特点。

架构 vs 架构风格：
- 某种穿搭是相对具体的，而某种穿搭风格是相对抽象的。

只有当一个系统的架构遵守以下6个约束时，才称这个系统是Representational State Transfer架构风格的系统：
- Client-Server：Client负责界面交互，Server负责数据存储。
- Stateless (Server)：Server不存储session context，Client存储session context（如果有的话）。
- Cache：Server在每个响应中标记当前响应中的数据是否可以被缓存，Client根据该标记操作缓存。
- Uniform Interface：
- Layered System：系统是分层的，每一层都只服务其上一层、只调用其下一层，不进行跨层服务或调用。
- Code-On-Demand (可选的)：Client可以从Server下载Java applet、JavaScript script代码并执行用以按需拓展Client的功能。

### Credits
- [Architectural Styles and the Design of Network-based Software Architectures](https://ics.uci.edu/~fielding/pubs/dissertation/top.htm)
