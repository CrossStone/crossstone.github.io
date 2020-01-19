#### 存在问题

- 流程较多（类别多、流程数量多），针对每个流程都有不同的判断条件，所以不同流程需要传输不同的业务参数，双方开发实施量大；
- 业务判断较多，只要涉及判断的参数都需要在A系统中构造好，并且作为表单传输过去。目前或者后期新增的流程，在OA提供的15个限定下不知道能不能控制得住；
- 后期如果流程有变动的话（包括业务判断修改、新增流程），都需要双方系统进行调整并进行接口测试；
- *A系统和B系统可以支持往返多次驳回提交*，是否可以友好支持多次往返驳回提交审批？
- 需要把审批分成两部分。抽取只做审批的环节放入到OA系统中，需要修改表单信息的环节还保留在A系统中。那么：
  - *需要把“修改表单信息”的环节放到最开始环节或者最后环节，如果修改环节发现单据问题需要驳回，需不需要逐步审批或一驳到底并给OA的审批人员发送知会？，如果需要不知道OA可否支持。*
  
  - A系统中使用了独立的流程引擎。流程环节放在两个系统中后，审批过程中或后期在A系统中查询流程的审批过程时，不能像以前一样，可以很完美的查看审批记录和过程（包括单据查看页面、流程跟催、打印页面等）。
  

  ![城堡.jpg](http://ww1.sinaimg.cn/large/662a2aably1gb1tddzuagj21hc0u0jx8.jpg)
- 推送附件时，A系统中的业务表单可以生成pdf。但A系统，都是一个个的表格，可以查看数据来源、对应附件、校验状态、如果表格是校验失败的那么原因是什么等等需要继续点击链接才能打开的很多业务信息，肯定不可能都在OA中再次一一实现。而且表格比较大，生成的pdf效果并不好。另外领导审批时，展现的话是直接展现还是下载展现？不管哪种展现方式，都会影响使用体验。
- **A系统和B系统都是按照角色来寻找下一个或下一组承担人，并支持多人抢先**，不知OA是否可以兼容


