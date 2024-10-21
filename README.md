# Readme
A note about Roy Thomas Fielding's PhD dissertation.

### PhD Dissertation of Roy Thomas Fielding

第一步，解释术语`架构风格`和`架构约束`，为描述Representational State Transfer架构风格做准备。

建筑 vs 软件 (糅合了我的个人观点)：
- 建筑是由建筑元素组成的，而软件是由软件元素组成的。
- 建筑有建筑结构，而软件有软件结构。
- 建筑中有水、电和燃气等介质的流动，而软件中有数据的流动。

结构 vs 架构 (糅合了我的个人观点)：
- 系统一定有结构，但是不一定有架构，只有当一个系统中的元素之间存在物料的输入和输出的时候，才称这个系统有架构。
- 结构是架构的一部分，为了描述一个系统的架构，不仅需要描述这个系统的结构，还需要描述这个系统在每一个运行阶段时的元素和物料的特点。

架构 vs 架构风格 (糅合了我的个人观点)：
- 架构和架构风格的区别类似于穿搭和穿搭风格的区别。
- 架构和架构风格的联系类似于穿搭和穿搭风格的联系。

架构风格 vs 架构约束 (糅合了我的个人观点)：
- 架构风格是对一组相关的架构约束的命名。
- 如果一个系统遵守了一种架构风格中的所有的架构约束，那么就称这个系统是属于这种架构风格的系统。

第二步，解释术语`REST components`、`resource identifier`、`resource representation`、`metadata`和`media type`，为描述Representational State Transfer架构风格做准备。

菲尔丁对术语REST components的解释 (摘抄自论文原文)：
- REST components perform actions on a resource by using a representation to capture the current or intended state of that resource and transferring that representation between components.
- REST components, summarized in Table 5-3, are typed by their roles in an overall application action.
- An origin server uses a server connector to govern the namespace for a requested resource. It is the definitive source for representations of its resources and must be the ultimate recipient of any request that intends to modify the value of its resources. Each origin server provides a generic interface to its services as a resource hierarchy. The resource implementation details are hidden behind the interface.
- A gateway (a.k.a., reverse proxy) component is an intermediary imposed by the network or origin server to provide an interface encapsulation of other services, for data translation, performance enhancement, or security enforcement.
- A proxy component is an intermediary selected by a client to provide interface encapsulation of other services, data translation, performance enhancement, or security protection.
- A user agent uses a client connector to initiate a request and becomes the ultimate recipient of the response.

菲尔丁对术语resource、resource representation和resource identifier的解释 (摘抄自论文原文)：
- Any information that can be named can be a resource: a document or image, a temporal service (e.g. "today's weather in Los Angeles"), a collection of other resources, a non-virtual object (e.g. a person), and so on.
- A resource is a conceptual mapping to a set of entities, not the entity that corresponds to the mapping at any particular point in time.
- More precisely, a resource R is a temporally varying membership function M<sub>R</sub>(t), which for time t maps to a set of entities, or values, which are equivalent. The values in the set may be resource representations and/or resource identifiers.

菲尔丁对术语metadata的解释 (摘抄自论文原文)：
- Metadata is in the form of name-value pairs, where the name corresponds to a standard that defines the value's structure and semantics.

菲尔丁对术语media type的解释 (摘抄自论文原文)：
- The data format of a representation is known as a media type.

第三步，描述`Representational State Transfer架构风格`。

只有当一个系统遵守了以下6个架构约束时，才称这个系统是Representational State Transfer架构风格的系统 (揉合了我的个人观点)：
- Client-Server：Client负责界面交互，Server负责数据存储。
- Stateless (Server)：Server不存储session context，Client存储session context（如果有的话）。
- Cache：Server在每个响应中标记当前响应中的数据是否可以被缓存，Client根据该标记操作缓存。
- Uniform Interface：所有的REST component都使用统一的接口输入和输出数据，具体表现为以下4个方面：
  - 所有的REST component都使用resource identifier定位resource。
  - 所有的REST component都使用resource representation操作resource。
  - 所有的REST component都使用metadata描述和理解resource和resource representation的属性。
  - 所有的REST component都使用media type描述和理解resource representation的数据格式。
- Layered System：系统是分层的，而且每一层都只服务其上一层、只调用其下一层，不进行跨层服务、跨层调用。
- Code-On-Demand (可选)：Client可以从Server下载Java applet、JavaScript script代码并执行以按需拓展Client的功能。

### Credits
- [Architectural Styles and the Design of Network-based Software Architectures](https://ics.uci.edu/~fielding/pubs/dissertation/top.htm)
