# RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md

## 目的

1999—2004 年中文旧网中的招聘页、人才网、网上双选会、企业招聘专题，看起来很像普通网页，但它们的证据性质比静态个人主页复杂得多。

一个被 archive 保存下来的招聘页面，可能同时混合：

- 某个历史时点真实开放的职位；
- 已过期但仍能访问的职位；
- 从纸质招聘广告同步过来的内容；
- online-only 职位；
- 需要登录后才能看到的简历数据库；
- 不会被网页档案直接保存的雇主端候选人搜索工具；
- 后续必须在线下招聘会、电话、邮件或现场面试中完成的流程。

因此，本仓以后研究招聘类旧网页时，必须把 **页面存在、职位有效、申请路径、简历生命周期、渠道覆盖人群** 分开。

配套生活史研究：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/search-before-travel-and-passive-findability-online-recruitment-1999-2004.zh-CN.md>

---

## 1. 最基本的禁止：archived listing ≠ live vacancy

一个 2002 年被保存的招聘页面，只能直接证明：

> **某个档案系统在某个时点保存了这份页面表示。**

它不能自动证明：

- capture 当天职位仍开放；
- 招聘单位仍存在；
- 页面中的联系电话/邮箱仍有效；
- 该职位从未被撤回；
- 应聘者当时仍能通过该页面提交申请；
- 页面显示的“发布日期”就是首次上线日期。

招聘页至少要区分四个时间：

```text
posting_time        # 平台/页面声称的发布时间
application_window  # 申请有效期，若可证
capture_time        # 档案保存时间
observation_time    # 研究者今天检查的时间
```

如果页面没有明确截止日期，不能因为 archive 在某天仍能抓到页面，就把职位生命周期延长到该日。

---

## 2. 1999—2004 的招聘网站不能默认理解成“互联网替代纸媒”

51job 在 2004 年提交给美国 SEC 的 F-1 文件明确记录：

- `Career Post Weekly` 与 `51job.com` 被紧密整合；
- 纸质刊物中的招聘广告会同步发布到网站；
- 网站还包含 online-only 广告；
- 网站职位按小时更新；
- 公司认为纸媒仍能覆盖没有方便互联网接入的中低收入求职者；
- 在线渠道更容易出现年轻求职者和技术类岗位。

原始来源：

- 51job, Inc., Form F-1, filed 2004-07-07：<https://www.sec.gov/Archives/edgar/data/1295484/000114554904000896/u99016fv1.htm>

证据等级：**A — 同时代公司监管申报文件。**

公司关于“市场领先”等自我判断只能证明其主张；但对自身产品、业务流程、纸网整合、岗位更新和数据库功能的说明可以作为强原始证据使用。

因此以后看到一个早期招聘网站，必须记录：

```yaml
channel_relationship:
  online_only: unknown
  print_syndicated: unknown
  job_fair_linked: unknown
  campus_office_linked: unknown
  government_workflow_linked: unknown
```

不能只因为岗位出现在 Web 上，就默认它只通过 Web 分发。

---

## 3. 必须把“职位页面”和“候选人数据库”视为两个不同的考古对象

公开网页档案天然更容易保存：

- 招聘首页；
- 职位列表；
- 单个职位详情；
- 帮助页；
- 招聘会专题；
- 企业品牌招聘页。

但招聘平台另一个关键系统——**简历数据库**——通常需要登录、权限、查询表单和雇主账户，极难被公共 archive 完整保存。

51job 2004 年原始文件明确记载：

- 求职者可在线发布简历；
- 雇主通过 eHire 搜索候选人数据库；
- 雇主可付费下载简历；
- 雇主端还有候选人管理工具。

来源同上，证据等级：**A**。

因此：

> **absence of archived resumes ≠ absence of a resume database**

也就是说，Wayback 里只有职位页、没有候选人页，不能推断“这个平台当时只是分类广告，没有简历库”。

相反，必须单独找：

- 官方帮助页；
- 同期产品说明；
- 企业年报/监管文件；
- 雇主端教程；
- 同期招聘人员评测；
- 用户端注册/发布简历说明。

---

## 4. 新的研究单位：opportunity object 与 candidate object

早期招聘网络把两个现实对象结构化：

### opportunity object

一份职位可以被编码为：

- 城市；
- 行业；
- 职位名称；
- 公司；
- 发布日期；
- 薪资（有时）；
- 学历/经验要求；
- 联系方式或申请按钮。

