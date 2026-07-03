# UI Components Glossary

Choose wording by component behavior. These terms describe UI patterns; they do not replace the visible user-facing copy.

| Chinese / Intent | Recommended | Avoid | Context | Notes | Risk |
|---|---|---|---|---|---|
| 空状态 | Empty state | Blank page | No content, first use | Explain absence and the next action when needed. | Medium |
| 加载中 | Loading | In loading | Page, list, button | Use a progress label only when it helps the user. | Low |
| 错误状态 | Error state | Wrong state | Page, field, request | State what failed and the recovery path. | High |
| 成功状态 | Success state | Successful state copy | Confirmation, result | Confirm the actual completed outcome. | Medium |
| 警告 | Warning | Warm prompt | Banner, modal | Do not use warning tone for neutral guidance. | Medium |
| 轻提示 | Toast | Tips popup | Temporary feedback | Keep it short; do not hide critical information in a toast. | Medium |
| 模态框 | Modal | Pop-up window | Blocking decision | Describe the decision and consequence. | High |
| 对话框 | Dialog | Dialogue box | Confirmation, input | `Dialog` can be modal or non-modal depending on the system. | Medium |
| 抽屉 | Drawer | Side pop-up | Navigation, details | Use `side panel` in user-facing documentation when clearer. | Low |
| 标签页 | Tab | Label page | Navigation | Keep sibling labels grammatically parallel. | Low |
| 筛选 | Filter | Screening | List, search | Use a noun or verb according to the control. | Low |
| 排序 | Sort | Sequence | List, table | Name the active order when useful. | Low |
| 搜索 | Search | Query | Input, button | `Search` can stand alone when the object is obvious. | Low |
| 下拉菜单 | Dropdown / Select menu | Pull-down box | Form, menu | `Select` describes the control in design systems. | Low |
| 复选框 | Checkbox | Check box button | Form, settings | Labels should describe the selected state. | Medium |
| 单选按钮 | Radio button | Single-choice button | Form | Use for mutually exclusive options. | Low |
| 输入框 | Input field | Input box | Form | Prefer the actual field label in user-facing copy. | Low |
| 多行文本框 | Text area | Multi-line input box | Form | Use for longer free-form content. | Low |
| 辅助说明 | Helper text | Tip words | Form | Put required constraints before examples. | Medium |
| 占位文案 | Placeholder | Default text | Input field | Do not use a placeholder as the only label. | Medium |
| 工具提示 | Tooltip | Hover tip | Supplemental help | Essential rules must remain visible without hover. | Medium |
| 横幅 | Banner | Banner ad | Notice, promotion | A banner can be informational, not only advertising. | Low |
| 卡片 | Card | Module box | Dashboard, feed | Do not expose the component name to users unless needed. | Low |
| 轮播 | Carousel | Swiper | Marketing, gallery | `Swiper` is a library or implementation term. | Low |
| 步骤条 | Stepper / Progress steps | Step bar | Multi-step flow | `Stepper` may also mean a numeric input; use context. | Low |
| 进度条 | Progress bar | Process bar | Upload, task | Do not imply precise progress if it is indeterminate. | Medium |
| 分页 | Pagination | Page turning | List, table | User-facing controls usually use page numbers or `Next`. | Low |
