# Flash

https://www.adobe.com/products/flashplayer/end-of-life.html

http://web.archive.org/web/20210115230817/https://www.adobe.com/products/flashplayer/end-of-life.html

https://www.423down.com/2082.html

<pre>
Windows Registry Editor Version 5.00

;导入Flash优化设置 支持Chromium/Chrome/新版Edge .

;AllowOutdatedPlugins	是否允许加载过期的Flash插件，1表示允许，0表示禁止，建议开启，避免flash狂刷版本号，频繁更新，根据自身情况酌情修改
;RunAllFlashInAllowMode	如果启用此设置（即设置为1），那么在内容设置中设为允许运行 Flash（无论是由用户还是由企业政策设置）的网站中内嵌的所有 Flash 内容（包括来自其他来源的内容或不重要的内容）都会运行。
;DefaultPluginsSetting	默认Flash设置，1 = 强制所有网站自动运行 Flash 插件，且用户无法再设置中关闭，2 = 禁止 Flash 插件运行，3 = 点击运行，类似先提示再运行【注，Chrome85以后版本此项的1已经被官方取消，为了兼容老版本，1选项与3选项效果相同】
;HardwareAccelerationModeEnabled	启用硬件加速，即使用GPU渲染网页,打开对3D 图形 API 的支持，1为开，0为关
;PluginsAllowedForUrls	强制允许Flash运行的白名单网站，即该项下面的值。键值名表示第几项规则序号，键值内容为白名单网站，我已经帮你匹配了所有域名了。
;特别说明：PluginsAllowedForUrls和DefaultPluginsSetting是结合使用的，两者不能分开，单独设置DefaultPluginsSetting是无效的，强制开启必须同时指定强制运行的白名单网址


;Chromium需要导入到User这个根键下面，否则不生效
[HKEY_CURRENT_USER\SOFTWARE\Policies\Chromium]
"AllowOutdatedPlugins"=dword:00000001
"RunAllFlashInAllowMode"=dword:00000001
"DefaultPluginsSetting"=dword:00000001
"HardwareAccelerationModeEnabled"=dword:00000001

[HKEY_CURRENT_USER\SOFTWARE\Policies\Chromium\PluginsAllowedForUrls]
"1"="https://*"
"2"="http://*"


;导入Chrome Flash优化设置 ，请注意注册表路径与Chromium不一样，chrome导入到MACHINE根键下面，并且子路径也与Chromium不同
[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome]
"AllowOutdatedPlugins"=dword:00000001
"RunAllFlashInAllowMode"=dword:00000001
"DefaultPluginsSetting"=dword:00000001
"HardwareAccelerationModeEnabled"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Google\Chrome\PluginsAllowedForUrls]
"1"="https://*"
"2"="http://*"


;导入新版Edge优化设置
[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge]
"AllowOutdatedPlugins"=dword:00000001
"RunAllFlashInAllowMode"=dword:00000001
"DefaultPluginsSetting"=dword:00000001
"HardwareAccelerationModeEnabled"=dword:00000001

[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Edge\PluginsAllowedForUrls]
"1"="https://*"
"2"="http://*"
</pre>