### candidate object

一名求职者可以被编码为：

- 姓名或账号；
- 联系方式；
- 教育；
- 工作经历；
- 目标职位；
- 目标城市；
- 期望工资；
- 更新时间；
- 可否被雇主检索。

这两类对象的历史意义不同：

> **职位数据库使人能够远程搜索机会；候选人数据库使机会能够反向搜索人。**

后者在旧网考古中尤其容易被低估，因为公开 archive 对登录后数据库保存极差。

---

## 5. 招聘页面建议增加的最小字段

```yaml
object_type: recruitment_listing
platform:
original_url:
capture_url:
capture_datetime:

claimed_posting_date:
claimed_expiry_date:
last_updated_visible:

employer_name:
employer_identity_confidence:
employer_verification_claimed:

job_title:
job_location:
job_category:
salary_visible:
requirements_visible:

application_channel:
  web_form: unknown
  platform_resume: unknown
  email: unknown
  phone: unknown
  fax: unknown
  postal_mail: unknown
  walk_in: unknown
  job_fair: unknown

login_required:
shared_terminal_usable:

cross_channel_origin:
  online_only: unknown
  print_origin: unknown
  campus_origin: unknown
  government_program_origin: unknown

vacancy_status_at_capture: unknown
vacancy_status_evidence:

privacy_risk:
evidence_grade:
confidence:
notes:
```

`vacancy_status_at_capture` 默认应为 `unknown`，除非有明确截止时间、实时状态标记或其他同期证据。

---

## 6. 对“网上双选会”要额外记录 institutional workflow

2001 年新华社关于南京毕业生就业网站的报道显示，网络可以同时连接：

```text
单位发布岗位
→ 毕业生登记求职资料
→ 双方达成意向
→ 就业主管部门在线审核/核准
```

来源：

- 新华社 / 新浪科技，2001-12-20：<https://tech.sina.com.cn/i/c/2001-12-20/96819.shtml>

证据等级：**B — 同时代高质量媒体对机构流程的报道。**

因此招聘网站考古不能只记录 UI。

建议增加：

```yaml
institutional_workflow:
  employer_verification: unknown
  candidate_registration: unknown
  application_submission: unknown
  government_approval: unknown
  campus_approval: unknown
  offline_interview: unknown
  contract_step: unknown
```

一个页面可能是就业制度的一部分，而不是普通“商业网站”。

---

## 7. 对 2003 年 SARS 期间招聘页必须记录 shock window

2003 年 SARS 期间，部分原本依赖现场交流的招聘活动转向网络、电话和短信。

例如同期报道中的“山西毕业生网上双选周”，359 家用人单位发布 9516 条招聘信息，并形成 933 个求职意向。

来源：

- 《云南日报》 / 新浪，2003-06-17，《网上求职显身手》：<https://news.sina.com.cn/e/2003-06-17/1159227983s.shtml>

证据等级：**B — 同时代媒体报道。**

这类页面必须和常态期页面分开：

```yaml
shock_context:
  event: SARS
  ordinary_offline_channel_disrupted: true/false/unknown
  online_channel_emergency_substitute: true/false/unknown
```

不能因为 2003 年危机窗口出现大量网上招聘，就倒推 2001 年普通月份已经具有同等线上替代程度。

---

## 8. 一个非常重要的抽样偏差：archived web labor market ≠ whole labor market

51job 2004 年文件直接说明：

- 在线渠道相对更能接触年轻、技术岗位求职者；
- 纸媒仍承担覆盖没有方便网络接入的中低收入求职者的作用。

美国 Pew 2002 年调查也发现：

- 高收入、高学历互联网用户更可能在线找工作；
- skilled laborers 与 service workers 在当时相对较少使用在线求职；
- 年轻互联网用户使用率更高。

来源：

- Pew Internet Project, 2002-07-17：<https://www.pewresearch.org/internet/2002/07/17/online-job-hunting/>

证据等级：**B / institutional survey**（海外比较证据，不直接证明中国分布）。

因此研究者必须明确：

> **保存得最好的网络招聘世界，本身就可能是当时劳动市场里接入条件更好的一部分。**

一个 2003 年招聘网站看起来全部是 IT、外企、大学生岗位，可能有两种完全不同的解释：

1. 当时整个劳动市场就是这样；
2. 这个数字渠道本来就选择性地吸引这些岗位和人群。

