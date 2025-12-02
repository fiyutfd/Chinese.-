if _G.XION_Script_Loaded then
    _G.XION_Execution_Count = (_G.XION_Execution_Count or 0) + 1
    return
end

_G.XION_Script_Loaded = true
_G.XION_Execution_Count = 1

local WindUI = loadstring(game:HttpGet("https://github.com/Footagesus/WindUI/releases/latest/download/main.lua"))()

local Window = WindUI:CreateWindow({
    Title = "Chinese脚本",
    Icon = "door-open",
    Author = "",
    Folder = "你 (废物)",
    Size = UDim2.fromOffset(560, 360),
    Transparent = true,
    Theme = "Dark",
    User = {
        Enabled = true,
        Callback = function() 
            print("clicked") 
        end,
        Anonymous = true
    },
})

Window:EditOpenButton({
    Title = "打开Chinese v1",
    Icon = "monitor",
    CornerRadius = UDim.new(0,16),
    StrokeThickness = 2,
    Color = ColorSequence.new(
        Color3.fromHex("FF0F7B"),
        Color3.fromHex("F89B29")
    ),
    Draggable = true,
})

function Tab(a)
    return Window:Tab({Title = a, Icon = "eye"})
end

function Button(a, b, c)
    return a:Button({Title = b, Callback = c})
end

function Toggle(a, b, c, d)
    return a:Toggle({Title = b, Value = c, Callback = d})
end

function Slider(a, b, c, d, e, f)
    return a:Slider({Title = b, Step = 1, Value = {Min = c, Max = d, Default = e}, Callback = f})
end

function Dropdown(a, b, c, d, e)
    return a:Dropdown({Title = b, Values = c, Value = d, Callback = e})
end

local Taba = Tab("公告")
local Tab1 = Tab("通用")
local Tab7 = Tab("傻逼黑名单")
local Tab6 = Tab("各大脚本中心")
local Tab8 = Tab("更新")
local Tab2 = Tab("最强的战场")
local Tab5 = Tab("客户端")
local Tab3 = Tab("死铁轨")
local Tab9 = Tab("自然灾害")
local Tab10 = Tab("99页")
local Tab11 = Tab("Ohio")

