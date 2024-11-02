# 设定

## CI schedule

```
workflowSchedule:
  setup.yml                           # ".upptimerc.yml"触发                         ，参照hst1189/uptime-monitor@master
     ⊥ Update template
     ⊥ Update response time
     ⊥ Update summary in README
     ⊥ Generate graphs
     ⊥ Generate site

  update-template.yml: "0 0 * * *"    #                                              ，参照hst1189/uptime-monitor@master
  response-time.yml: "0 0 * * *"      # update response time                         ，参照hst1189/uptime-monitor@master
  summary.yml: "0 0 * * *"            # update readme.md                             ，参照hst1189/uptime-monitor@master
  graphs.yml: "0 0 * * *"             # generate graphs                              ，参照hst1189/uptime-monitor@master
  site.yml: "0 1 * * *"               # generate site                                ，参照hst1189/uptime-monitor@master
  
  uptime.yml: "*/15 * * * *"          # 每15分钟执行死活監視                         ，参照hst1189/uptime-monitor@master
  
  updates.yml: "- - - - -"            # upptime自体更新 update code，schedule暂时禁用，参照upptime/updates@master
```