不能在没有线下人才市场、报纸招聘、劳务市场和熟人网络对照时选择第一种解释。

---

## 9. 反例：网络也可以被组织成面向非白领的渠道

2003 年“全国首届下岗失业青年网上招聘大会”提供了一个重要反例：

- 1874 家企业；
- 41376 个岗位；
- 覆盖 28 个省区市；
- 很多岗位属于服装、机电、家政、餐饮、建筑等行业的一线操作或服务工种；
- 报道还明确提到，地方组织需要“为下岗失业青年登陆网站创造必要条件”。

来源：

- 新华社 / 新浪，2003-01-27：<https://news.sina.com.cn/s/2003-01-27/203340616s.shtml>

证据等级：**B — 同时代新华社报道。**

因此不要写：

> “早期网络招聘只服务大学生和白领。”

更准确的是：

> **普通商业网络招聘的接入和岗位结构可能偏向更年轻、更高学历和更易上网的人群；但机构化活动可以通过集中供给岗位和提供公共接入，把网络渠道扩展到其他劳动者。**

这要求记录的不只是“网站是谁办的”，还要记录**谁帮助目标人群真正进入网站**。

建议字段：

```yaml
access_intermediation:
  cybercafe: unknown
  school_lab: unknown
  public_employment_office: unknown
  youth_organization_site: unknown
  friend_or_family_device: unknown
  home_access: unknown
```

---

## 10. 旧网页中“招聘信息存在”不能证明真实机会同样可及

要区分至少五层：

```text
listing_exists
→ user_can_access_listing
→ user_is_eligible
→ user_can_submit_application
→ employer_can_receive/process_application
→ interview/hire can actually occur
```

archive 往往只能强证明第一层，有时能证明第二、第三层。

例如：

- 页面公开，但申请按钮依赖已失效脚本；
- 职位显示，但只允许某校毕业生注册；
- 简历可以填，但服务器端 CGI 已经无法验证；
- archive 保存职位页，却没有保存登录后的申请确认；
- 招聘会专题仍在，但活动已经结束。

因此 reconstruction 时不能为了“体验完整”而伪造成功申请流程。

如果后端缺失，应明确显示：

```text
historical form preserved
submission endpoint unavailable
successful application not demonstrated
```

---

## 11. 隐私：招聘资料比一般个人主页更敏感

简历天然包含高密度个人信息。

本仓研究招聘平台结构时：

- 不批量重新公开历史个人简历；
- 不为了证明数据库存在而列真实普通求职者姓名；
- 不重新暴露历史电话、邮箱、住址、身份证件或家庭信息；
- 优先引用平台帮助页、字段结构、聚合数量、匿名化截图描述；
- 若 archive 中存在公开简历页，只保留支持技术 claim 所必需的最少字段。

尤其禁止：

> 把已经失效、但仍被档案服务保存的求职者联系方式重新整理成可搜索列表。

“历史上公开过”不等于“今天适合重新扩散”。

---

## 12. 招聘平台案例的推荐 claim 模板

### 可以写

> 2004 年 51job 的监管文件证明，该平台允许求职者搜索职位、直接投递简历、跟踪申请，并允许付费雇主搜索候选人简历数据库。

### 不应直接写

> 2004 年中国人已经主要靠网络找工作。

### 可以写

> 2001 年南京的毕业生就业网站已把单位招聘、毕业生登记与部分主管部门审批纳入在线流程。

### 不应直接写

> 2001 年南京毕业生就业已经完全线上化，现场招聘不再重要。

### 可以写

> 2003 年针对下岗失业青年的全国网上招聘活动包含大量服务与一线岗位，并由地方组织帮助目标人群获得网站接入。

### 不应直接写

> 2003 年普通工人已经普遍使用互联网求职。

---

## 13. 本文新增的核心证据规则

以后旧网招聘案例必须默认遵守：

> **archived listing ≠ live vacancy**
>
> **public job page ≠ whole recruitment system**
>
> **absence of archived resumes ≠ absence of resume database**
>
> **web labor market ≠ whole labor market**
>
> **online application capability ≠ completed online hiring**
>
> **platform access ≠ target population access**

以及一条对生活史尤其重要的规则：

> **当职位和简历都变成数据库后，旧网保存的不只是“招聘广告”，而是劳动市场开始被重写成可查询对象的证据。**

这应该成为以后研究中华英才网、51job、智联招聘、地方人才网、高校就业网、招聘专题页和招聘会专题时的默认解释框架。