Taba:Paragraph({
    Title = "当前用户：",
    Desc = game.Players.LocalPlayer.DisplayName, -- 直接使用玩家的用户名
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

-- 假设您有一个全局变量来存储当前使用的注入器
local currentInjector = {
    name = "AwesomeInjector", -- 注入器名称
    version = "1.2.3",       -- 注入器版本
    displayName = "Awesome Injector" -- 用于显示的名称
}

-- 创建一个包含“当前注入器”信息的 UI 段落
Taba:Paragraph({
    Title = "当前注入器",
    Desc = currentInjector.displayName, -- 显示注入器名称
    Image = "info", -- 使用信息图标
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})


Taba:Paragraph({
    Title = "作者：",
    Desc = [[Chinese]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Taba:Paragraph({
    Title = "最大帮助人：",
    Desc = [[司空]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Taba:Paragraph({
    Title = "禁止搬运",
    Desc = [[ ]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Taba:Paragraph({
    Title = "禁止二创",
    Desc = [[ ]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Slider(Tab1, "移动速度", 1, 600, game.Players.LocalPlayer.Character.Humanoid.WalkSpeed, function(a) 
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = a
end)

Slider(Tab1, "跳跃高度", 1, 600, game.Players.LocalPlayer.Character.Humanoid.JumpPower, function(a) 
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = a
end)

Slider(Tab1, "重力设置", 1, 500, workspace.Gravity, function(a) 
        workspace.Gravity = a
end)

Button(Tab1, "飞行", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
end)

Button(Tab1, "超人", function() 
    loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Invinicible-Flight-R15-45414"))()
end)

Button(Tab1, "防摔", function() 
    loadstring(game:HttpGet("http://rawscripts.net/raw/Universal-Script-Touch-fling-script-22447"))()
end)

Button(Tab5, "封禁锤", function() 
    loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Ban-hammer-v0-47112"))()
end)

Button(Tab5, "John Doe脚本", function() 
    loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-John-doe-script-by-g00byd0lan-10381"))()
end)

Button(Tab6, "北极星", function() 
    BJX_HUB = "北极星加载器"
    loadstring(game:HttpGet("https://raw.githubusercontent.com/zilinskaslandon/-/refs/heads/main/%E5%8C%97%E6%9E%81%E6%98%9F%E5%8A%A0%E8%BD%BD%E5%99%A8%E5%B7%B2%E5%8A%A0.lua"))()
end)

Button(Tab6, "混脚本", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
end)

Button(Tab6, "不知名脚本中心", function() 
    loadstring(utf8.char((function() return table.unpack({108,111,97,100,115,116,114,105,110,103,40,103,97,109,101,58,72,116,116,112,71,101,116,40,34,104,116,116,112,115,58,47,47,114,97,119,46,103,105,116,104,117,98,117,115,101,114,99,111,110,116,101,110,116,46,99,111,109,47,67,104,105,110,97,81,89,47,45,47,109,97,105,110,47,37,69,54,37,56,51,37,56,53,37,69,52,37,66,65,37,57,49,34,41,41,40,41})end)()))()
end)

Button(Tab6, "kG", function() 
    KG_SCRIPT = "张硕制作"
    loadstring(game:HttpGet("https://github.com/ZS-NB/KG/raw/main/Zhang-Shuo.lua"))()
end)

Button(Tab6, "XION", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/smalldesikon/wocaonima/main/qq984820669.txt"))()
end)

Button(Tab6, "黄某脚本", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/xiaokong6/x1/refs/heads/main/黄某脚本加载器"))()
end)

Button(Tab2, "金身", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Cyborg883/GoldenPakiFusion/refs/heads/main/Script"))()
end)

Tab8:Paragraph({
    Title = "1.0",
    Desc = [[脚本诞生了]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

 Button(Tab1, "撸管r6", function() 
    loadstring(game:HttpGet("https://pastefy.app/wa3v2Vgm/raw"))()
end)

 Button(Tab1, "撸管r15", function() 
    loadstring(game:HttpGet("https://pastefy.app/YZoglOyJ/raw"))()
end)

Button(Tab9, "v1", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/V1.lua.txt"))()
end)

Button(Tab9, "v2", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/%E7%A3%81%E9%93%81%E9%BB%91%E6%B4%9EV2.txt"))()
end)

Button(Tab9, "v3", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/V3.txt"))()
end)

Button(Tab9, "v4", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/V4.txt"))()
end)

Button(Tab9, "v5", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/V5.txt"))()
end)

Button(Tab9, "v6", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/V6.txt"))()
end)

Tab8:Paragraph({
    Title = "1.1",
    Desc = [[更新自然灾害]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Button(Tab6, "皮脚本", function() 
    getgenv().XiaoPi="皮脚本QQ群1002100032" loadstring(game:HttpGet("https://raw.githubusercontent.com/xiaopi77/xiaopi77/main/QQ1002100032-Roblox-Pi-script.lua"))()
end)

Button(Tab6, "叶脚本", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/roblox-ye/QQ515966991/refs/heads/main/ROBLOX-CNVIP-XIAOYE.lua"))()
end)

Button(Tab2, "火车头", function() 
    getgenv().settings = {
    ["morph"] = {
        ["enabled"] = false,
        ["dontchangeskincolor"] = false,
    },
    ["ult_forcewalkspeed"] = true, -- forces walkspeed even if set to 0
    ["ult_walkspeed"] = 64, -- how fast you walk in ult
    ["tp_duration"] = 0.15 -- how long it takes to tp
} 

loadstring(game:HttpGet("https://raw.githubusercontent.com/skibiditoiletfan2007/ATrainSounds/refs/heads/main/ATrain.lua"))()
end)

Button(Tab10, "DARK (需要进DC)", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/DARK.lua"))()
end)

Tab8:Paragraph({
    Title = "1.2",
    Desc = [[更新了99页]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Button(Tab6, "XK", function() 
    loadstring(game:HttpGet(('https://github.com/devslopo/DVES/raw/main/XK%20Hub')))()
end)

Toggle(Tab1, "夜视", false, function(a)
    if a then
            game.Lighting.Ambient = Color3.new(1, 1, 1)
        else
            game.Lighting.Ambient = Color3.new(0, 0, 0)
        end
end)

Button(Tab1, "无头加短腿美化", function() 
    loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Permanent-Headless-And-korblox-Script-4140"))()
end)

Button(Tab1, "踏空行走", function() 
    loadstring(game:HttpGet('https://raw.githubusercontent.com/GhostPlayer352/Test4/main/Float'))()
end)

Button(Tab6, "皮空脚本", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/smalldesikon/vv/1647f5471c89de3fba6b2f7d783173a4d51a2f54/%E5%8D%A1%E5%AF%86%E7%B3%BB%E7%BB%9F.lua"))()
end)

Button(Tab6, "皮空脚本二", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/smalldesikon/vv/c43cc7847ac9846287fad439930ac41b2d65dbe0/%E7%9A%AE%E7%A9%BA%E8%84%9A%E6%9C%AC(%E4%BA%8C)"))()
end)

Button(Tab10, "op级99夜(中文)", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/hdjsjjdgrhj/script-hub/refs/heads/main/99Nights"))()
end)

Button(Tab10, "99虚空汉化(Kenny汉化)", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ke9460394-dot/ugik/refs/heads/main/99%E5%A4%9C%E8%99%9A%E7%A9%BA.txt"))()
end)

Button(Tab10, "xa的99夜", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Xingtaiduan/Script/refs/heads/main/Games/森林中的99夜.lua"))()
end)

Button(Tab10, "99夜[疑似可以伤害队友]", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/358545698555/roblox-/refs/heads/main%E5%8F%AF%E6%9D%80%E9%98%9F%E5%8F%8B99%E5%A4%9C"))()
end)

Button(Tab1, "皮炎汉化(无卡密)", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/358545698555/roblox-/refs/heads/main%E5%8A%9B%E9%87%8F%E4%BC%A0%E5%A5%87"))()
end)

Button(Tab1, "静默破解[皮炎汉化]", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/smalldesikon/vv/1eab6c39306f06abf61c13771da42bec95f5292d/%E9%9D%99%E9%BB%98"))()
end)

Button(Tab11, "笑川Ohio", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/SUNXIAOCHUAN886/XiaoChuan/refs/heads/main/ohio.lua"))()
end)

Button(Tab11, "snow", function() 
    loadstring(game:HttpGet("https://raw.githubusercontent.com/aaajackmiller-hub/Fang/main/snow%20Ohio.lua", true))()
end)

Tab8:Paragraph({
    Title = "1.3.1",
    Desc = [[添加了Ohio和更多功能]],
    Image = "eye",
    ImageSize = 24,
    Color = Color3.fromHex("#FFFFFF"),
    BackgroundTransparency = 1,
    OutlineColor = Color3.fromHex("#FFFFFF"),
    OutlineThickness = 1,
    Padding = UDim.new(0, 1)
})

Button(Tab2, "大功能提升 (必须用致命忍者)", function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/Reapvitalized/TSB/refs/heads/main/SIONELTNAMATLASIA.lua"))()
end)
