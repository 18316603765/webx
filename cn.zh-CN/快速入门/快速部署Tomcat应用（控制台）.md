# 快速部署Tomcat应用（控制台） {#concept_263470 .concept}

Web+可让您轻松创建和部署应用。本文旨在指导您如何快速使用Web+创建并部署一个Tomcat作为应用容器的示例应用。

## 前提条件 {#section_6sq_wht_uma .section}

-   已开通Web+服务，具体操作请参见[开通Web+服务](../../../../cn.zh-CN/准备工作/开通相关服务并授权.md#section_e7m_lmj_c0l)。
-   创建部署环境使用的VPC和交换机，具体操作请参见[创建VPC](../../SP_22/DNVPC11885991/ZH-CN_TP_2434_V13.dita#concept_isl_ghv_rdb)。

    **说明：** 当创建一个云产品实例时，如果没有可用的专有网络和交换机，您可以使用默认专有网络和交换机。在实例创建后，一个默认的专有网络和交换机也会随之创建好。在Web+中如果您没有设置专有网络和交换机，部署环境中的网络会选择为默认VPC和交换机。


## 创建应用及部署环境 {#section_lvf_s28_gp1 .section}

使用Web+，您需先创建一个应用和部署环境，应用部署包上传到应用所在的部署环境内，然后配置环境参数并完成应用部署。

![](images/48242_zh-CN.png "部署应用流程图")

1.  登录[Web+控制台](https://webplus.console.aliyun.com)。
2.  在**概览**页**最近更新的部署环境**区域的右上角单击**新建**。
3.  在**应用基本信息**页面设置应用基本信息，设置完成后单击**下一步**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/217610/156048110649170_zh-CN.png)

    |配置|说明|
    |--|--|
    |技术栈类型|此处可以选择**Tomcat**或**Java**，选择两种技术栈的部署包类型会有差异。在本文中将选择**Tomcat**作为示例，Tomcat作为应用容器支持使用WAR或ZIP类型的应用部署包。|
    |应用名称|设置应用名称，此处设置为doc-test作为示例。应用名称仅支持大小写字母、数字，及中划线（-）、下划线（\_）两种特殊字符，名称长度不能超过64个字符。|
    |应用描述（可选）|输入一段描述信息帮助您识别这个应用，此处设置为文档测试作为示例。输入文字长度不能超过1024个字符。|

4.  在**部署环境信息**页面设置环境和部署包信息，完成设置后单击**完成创建**，然后在弹出的**提示**对话框中单击**确认**完成部署环境的创建。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/217610/156048110649172_zh-CN.png)

    |配置|说明|
    |--|--|
    |部署环境名称|设置部署环境名称，此处设置为test-env作为示例。部署环境名称仅支持大小写字母、数字，及中划线（-）、下划线（\_）两种特殊字符，名称长度不能超过64个字符。|
    |部署环境描述|输入创建应用的部署环境的描述，此处设置为文档测试环境作为示例。描述长度不能超过1024个字符。|
    |部署包来源|您可以选择**上传本地程序**或**使用样例程序**。此处选择**使用样例程序**作为示例，您无需手动上传部署包，Web+已经默认上传好样例程序的部署包。 **说明：** 若您选择**上传本地程序**，您可单击**选择文件**来将本地部署包上传至Web+。

 |
    |部署包版本|Web+会默认生成一个部署包版本号，您也可以自定义该版本。|
    |版本描述|输入一段描述信息帮助您识别部署包的版本，此处设置为部署包V1作为示例。输入文字长度不能超过1024个字符。|

5.  在**完成创建**页面可查看应用的创建进度：

    -   单击**查看该应用**或**完成创建**可进入**应用详情**页面。
    -   单击**查看部署包版本**可进入部署包版本管理页面。
    -   单击**查看部署环境日志**可进入环境变更事件页面。
    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/217610/156048110649173_zh-CN.png)


## 查看部署环境信息并访问应用 {#section_ikl_3o1_utr .section}

创建应用及部署环境之后，您可以进入[Web+控制台](https://webplus.console.aliyun.com)中的部署环境的**概览**页面，在该页面可以对环境进行常见配置，包括启停、部署、重启、释放和删除环境等操作，还可以查看环境的版本、运行状态、技术栈、负责人、操作时间、访问地址以及环境最近生成的事件的列表。

1.  登录[Web+控制台](https://webplus.console.aliyun.com)。
2.  在**概览**页**最近更新的部署环境**区域的右上角单击**查看全部**，在**应用及部署环境页面**单击所选应用的ID进入**部署环境管理**页面。

    **说明：** 进入应用详情页后一般默认是在**部署环境管理**页面，若不在**部署环境管理**页面，请在应用详情页面的左侧导航栏单击**部署环境管理**。

3.  选择并单击部署环境名称进入部署环境**概览**页面。
4.  当应用的运行状态为**运行中**时，您可单击**访问地址**右侧的链接地址，进入应用首页查看应用。

    **说明：** 当部署环境运行状态最终显示为**异常**时，您可尝试在页面右上角单击**重建**使部署环境恢复正常。


## 删除应用 {#section_b7l_47j_4g1 .section}

删除应用前必须先释放应用内的所有部署环境。当您释放部署环境后，部署环境中的ECS、SLB等资源将会被释放进而终止相应资源的计费，您只需支付存储所产生的很少的费用。

1.  **释放环境**：
    1.  登录[Web+控制台](https://webplus.console.aliyun.com)。
    2.  在**概览**页**最近更新的部署环境**区域的右上角单击**查看全部**，在**应用及部署环境页面**单击要删除应用的ID进入**部署环境管理**页面。

        **说明：** 进入应用详情页后一般默认是在**部署环境管理**页面，若不在**部署环境管理**页面，请在应用详情页面的左侧导航栏单击**部署环境管理**。

    3.  选择一个未释放的环境，在环境卡片右上角单击 ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/159334/156048110746681_zh-CN.png) ，然后在下拉列表中单击**释放** 。
    4.  在**确定释放部署环境**对话框内输入要释放的环境名称，然后单击**确定**。
    5.  如果一个应用部署在多个环境内，重复上面步骤iii-iv完成应用内的所有环境的释放操作。
2.  返回应用的**部署环境管理**页面，单击页面右上角的**删除**，在**确定删除应用**对话框中单击**确认**完成应用的删除。

## 更多信息 {#section_dag_0mc_a2b .section}

-   部署应用的详细配置步骤请参见[部署应用](../DNICMS19100635/ZH-CN_TP_159334_V1.dita)。
-   Web+不仅可以在控制台完成应用的托管，还可以通过命令行来完成所有托管操作，使用CLI的托管操作请参见[CLI命令](../DNICMS19100639/ZH-CN_TP_161078_V1.dita)。
-   完成应用托管之后的应用的管理操作请参见[应用管理](../DNICMS19100635/ZH-CN_TP_163214_V1.dita)。
-   管理应用所在的环境的操作请参见[部署环境概览](../DNICMS19100636/ZH-CN_TP_163212_V1.dita)。

## 问题反馈 {#section_ayn_lyd_oho .section}

如果您在使用Web+过程中有任何疑问，欢迎您扫描下面的二维码加入钉钉群进行反馈。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/217610/156048110748521_zh-CN.jpg)

