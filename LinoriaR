--!nolint
--!nocheck
--!native
--!optimize 2

--[[
    Linoria (RIOT Version)

    This file was built with DarkLua, it is not intended for manual editing.
--]]

local a a={cache={},load=function(b)if not a.cache[b]then a.cache[b]={c=a[b]()}
end return a.cache[b].c end}do function a.a()local b={}b.ProtectGui=function(c)
local d=cloneref and cloneref(game)or game local e,f=pcall(function()c.Parent=
gethui and gethui()or cloneref and cloneref(d:GetService'CoreGui')or d:
GetService'CoreGui'end)return e and c or error('Failed to protect GUI: '..
tostring(f))end b.ProtectGui=newcclosure and newcclosure(b.ProtectGui)or b.
ProtectGui b.SecureService=function(c)local d=cloneref and cloneref(game)or game
local e,f=pcall(function()return cloneref and cloneref(d:GetService(c))or d:
GetService(c)end)return e and f or error('Unable to retrieve service: '..c)end b
.SecureService=newcclosure and newcclosure(b.SecureService)or b.SecureService
function b.GetPlayer()local c,d=pcall(function()return(b.SecureService'Players')
end)return c and(d).LocalPlayer or nil end function b.GetCharacter(c)local d,e=
pcall(function()return c and c.Character or nil end)return d and e or nil end
function b.GetHumanoid(c)local d,e=pcall(function()local d=b.GetCharacter(c)
return d and d:FindFirstChildOfClass'Humanoid'or nil end)return d and e or nil
end return b end function a.b()local b=a.load'a'local c,d=b.SecureService,
getgenv().protectgui local e,f,g,h,i,j,k=c'UserInputService',c'TextService',c
'CoreGui',c'Teams',c'Players',c'RunService',c'TweenService'local l,m=j.
RenderStepped,i.LocalPlayer local n=m:GetMouse()if not d then d=function(o)local
p,q=pcall(function()o.Parent=gethui and gethui()or c'CoreGui'end)if p then
return o else error('Failed to protect GUI: '..tostring(q))end end d=newcclosure
and newcclosure(d)or d end local o=Instance.new'ScreenGui'd(o)o.ZIndexBehavior=
Enum.ZIndexBehavior.Global o.Parent=g local p,q,r={Registry={},RegistryMap={},
HudRegistry={},FontColor=Color3.fromRGB(255,255,255),MainColor=Color3.fromRGB(28
,28,28),BackgroundColor=Color3.fromRGB(20,20,20),AccentColor=Color3.fromRGB(0,85
,255),OutlineColor=Color3.fromRGB(50,50,50),RiskColor=Color3.fromRGB(255,50,50),
Black=Color3.new(0,0,0),Font=Enum.Font.Code,OpenedFrames={},DependencyBoxes={},
Signals={},ScreenGui=o,Toggles={},Options={}},0,0 table.insert(p.Signals,l:
Connect(function(s)q=q+s if q>=(1.6666666666666665E-2)then q=0 r=r+(2.5E-3)if r>
1 then r=0 end p.CurrentRainbowHue=r p.CurrentRainbowColor=Color3.fromHSV(r,0.8,
1)end end))local s,t=function()local s=i:GetPlayers()for t=1,#s do s[t]=s[t].
Name end table.sort(s,function(t,u)return t<u end)return s end,function()local s
=h:GetTeams()for t=1,#s do s[t]=s[t].Name end table.sort(s,function(t,u)return t
<u end)return s end function p:SafeCallback(u,...)if(not u)then return end if
not p.NotifyOnError then return u(...)end local v,w=pcall(u,...)if not v then
local x,y=w:find':%d+: 'if not y then return p:Notify(w)end return p:Notify(w:
sub(y+1),3)end return nil end function p:AttemptSave()if p.SaveManager then p.
SaveManager:Save()end end function p:Create(u,v)local w=u if type(u)=='string'
then w=Instance.new(u)end for x,y in next,v do w[x]=y end return w end function
p:ApplyTextStroke(u)u.TextStrokeTransparency=1 p:Create('UIStroke',{Color=Color3
.new(0,0,0),Thickness=1,LineJoinMode=Enum.LineJoinMode.Miter,Parent=u})end
function p:CreateLabel(u,v)local w=p:Create('TextLabel',{BackgroundTransparency=
1,Font=p.Font,TextColor3=p.FontColor,TextSize=16,TextStrokeTransparency=0})p:
ApplyTextStroke(w)p:AddToRegistry(w,{TextColor3='FontColor'},v)return p:Create(w
,u)end function p:MakeDraggable(u,v)u.Active=true u.InputBegan:Connect(function(
w)if w.UserInputType==Enum.UserInputType.MouseButton1 then local x=Vector2.new(n
.X-u.AbsolutePosition.X,n.Y-u.AbsolutePosition.Y)if x.Y>(v or 40)then return end
while e:IsMouseButtonPressed(Enum.UserInputType.MouseButton1)do u.Position=UDim2
.new(0,n.X-x.X+(u.Size.X.Offset*u.AnchorPoint.X),0,n.Y-x.Y+(u.Size.Y.Offset*u.
AnchorPoint.Y))l:Wait()end end end)end function p:AddToolTip(u,v)local w,x=p:
GetTextBounds(u,p.Font,14)local y=p:Create('Frame',{BackgroundColor3=p.MainColor
,BorderColor3=p.OutlineColor,Size=UDim2.fromOffset(w+5,x+4),ZIndex=100,Parent=p.
ScreenGui,Visible=false})local z=p:CreateLabel{Position=UDim2.fromOffset(3,1),
Size=UDim2.fromOffset(w,x),TextSize=14,Text=u,TextColor3=p.FontColor,
TextXAlignment=Enum.TextXAlignment.Left,ZIndex=y.ZIndex+1,Parent=y}p:
AddToRegistry(y,{BackgroundColor3='MainColor',BorderColor3='OutlineColor'})p:
AddToRegistry(z,{TextColor3='FontColor'})local A=false v.MouseEnter:Connect(
function()if p:MouseIsOverOpenedFrame()then return end A=true y.Position=UDim2.
fromOffset(n.X+15,n.Y+12)y.Visible=true while A do j.Heartbeat:Wait()y.Position=
UDim2.fromOffset(n.X+15,n.Y+12)end end)v.MouseLeave:Connect(function()A=false y.
Visible=false end)end function p:OnHighlight(u,v,w,x)u.MouseEnter:Connect(
function()local y=p.RegistryMap[v]for z,A in next,w do v[z]=p[A]or A if y and y.
Properties[z]then y.Properties[z]=A end end end)u.MouseLeave:Connect(function()
local y=p.RegistryMap[v]for z,A in next,x do v[z]=p[A]or A if y and y.Properties
[z]then y.Properties[z]=A end end end)end function p:MouseIsOverOpenedFrame()for
u,v in next,p.OpenedFrames do local w,x=u.AbsolutePosition,u.AbsoluteSize if n.X
>=w.X and n.X<=w.X+x.X and n.Y>=w.Y and n.Y<=w.Y+x.Y then return true end end
return nil end function p:IsMouseOverFrame(u)local v,w=u.AbsolutePosition,u.
AbsoluteSize if n.X>=v.X and n.X<=v.X+w.X and n.Y>=v.Y and n.Y<=v.Y+w.Y then
return true end return nil end function p:UpdateDependencyBoxes()for u,v in next
,p.DependencyBoxes do v:Update()end end function p:MapValue(u,v,w,x,y)return(1-(
(u-v)/(w-v)))*x+((u-v)/(w-v))*y end function p:GetTextBounds(u,v,w,x)local y=f:
GetTextSize(u,w,v,x or Vector2.new(1920,1080))return y.X,y.Y end function p:
GetDarkerColor(u)local v,w,x=Color3.toHSV(u)return Color3.fromHSV(v,w,x/1.5)end
p.AccentColorDark=p:GetDarkerColor(p.AccentColor)function p:AddToRegistry(u,v,w)
local x=#p.Registry+1 local y={Instance=u,Properties=v,Idx=x}table.insert(p.
Registry,y)p.RegistryMap[u]=y if w then table.insert(p.HudRegistry,y)end end
function p:RemoveFromRegistry(u)local v=p.RegistryMap[u]if v then for w=#p.
Registry,1,-1 do if p.Registry[w]==v then table.remove(p.Registry,w)end end for
w=#p.HudRegistry,1,-1 do if p.HudRegistry[w]==v then table.remove(p.HudRegistry,
w)end end p.RegistryMap[u]=nil end end function p:UpdateColorsUsingRegistry()for
u,v in next,p.Registry do for w,x in next,v.Properties do if type(x)=='string'
then v.Instance[w]=p[x]elseif type(x)=='function'then v.Instance[w]=x()end end
end end function p:GiveSignal(u)table.insert(p.Signals,u)end function p:Unload()
for u=#p.Signals,1,-1 do local v=table.remove(p.Signals,u)v:Disconnect()end if p
.OnUnload then p.OnUnload()end o:Destroy()end function p:OnUnload(u)p.OnUnload=u
end p:GiveSignal(o.DescendantRemoving:Connect(function(u)if p.RegistryMap[u]then
p:RemoveFromRegistry(u)end end))local u={}do local v={}function v:AddColorPicker
(w,x)local y=self.TextLabel assert(x.Default,
'AddColorPicker: Missing default value.')local z={Value=x.Default,Transparency=x
.Transparency or 0,Type='ColorPicker',Title=type(x.Title)=='string'and x.Title
or'Color picker',Callback=x.Callback or function(z)end}function z:SetHSVFromRGB(
A)local B,C,D=Color3.toHSV(A)z.Hue=B z.Sat=C z.Vib=D end z:SetHSVFromRGB(z.Value
)local A=p:Create('Frame',{BackgroundColor3=z.Value,BorderColor3=p:
GetDarkerColor(z.Value),BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(0,28,0,
14),ZIndex=6,Parent=y})p:Create('ImageLabel',{BorderSizePixel=0,Size=UDim2.new(0
,27,0,13),ZIndex=5,Image='http://www.roblox.com/asset/?id=12977615774',Visible=
not not x.Transparency,Parent=A})local B=p:Create('Frame',{Name='Color',
BackgroundColor3=Color3.new(1,1,1),BorderColor3=Color3.new(0,0,0),Position=UDim2
.fromOffset(A.AbsolutePosition.X,A.AbsolutePosition.Y+18),Size=UDim2.fromOffset(
230,x.Transparency and 271 or 253),Visible=false,ZIndex=15,Parent=o})A:
GetPropertyChangedSignal'AbsolutePosition':Connect(function()B.Position=UDim2.
fromOffset(A.AbsolutePosition.X,A.AbsolutePosition.Y+18)end)local C=p:Create(
'Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=p.OutlineColor,
BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=16,Parent=B})
local D,E=p:Create('Frame',{BackgroundColor3=p.AccentColor,BorderSizePixel=0,
Size=UDim2.new(1,0,0,2),ZIndex=17,Parent=C}),p:Create('Frame',{BorderColor3=
Color3.new(0,0,0),Position=UDim2.new(0,4,0,25),Size=UDim2.new(0,200,0,200),
ZIndex=17,Parent=C})local F=p:Create('Frame',{BackgroundColor3=p.BackgroundColor
,BorderColor3=p.OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0
,1,0),ZIndex=18,Parent=E})local G=p:Create('ImageLabel',{BorderSizePixel=0,Size=
UDim2.new(1,0,1,0),ZIndex=18,Image='rbxassetid://4155801252',Parent=F})local H=p
:Create('ImageLabel',{AnchorPoint=Vector2.new(0.5,0.5),Size=UDim2.new(0,6,0,6),
BackgroundTransparency=1,Image='http://www.roblox.com/asset/?id=9619665977',
ImageColor3=Color3.new(0,0,0),ZIndex=19,Parent=G})p:Create('ImageLabel',{Size=
UDim2.new(0,H.Size.X.Offset-2,0,H.Size.Y.Offset-2),Position=UDim2.new(0,1,0,1),
BackgroundTransparency=1,Image='http://www.roblox.com/asset/?id=9619665977',
ZIndex=20,Parent=H})local I=p:Create('Frame',{BorderColor3=Color3.new(0,0,0),
Position=UDim2.new(0,208,0,25),Size=UDim2.new(0,15,0,200),ZIndex=17,Parent=C})
local J=p:Create('Frame',{BackgroundColor3=Color3.new(1,1,1),BorderSizePixel=0,
Size=UDim2.new(1,0,1,0),ZIndex=18,Parent=I})local K,L=p:Create('Frame',{
BackgroundColor3=Color3.new(1,1,1),AnchorPoint=Vector2.new(0,0.5),BorderColor3=
Color3.new(0,0,0),Size=UDim2.new(1,0,0,1),ZIndex=18,Parent=J}),p:Create('Frame',
{BorderColor3=Color3.new(0,0,0),Position=UDim2.fromOffset(4,228),Size=UDim2.new(
0.5,-6,0,20),ZIndex=18,Parent=C})local M=p:Create('Frame',{BackgroundColor3=p.
MainColor,BorderColor3=p.OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=
UDim2.new(1,0,1,0),ZIndex=18,Parent=L})p:Create('UIGradient',{Color=
ColorSequence.new{ColorSequenceKeypoint.new(0,Color3.new(1,1,1)),
ColorSequenceKeypoint.new(1,Color3.fromRGB(212,212,212))},Rotation=90,Parent=M})
local N=p:Create('TextBox',{BackgroundTransparency=1,Position=UDim2.new(0,5,0,0)
,Size=UDim2.new(1,-5,1,0),Font=p.Font,PlaceholderColor3=Color3.fromRGB(190,190,
190),PlaceholderText='Hex color',Text='#FFFFFF',TextColor3=p.FontColor,TextSize=
14,TextStrokeTransparency=0,TextXAlignment=Enum.TextXAlignment.Left,ZIndex=20,
Parent=M})p:ApplyTextStroke(N)local O=p:Create(L:Clone(),{Position=UDim2.new(0.5
,2,0,228),Size=UDim2.new(0.5,-6,0,20),Parent=C})local P,Q,R,S=(p:Create(O.Frame:
FindFirstChild'TextBox',{Text='255, 255, 255',PlaceholderText='RGB color',
TextColor3=p.FontColor}))if x.Transparency then Q=p:Create('Frame',{BorderColor3
=Color3.new(0,0,0),Position=UDim2.fromOffset(4,251),Size=UDim2.new(1,-8,0,15),
ZIndex=19,Parent=C})R=p:Create('Frame',{BackgroundColor3=z.Value,BorderColor3=p.
OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=19,
Parent=Q})p:AddToRegistry(R,{BorderColor3='OutlineColor'})p:Create('ImageLabel',
{BackgroundTransparency=1,Size=UDim2.new(1,0,1,0),Image=
'http://www.roblox.com/asset/?id=12978095818',ZIndex=20,Parent=R})S=p:Create(
'Frame',{BackgroundColor3=Color3.new(1,1,1),AnchorPoint=Vector2.new(0.5,0),
BorderColor3=Color3.new(0,0,0),Size=UDim2.new(0,1,1,0),ZIndex=21,Parent=R})end p
:CreateLabel{Size=UDim2.new(1,0,0,14),Position=UDim2.fromOffset(5,5),
TextXAlignment=Enum.TextXAlignment.Left,TextSize=14,Text=z.Title,TextWrapped=
false,ZIndex=16,Parent=C}local T={}do T.Options={}T.Container=p:Create('Frame',{
BorderColor3=Color3.new(),ZIndex=14,Visible=false,Parent=o})T.Inner=p:Create(
'Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=p.OutlineColor,
BorderMode=Enum.BorderMode.Inset,Size=UDim2.fromScale(1,1),ZIndex=15,Parent=T.
Container})p:Create('UIListLayout',{Name='Layout',FillDirection=Enum.
FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,Parent=T.Inner})p:
Create('UIPadding',{Name='Padding',PaddingLeft=UDim.new(0,4),Parent=T.Inner})
local U,V=function()T.Container.Position=UDim2.fromOffset((A.AbsolutePosition.X+
A.AbsoluteSize.X)+4,A.AbsolutePosition.Y+1)end,function()local U=60 for V,W in
next,T.Inner:GetChildren()do if W:IsA'TextLabel'then U=math.max(U,W.TextBounds.X
)end end T.Container.Size=UDim2.fromOffset(U+8,T.Inner.Layout.
AbsoluteContentSize.Y+4)end A:GetPropertyChangedSignal'AbsolutePosition':
Connect(U)T.Inner.Layout:GetPropertyChangedSignal'AbsoluteContentSize':Connect(V
)task.spawn(U)task.spawn(V)p:AddToRegistry(T.Inner,{BackgroundColor3=
'BackgroundColor',BorderColor3='OutlineColor'})function T:Show()self.Container.
Visible=true end function T:Hide()self.Container.Visible=false end function T:
AddOption(W,X)if type(X)~='function'then X=function()end end local Y=p:
CreateLabel{Active=false,Size=UDim2.new(1,0,0,15),TextSize=13,Text=W,ZIndex=16,
Parent=self.Inner,TextXAlignment=Enum.TextXAlignment.Left}p:OnHighlight(Y,Y,{
TextColor3='AccentColor'},{TextColor3='FontColor'})Y.InputBegan:Connect(function
(Z)if Z.UserInputType~=Enum.UserInputType.MouseButton1 then return end X()end)
end T:AddOption('Copy color',function()p.ColorClipboard=z.Value p:Notify(
'Copied color!',2)end)T:AddOption('Paste color',function()if not p.
ColorClipboard then return p:Notify('You have not copied a color!',2)end z:
SetValueRGB(p.ColorClipboard)return nil end)T:AddOption('Copy HEX',function()
pcall(setclipboard,z.Value:ToHex())p:Notify('Copied hex code to clipboard!',2)
end)T:AddOption('Copy RGB',function()pcall(setclipboard,table.concat({math.
floor(z.Value.R*255),math.floor(z.Value.G*255),math.floor(z.Value.B*255)},', '))
p:Notify('Copied RGB values to clipboard!',2)end)end p:AddToRegistry(C,{
BackgroundColor3='BackgroundColor',BorderColor3='OutlineColor'})p:AddToRegistry(
D,{BackgroundColor3='AccentColor'})p:AddToRegistry(F,{BackgroundColor3=
'BackgroundColor',BorderColor3='OutlineColor'})p:AddToRegistry(M,{
BackgroundColor3='MainColor',BorderColor3='OutlineColor'})p:AddToRegistry(O.
Frame,{BackgroundColor3='MainColor',BorderColor3='OutlineColor'})p:
AddToRegistry(P,{TextColor3='FontColor'})p:AddToRegistry(N,{TextColor3=
'FontColor'})local U={}for V=0,1,0.1 do table.insert(U,ColorSequenceKeypoint.
new(V,Color3.fromHSV(V,1,1)))end p:Create('UIGradient',{Color=ColorSequence.new(
U),Rotation=90,Parent=J})N.FocusLost:Connect(function(V)if V then local W,X=
pcall(Color3.fromHex,N.Text)if W and typeof(X)=='Color3'then z.Hue,z.Sat,z.Vib=
Color3.toHSV(X)end end z:Display()end)P.FocusLost:Connect(function(V)if V then
local W,X,Y=P.Text:match'(%d+),%s*(%d+),%s*(%d+)'if W and X and Y then z.Hue,z.
Sat,z.Vib=Color3.toHSV(Color3.fromRGB(W,X,Y))end end z:Display()end)function z:
Display()z.Value=Color3.fromHSV(z.Hue,z.Sat,z.Vib)G.BackgroundColor3=Color3.
fromHSV(z.Hue,1,1)p:Create(A,{BackgroundColor3=z.Value,BackgroundTransparency=z.
Transparency,BorderColor3=p:GetDarkerColor(z.Value)})if R then R.
BackgroundColor3=z.Value S.Position=UDim2.new(1-z.Transparency,0,0,0)end H.
Position=UDim2.new(z.Sat,0,1-z.Vib,0)K.Position=UDim2.new(0,0,z.Hue,0)N.Text='#'
..z.Value:ToHex()P.Text=table.concat({math.floor(z.Value.R*255),math.floor(z.
Value.G*255),math.floor(z.Value.B*255)},', ')p:SafeCallback(z.Callback,z.Value)p
:SafeCallback(z.Changed,z.Value)end function z:OnChanged(V)z.Changed=V V(z.Value
)end function z:Show()for V,W in next,p.OpenedFrames do if V.Name=='Color'then V
.Visible=false p.OpenedFrames[V]=nil end end B.Visible=true p.OpenedFrames[B]=
true end function z:Hide()B.Visible=false p.OpenedFrames[B]=nil end function z:
SetValue(V,W)local X=Color3.fromHSV(V[1],V[2],V[3])z.Transparency=W or 0 z:
SetHSVFromRGB(X)z:Display()end function z:SetValueRGB(V,W)z.Transparency=W or 0
z:SetHSVFromRGB(V)z:Display()end G.InputBegan:Connect(function(V)if V.
UserInputType==Enum.UserInputType.MouseButton1 then while e:
IsMouseButtonPressed(Enum.UserInputType.MouseButton1)do local W=G.
AbsolutePosition.X local X=W+G.AbsoluteSize.X local Y,Z=math.clamp(n.X,W,X),G.
AbsolutePosition.Y local _=Z+G.AbsoluteSize.Y local aa=math.clamp(n.Y,Z,_)z.Sat=
(Y-W)/(X-W)z.Vib=1-((aa-Z)/(_-Z))z:Display()l:Wait()end p:AttemptSave()end end)J
.InputBegan:Connect(function(aa)if aa.UserInputType==Enum.UserInputType.
MouseButton1 then while e:IsMouseButtonPressed(Enum.UserInputType.MouseButton1)
do local V=J.AbsolutePosition.Y local W=V+J.AbsoluteSize.Y local X=math.clamp(n.
Y,V,W)z.Hue=((X-V)/(W-V))z:Display()l:Wait()end p:AttemptSave()end end)A.
InputBegan:Connect(function(aa)if aa.UserInputType==Enum.UserInputType.
MouseButton1 and not p:MouseIsOverOpenedFrame()then if B.Visible then z:Hide()
else T:Hide()z:Show()end elseif aa.UserInputType==Enum.UserInputType.
MouseButton2 and not p:MouseIsOverOpenedFrame()then T:Show()z:Hide()end end)if R
then R.InputBegan:Connect(function(aa)if aa.UserInputType==Enum.UserInputType.
MouseButton1 then while e:IsMouseButtonPressed(Enum.UserInputType.MouseButton1)
do local V=R.AbsolutePosition.X local W=V+R.AbsoluteSize.X local X=math.clamp(n.
X,V,W)z.Transparency=1-((X-V)/(W-V))z:Display()l:Wait()end p:AttemptSave()end
end)end p:GiveSignal(e.InputBegan:Connect(function(aa)if aa.UserInputType==Enum.
UserInputType.MouseButton1 then local V,W=B.AbsolutePosition,B.AbsoluteSize if n
.X<V.X or n.X>V.X+W.X or n.Y<(V.Y-20-1)or n.Y>V.Y+W.Y then z:Hide()end if not p:
IsMouseOverFrame(T.Container)then T:Hide()end end if aa.UserInputType==Enum.
UserInputType.MouseButton2 and T.Container.Visible then if not p:
IsMouseOverFrame(T.Container)and not p:IsMouseOverFrame(A)then T:Hide()end end
end))z:Display()z.DisplayFrame=A p.Options[w]=z return self end function v:
AddKeyPicker(aa,w)local x,y=self,self.TextLabel assert(w.Default,
'AddKeyPicker: Missing default value.')local z={Value=w.Default,Toggled=false,
Mode=w.Mode or'Toggle',Type='KeyPicker',Callback=w.Callback or function(z)end,
ChangedCallback=w.ChangedCallback or function(z)end,SyncToggleState=w.
SyncToggleState or false}if z.SyncToggleState then w.Modes={'Toggle'}w.Mode=
'Toggle'end local A=p:Create('Frame',{BackgroundColor3=Color3.new(0,0,0),
BorderColor3=Color3.new(0,0,0),Size=UDim2.new(0,28,0,15),ZIndex=6,Parent=y})
local B=p:Create('Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=p.
OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=7,
Parent=A})p:AddToRegistry(B,{BackgroundColor3='BackgroundColor',BorderColor3=
'OutlineColor'})local C,D=p:CreateLabel{Size=UDim2.new(1,0,1,0),TextSize=13,Text
=w.Default,TextWrapped=true,ZIndex=8,Parent=B},p:Create('Frame',{BorderColor3=
Color3.new(0,0,0),Position=UDim2.fromOffset(y.AbsolutePosition.X+y.AbsoluteSize.
X+4,y.AbsolutePosition.Y+1),Size=UDim2.new(0,60,0,47),Visible=false,ZIndex=14,
Parent=o})y:GetPropertyChangedSignal'AbsolutePosition':Connect(function()D.
Position=UDim2.fromOffset(y.AbsolutePosition.X+y.AbsoluteSize.X+4,y.
AbsolutePosition.Y+1)end)local E=p:Create('Frame',{BackgroundColor3=p.
BackgroundColor,BorderColor3=p.OutlineColor,BorderMode=Enum.BorderMode.Inset,
Size=UDim2.new(1,0,1,0),ZIndex=15,Parent=D})p:AddToRegistry(E,{BackgroundColor3=
'BackgroundColor',BorderColor3='OutlineColor'})p:Create('UIListLayout',{
FillDirection=Enum.FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,
Parent=E})local F,G,H=p:CreateLabel({TextXAlignment=Enum.TextXAlignment.Left,
Size=UDim2.new(1,0,0,18),TextSize=13,Visible=false,ZIndex=110,Parent=p.
KeybindContainer},true),w.Modes or{'Always','Toggle','Hold'},{}for I,J in next,G
do local K,L={},p:CreateLabel{Active=false,Size=UDim2.new(1,0,0,15),TextSize=13,
Text=J,ZIndex=16,Parent=E}function K:Select()for M,N in next,H do N:Deselect()
end z.Mode=J L.TextColor3=p.AccentColor p.RegistryMap[L].Properties.TextColor3=
'AccentColor'D.Visible=false end function K:Deselect()z.Mode=nil L.TextColor3=p.
FontColor p.RegistryMap[L].Properties.TextColor3='FontColor'end L.InputBegan:
Connect(function(M)if M.UserInputType==Enum.UserInputType.MouseButton1 then K:
Select()p:AttemptSave()end end)if J==z.Mode then K:Select()end H[J]=K end
function z:Update()if w.NoUI then return end local K=z:GetState()F.Text=string.
format('[%s] %s (%s)',z.Value,w.Text,z.Mode)F.Visible=true F.TextColor3=K and p.
AccentColor or p.FontColor p.RegistryMap[F].Properties.TextColor3=K and
'AccentColor'or'FontColor'local L,M=0,0 for N,O in next,p.KeybindContainer:
GetChildren()do if O:IsA'TextLabel'and O.Visible then L=L+18 if(O.TextBounds.X>M
)then M=O.TextBounds.X end end end p.KeybindFrame.Size=UDim2.new(0,math.max(M+10
,210),0,L+23)end function z:GetState()if z.Mode=='Always'then return true elseif
z.Mode=='Hold'then if z.Value=='None'then return false end local K=z.Value if K
=='MB1'or K=='MB2'then return K=='MB1'and e:IsMouseButtonPressed(Enum.
UserInputType.MouseButton1)or K=='MB2'and e:IsMouseButtonPressed(Enum.
UserInputType.MouseButton2)else return e:IsKeyDown(Enum.KeyCode[z.Value])end
else return z.Toggled end end function z:SetValue(K)local L,M=K[1],K[2]C.Text=L
z.Value=L H[M]:Select()z:Update()end function z:OnClick(K)z.Clicked=K end
function z:OnChanged(K)z.Changed=K K(z.Value)end if x.Addons then table.insert(x
.Addons,z)end function z:DoClick()if x.Type=='Toggle'and z.SyncToggleState then
x:SetValue(not x.Value)end p:SafeCallback(z.Callback,z.Toggled)p:SafeCallback(z.
Clicked,z.Toggled)end local K=false A.InputBegan:Connect(function(L)if L.
UserInputType==Enum.UserInputType.MouseButton1 and not p:MouseIsOverOpenedFrame(
)then K=true C.Text=''local M,N=''task.spawn(function()while(not N)do if M==
'...'then M=''end M=M..'.'C.Text=M wait(0.4)end end)wait(0.2)local O O=e.
InputBegan:Connect(function(P)local Q if P.UserInputType==Enum.UserInputType.
Keyboard then Q=P.KeyCode.Name elseif P.UserInputType==Enum.UserInputType.
MouseButton1 then Q='MB1'elseif P.UserInputType==Enum.UserInputType.MouseButton2
then Q='MB2'end N=true K=false C.Text=Q z.Value=Q p:SafeCallback(z.
ChangedCallback,P.KeyCode or P.UserInputType)p:SafeCallback(z.Changed,P.KeyCode
or P.UserInputType)p:AttemptSave()O:Disconnect()end)elseif L.UserInputType==Enum
.UserInputType.MouseButton2 and not p:MouseIsOverOpenedFrame()then D.Visible=
true end end)p:GiveSignal(e.InputBegan:Connect(function(L)if(not K)then if z.
Mode=='Toggle'then local M=z.Value if M=='MB1'or M=='MB2'then if M=='MB1'and L.
UserInputType==Enum.UserInputType.MouseButton1 or M=='MB2'and L.UserInputType==
Enum.UserInputType.MouseButton2 then z.Toggled=not z.Toggled z:DoClick()end
elseif L.UserInputType==Enum.UserInputType.Keyboard then if L.KeyCode.Name==M
then z.Toggled=not z.Toggled z:DoClick()end end end z:Update()end if L.
UserInputType==Enum.UserInputType.MouseButton1 then local M,N=D.AbsolutePosition
,D.AbsoluteSize if n.X<M.X or n.X>M.X+N.X or n.Y<(M.Y-20-1)or n.Y>M.Y+N.Y then D
.Visible=false end end end))p:GiveSignal(e.InputEnded:Connect(function(L)if(not
K)then z:Update()end end))z:Update()p.Options[I]=z return self end u.__index=v u
.__namecall=function(aa,w,...)return v[w](...)end end local aa={}do local v={}
function v:AddBlank(w)local x=self local y=x.Container p:Create('Frame',{
BackgroundTransparency=1,Size=UDim2.new(1,0,0,w),ZIndex=1,Parent=y})end function
v:AddLabel(w,x)local y,z={},self local A=z.Container local B=p:CreateLabel{Size=
UDim2.new(1,-4,0,15),TextSize=14,Text=w,TextWrapped=x or false,TextXAlignment=
Enum.TextXAlignment.Left,ZIndex=5,Parent=A}if x then local C=select(2,p:
GetTextBounds(w,p.Font,14,Vector2.new(B.AbsoluteSize.X,math.huge)))B.Size=UDim2.
new(1,-4,0,C)else p:Create('UIListLayout',{Padding=UDim.new(0,4),FillDirection=
Enum.FillDirection.Horizontal,HorizontalAlignment=Enum.HorizontalAlignment.Right
,SortOrder=Enum.SortOrder.LayoutOrder,Parent=B})end y.TextLabel=B y.Container=A
function y:SetText(C)B.Text=C if x then local D=select(2,p:GetTextBounds(C,p.
Font,14,Vector2.new(B.AbsoluteSize.X,math.huge)))B.Size=UDim2.new(1,-4,0,D)end z
:Resize()end if(not x)then setmetatable(y,u)end z:AddBlank(5)z:Resize()return y
end function v:AddButton(...)local w,x={},function(w,x,...)local y=select(1,...)
if type(y)=='table'then x.Text=y.Text x.Func=y.Func x.DoubleClick=y.DoubleClick
x.Tooltip=y.Tooltip else x.Text=select(1,...)x.Func=select(2,...)end assert(
type(x.Func)=='function','AddButton: `Func` callback is missing.')end x('Button'
,w,...)local y=self local z,A,B=y.Container,function(z)local A=p:Create('Frame',
{BackgroundColor3=Color3.new(0,0,0),BorderColor3=Color3.new(0,0,0),Size=UDim2.
new(1,-4,0,20),ZIndex=5})local B=p:Create('Frame',{BackgroundColor3=p.MainColor,
BorderColor3=p.OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,
1,0),ZIndex=6,Parent=A})local C=p:CreateLabel{Size=UDim2.new(1,0,1,0),TextSize=
14,Text=z.Text,ZIndex=6,Parent=B}p:Create('UIGradient',{Color=ColorSequence.new{
ColorSequenceKeypoint.new(0,Color3.new(1,1,1)),ColorSequenceKeypoint.new(1,
Color3.fromRGB(212,212,212))},Rotation=90,Parent=B})p:AddToRegistry(A,{
BorderColor3='Black'})p:AddToRegistry(B,{BackgroundColor3='MainColor',
BorderColor3='OutlineColor'})p:OnHighlight(A,A,{BorderColor3='AccentColor'},{
BorderColor3='Black'})return A,B,C end,function(z)local A,B=function(A,B,C)local
D=Instance.new'BindableEvent'local E=A:Once(function(...)if type(C)=='function'
and C(...)then D:Fire(true)else D:Fire(false)end end)task.delay(B,function()E:
disconnect()D:Fire(false)end)return D.Event:Wait()end,function(A)if p:
MouseIsOverOpenedFrame()then return false end if A.UserInputType~=Enum.
UserInputType.MouseButton1 then return false end return true end z.Outer.
InputBegan:Connect(function(C)if not B(C)then return end if z.Locked then return
end if z.DoubleClick then p:RemoveFromRegistry(z.Label)p:AddToRegistry(z.Label,{
TextColor3='AccentColor'})z.Label.TextColor3=p.AccentColor z.Label.Text=
'Are you sure?'z.Locked=true local D=A(z.Outer.InputBegan,0.5,B)p:
RemoveFromRegistry(z.Label)p:AddToRegistry(z.Label,{TextColor3='FontColor'})z.
Label.TextColor3=p.FontColor z.Label.Text=z.Text task.defer(rawset,z,'Locked',
false)if D then p:SafeCallback(z.Func)end return end p:SafeCallback(z.Func)end)
end w.Outer,w.Inner,w.Label=A(w)w.Outer.Parent=z B(w)function w:AddTooltip(C)if
type(C)=='string'then p:AddToolTip(C,self.Outer)end return self end function w:
AddButton(...)local C={}x('SubButton',C,...)self.Outer.Size=UDim2.new(0.5,-2,0,
20)C.Outer,C.Inner,C.Label=A(C)C.Outer.Position=UDim2.new(1,3,0,0)C.Outer.Size=
UDim2.fromOffset(self.Outer.AbsoluteSize.X-2,self.Outer.AbsoluteSize.Y)C.Outer.
Parent=self.Outer function C:AddTooltip(D)if type(D)=='string'then p:AddToolTip(
D,self.Outer)end return C end if type(C.Tooltip)=='string'then C:AddTooltip(C.
Tooltip)end B(C)return C end if type(w.Tooltip)=='string'then w:AddTooltip(w.
Tooltip)end y:AddBlank(5)y:Resize()return w end function v:AddDivider()local w,x
=self,self.Container w:AddBlank(2)local y=p:Create('Frame',{BackgroundColor3=
Color3.new(0,0,0),BorderColor3=Color3.new(0,0,0),Size=UDim2.new(1,-4,0,5),ZIndex
=5,Parent=x})local z=p:Create('Frame',{BackgroundColor3=p.MainColor,BorderColor3
=p.OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=
6,Parent=y})p:AddToRegistry(y,{BorderColor3='Black'})p:AddToRegistry(z,{
BackgroundColor3='MainColor',BorderColor3='OutlineColor'})w:AddBlank(9)w:Resize(
)end function v:AddInput(w,x)assert(x.Text,'AddInput: Missing `Text` string.')
local y,z={Value=x.Default or'',Numeric=x.Numeric or false,Finished=x.Finished
or false,Type='Input',Callback=x.Callback or function(y)end},self local A=z.
Container p:CreateLabel{Size=UDim2.new(1,0,0,15),TextSize=14,Text=x.Text,
TextXAlignment=Enum.TextXAlignment.Left,ZIndex=5,Parent=A}z:AddBlank(1)local B=p
:Create('Frame',{BackgroundColor3=Color3.new(0,0,0),BorderColor3=Color3.new(0,0,
0),Size=UDim2.new(1,-4,0,20),ZIndex=5,Parent=A})local C=p:Create('Frame',{
BackgroundColor3=p.MainColor,BorderColor3=p.OutlineColor,BorderMode=Enum.
BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=6,Parent=B})p:AddToRegistry(C,{
BackgroundColor3='MainColor',BorderColor3='OutlineColor'})p:OnHighlight(B,B,{
BorderColor3='AccentColor'},{BorderColor3='Black'})if type(x.Tooltip)=='string'
then p:AddToolTip(x.Tooltip,B)end p:Create('UIGradient',{Color=ColorSequence.new
{ColorSequenceKeypoint.new(0,Color3.new(1,1,1)),ColorSequenceKeypoint.new(1,
Color3.fromRGB(212,212,212))},Rotation=90,Parent=C})local D=p:Create('Frame',{
BackgroundTransparency=1,ClipsDescendants=true,Position=UDim2.new(0,5,0,0),Size=
UDim2.new(1,-5,1,0),ZIndex=7,Parent=C})local E=p:Create('TextBox',{
BackgroundTransparency=1,Position=UDim2.fromOffset(0,0),Size=UDim2.fromScale(5,1
),Font=p.Font,PlaceholderColor3=Color3.fromRGB(190,190,190),PlaceholderText=x.
Placeholder or'',Text=x.Default or'',TextColor3=p.FontColor,TextSize=14,
TextStrokeTransparency=0,TextXAlignment=Enum.TextXAlignment.Left,ZIndex=7,Parent
=D})p:ApplyTextStroke(E)function y:SetValue(F)if x.MaxLength and#F>x.MaxLength
then F=F:sub(1,x.MaxLength)end if y.Numeric then if(not tonumber(F))and F:len()>
0 then F=y.Value end end y.Value=F E.Text=F p:SafeCallback(y.Callback,y.Value)p:
SafeCallback(y.Changed,y.Value)end if y.Finished then E.FocusLost:Connect(
function(F)if not F then return end y:SetValue(E.Text)p:AttemptSave()end)else E:
GetPropertyChangedSignal'Text':Connect(function()y:SetValue(E.Text)p:
AttemptSave()end)end local F=function()local F,G=2,D.AbsoluteSize.X if not E:
IsFocused()or E.TextBounds.X<=G-2*F then E.Position=UDim2.new(0,F,0,0)else local
H=E.CursorPosition if H~=-1 then local I=string.sub(E.Text,1,H-1)local J=f:
GetTextSize(I,E.TextSize,E.Font,Vector2.new(math.huge,math.huge)).X local K=E.
Position.X.Offset+J if K<F then E.Position=UDim2.fromOffset(F-J,0)elseif K>G-F-1
then E.Position=UDim2.fromOffset(G-J-F-1,0)end end end end task.spawn(F)E:
GetPropertyChangedSignal'Text':Connect(F)E:GetPropertyChangedSignal
'CursorPosition':Connect(F)E.FocusLost:Connect(F)E.Focused:Connect(F)p:
AddToRegistry(E,{TextColor3='FontColor'})function y:OnChanged(G)y.Changed=G G(y.
Value)end z:AddBlank(5)z:Resize()p.Options[w]=y return y end function v:
AddToggle(w,x)assert(x.Text,'AddInput: Missing `Text` string.')local y,z={Value=
x.Default or false,Type='Toggle',Callback=x.Callback or function(y)end,Addons={}
,Risky=x.Risky},self local A=z.Container local B=p:Create('Frame',{
BackgroundColor3=Color3.new(0,0,0),BorderColor3=Color3.new(0,0,0),Size=UDim2.
new(0,13,0,13),ZIndex=5,Parent=A})p:AddToRegistry(B,{BorderColor3='Black'})local
C=p:Create('Frame',{BackgroundColor3=p.MainColor,BorderColor3=p.OutlineColor,
BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=6,Parent=B})p:
AddToRegistry(C,{BackgroundColor3='MainColor',BorderColor3='OutlineColor'})local
D=p:CreateLabel{Size=UDim2.new(0,216,1,0),Position=UDim2.new(1,6,0,0),TextSize=
14,Text=x.Text,TextXAlignment=Enum.TextXAlignment.Left,ZIndex=6,Parent=C}p:
Create('UIListLayout',{Padding=UDim.new(0,4),FillDirection=Enum.FillDirection.
Horizontal,HorizontalAlignment=Enum.HorizontalAlignment.Right,SortOrder=Enum.
SortOrder.LayoutOrder,Parent=D})local E=p:Create('Frame',{BackgroundTransparency
=1,Size=UDim2.new(0,170,1,0),ZIndex=8,Parent=B})p:OnHighlight(E,B,{BorderColor3=
'AccentColor'},{BorderColor3='Black'})function y:UpdateColors()y:Display()end if
type(x.Tooltip)=='string'then p:AddToolTip(x.Tooltip,E)end function y:Display()C
.BackgroundColor3=y.Value and p.AccentColor or p.MainColor C.BorderColor3=y.
Value and p.AccentColorDark or p.OutlineColor p.RegistryMap[C].Properties.
BackgroundColor3=y.Value and'AccentColor'or'MainColor'p.RegistryMap[C].
Properties.BorderColor3=y.Value and'AccentColorDark'or'OutlineColor'end function
y:OnChanged(F)y.Changed=F F(y.Value)end function y:SetValue(F)F=(not not F)y.
Value=F y:Display()for G,H in next,y.Addons do if H.Type=='KeyPicker'and H.
SyncToggleState then H.Toggled=F H:Update()end end p:SafeCallback(y.Callback,y.
Value)p:SafeCallback(y.Changed,y.Value)p:UpdateDependencyBoxes()end E.InputBegan
:Connect(function(F)if F.UserInputType==Enum.UserInputType.MouseButton1 and not
p:MouseIsOverOpenedFrame()then y:SetValue(not y.Value)p:AttemptSave()end end)if
y.Risky then p:RemoveFromRegistry(D)D.TextColor3=p.RiskColor p:AddToRegistry(D,{
TextColor3='RiskColor'})end y:Display()z:AddBlank(x.BlankSize or 7)z:Resize()y.
TextLabel=D y.Container=A setmetatable(y,u)p.Toggles[w]=y p:
UpdateDependencyBoxes()return y end function v:AddSlider(w,x)assert(x.Default,
'AddSlider: Missing default value.')assert(x.Text,
'AddSlider: Missing slider text.')assert(x.Min,
'AddSlider: Missing minimum value.')assert(x.Max,
'AddSlider: Missing maximum value.')assert(x.Rounding,
'AddSlider: Missing rounding value.')local y,z={Value=x.Default,Min=x.Min,Max=x.
Max,Rounding=x.Rounding,MaxSize=232,Type='Slider',Callback=x.Callback or
function(y)end},self local A=z.Container if not x.Compact then p:CreateLabel{
Size=UDim2.new(1,0,0,10),TextSize=14,Text=x.Text,TextXAlignment=Enum.
TextXAlignment.Left,TextYAlignment=Enum.TextYAlignment.Bottom,ZIndex=5,Parent=A}
z:AddBlank(3)end local B=p:Create('Frame',{BackgroundColor3=Color3.new(0,0,0),
BorderColor3=Color3.new(0,0,0),Size=UDim2.new(1,-4,0,13),ZIndex=5,Parent=A})p:
AddToRegistry(B,{BorderColor3='Black'})local C=p:Create('Frame',{
BackgroundColor3=p.MainColor,BorderColor3=p.OutlineColor,BorderMode=Enum.
BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=6,Parent=B})p:AddToRegistry(C,{
BackgroundColor3='MainColor',BorderColor3='OutlineColor'})local D=p:Create(
'Frame',{BackgroundColor3=p.AccentColor,BorderColor3=p.AccentColorDark,Size=
UDim2.new(0,0,1,0),ZIndex=7,Parent=C})p:AddToRegistry(D,{BackgroundColor3=
'AccentColor',BorderColor3='AccentColorDark'})local E=p:Create('Frame',{
BackgroundColor3=p.AccentColor,BorderSizePixel=0,Position=UDim2.new(1,0,0,0),
Size=UDim2.new(0,1,1,0),ZIndex=8,Parent=D})p:AddToRegistry(E,{BackgroundColor3=
'AccentColor'})local F=p:CreateLabel{Size=UDim2.new(1,0,1,0),TextSize=14,Text=
'Infinite',ZIndex=9,Parent=C}p:OnHighlight(B,B,{BorderColor3='AccentColor'},{
BorderColor3='Black'})if type(x.Tooltip)=='string'then p:AddToolTip(x.Tooltip,B)
end function y:UpdateColors()D.BackgroundColor3=p.AccentColor D.BorderColor3=p.
AccentColorDark end function y:Display()local G=x.Suffix or''if x.Compact then F
.Text=x.Text..': '..y.Value..G elseif x.HideMax then F.Text=string.format('%s',y
.Value..G)else F.Text=string.format('%s/%s',y.Value..G,y.Max..G)end local H=math
.ceil(p:MapValue(y.Value,y.Min,y.Max,0,y.MaxSize))D.Size=UDim2.new(0,H,1,0)E.
Visible=not(H==y.MaxSize or H==0)end function y:OnChanged(G)y.Changed=G G(y.
Value)end local G=function(G)if y.Rounding==0 then return math.floor(G)end
return tonumber(string.format('%.'..y.Rounding..'f',G))end function y:
GetValueFromXOffset(H)return G(p:MapValue(H,0,y.MaxSize,y.Min,y.Max))end
function y:SetValue(H)local I=tonumber(H)if(not I)then return end I=math.clamp(I
,y.Min,y.Max)y.Value=I y:Display()p:SafeCallback(y.Callback,y.Value)p:
SafeCallback(y.Changed,y.Value)end C.InputBegan:Connect(function(H)if H.
UserInputType==Enum.UserInputType.MouseButton1 and not p:MouseIsOverOpenedFrame(
)then local I,J=n.X,D.Size.X.Offset local K=I-(D.AbsolutePosition.X+J)while e:
IsMouseButtonPressed(Enum.UserInputType.MouseButton1)do local L=n.X local M=math
.clamp(J+(L-I)+K,0,y.MaxSize)local N,O=y:GetValueFromXOffset(M),y.Value y.Value=
N y:Display()if N~=O then p:SafeCallback(y.Callback,y.Value)p:SafeCallback(y.
Changed,y.Value)end l:Wait()end p:AttemptSave()end end)y:Display()z:AddBlank(x.
BlankSize or 6)z:Resize()p.Options[w]=y return y end function v:AddDropdown(w,x)
if x.SpecialType=='Player'then x.Values=s()x.AllowNull=true elseif x.SpecialType
=='Team'then x.Values=t()x.AllowNull=true end assert(x.Values,
'AddDropdown: Missing dropdown value list.')assert(x.AllowNull or x.Default,
[[AddDropdown: Missing default value. Pass `AllowNull` as true if this was intentional.]]
)if(not x.Text)then x.Compact=true end local y,z={Values=x.Values,Value=x.Multi
and{},Multi=x.Multi,Type='Dropdown',SpecialType=x.SpecialType,Callback=x.
Callback or function(y)end},self local A,B=z.Container,0 if not x.Compact then p
:CreateLabel{Size=UDim2.new(1,0,0,10),TextSize=14,Text=x.Text,TextXAlignment=
Enum.TextXAlignment.Left,TextYAlignment=Enum.TextYAlignment.Bottom,ZIndex=5,
Parent=A}z:AddBlank(3)end for C,D in next,A:GetChildren()do if not D:IsA
'UIListLayout'then B=B+D.Size.Y.Offset end end local E=p:Create('Frame',{
BackgroundColor3=Color3.new(0,0,0),BorderColor3=Color3.new(0,0,0),Size=UDim2.
new(1,-4,0,20),ZIndex=5,Parent=A})p:AddToRegistry(E,{BorderColor3='Black'})local
F=p:Create('Frame',{BackgroundColor3=p.MainColor,BorderColor3=p.OutlineColor,
BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=6,Parent=E})p:
AddToRegistry(F,{BackgroundColor3='MainColor',BorderColor3='OutlineColor'})p:
Create('UIGradient',{Color=ColorSequence.new{ColorSequenceKeypoint.new(0,Color3.
new(1,1,1)),ColorSequenceKeypoint.new(1,Color3.fromRGB(212,212,212))},Rotation=
90,Parent=F})local G,H=p:Create('ImageLabel',{AnchorPoint=Vector2.new(0,0.5),
BackgroundTransparency=1,Position=UDim2.new(1,-16,0.5,0),Size=UDim2.new(0,12,0,
12),Image='http://www.roblox.com/asset/?id=6282522798',ZIndex=8,Parent=F}),p:
CreateLabel{Position=UDim2.new(0,5,0,0),Size=UDim2.new(1,-5,1,0),TextSize=14,
Text='--',TextXAlignment=Enum.TextXAlignment.Left,TextWrapped=true,ZIndex=7,
Parent=F}p:OnHighlight(E,E,{BorderColor3='AccentColor'},{BorderColor3='Black'})
if type(x.Tooltip)=='string'then p:AddToolTip(x.Tooltip,E)end local I,J=8,p:
Create('Frame',{BackgroundColor3=Color3.new(0,0,0),BorderColor3=Color3.new(0,0,0
),ZIndex=20,Visible=false,Parent=o})local K,L=function()J.Position=UDim2.
fromOffset(E.AbsolutePosition.X,E.AbsolutePosition.Y+E.Size.Y.Offset+1)end,
function(K)J.Size=UDim2.fromOffset(E.AbsoluteSize.X,K or(I*20+2))end K()L()E:
GetPropertyChangedSignal'AbsolutePosition':Connect(K)local M=p:Create('Frame',{
BackgroundColor3=p.MainColor,BorderColor3=p.OutlineColor,BorderMode=Enum.
BorderMode.Inset,BorderSizePixel=0,Size=UDim2.new(1,0,1,0),ZIndex=21,Parent=J})p
:AddToRegistry(M,{BackgroundColor3='MainColor',BorderColor3='OutlineColor'})
local N=p:Create('ScrollingFrame',{BackgroundTransparency=1,BorderSizePixel=0,
CanvasSize=UDim2.new(0,0,0,0),Size=UDim2.new(1,0,1,0),ZIndex=21,Parent=M,
TopImage='rbxasset://textures/ui/Scroll/scroll-middle.png',BottomImage=
'rbxasset://textures/ui/Scroll/scroll-middle.png',ScrollBarThickness=3,
ScrollBarImageColor3=p.AccentColor})p:AddToRegistry(N,{ScrollBarImageColor3=
'AccentColor'})p:Create('UIListLayout',{Padding=UDim.new(0,0),FillDirection=Enum
.FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,Parent=N})function
y:Display()local O,P=y.Values,''if x.Multi then for Q,R in next,O do if y.Value[
R]then P=P..R..', 'end end P=P:sub(1,#P-2)else P=y.Value or''end H.Text=(P==''
and'--'or P)end function y:GetActiveValues()if x.Multi then local O={}for P,Q in
next,y.Value do table.insert(O,P)end return O else return y.Value and 1 or 0 end
end function y:BuildDropdownList()local O,P=y.Values,{}for Q,R in next,N:
GetChildren()do if not R:IsA'UIListLayout'then R:Destroy()end end local S=0 for
T,U in next,O do local V={}S=S+1 local W=p:Create('Frame',{BackgroundColor3=p.
MainColor,BorderColor3=p.OutlineColor,BorderMode=Enum.BorderMode.Middle,Size=
UDim2.new(1,-1,0,20),ZIndex=23,Active=true,Parent=N})p:AddToRegistry(W,{
BackgroundColor3='MainColor',BorderColor3='OutlineColor'})local X=p:CreateLabel{
Active=false,Size=UDim2.new(1,-6,1,0),Position=UDim2.new(0,6,0,0),TextSize=14,
Text=U,TextXAlignment=Enum.TextXAlignment.Left,ZIndex=25,Parent=W}p:OnHighlight(
W,W,{BorderColor3='AccentColor',ZIndex=24},{BorderColor3='OutlineColor',ZIndex=
23})local Y if x.Multi then Y=y.Value[U]else Y=y.Value==U end function V:
UpdateButton()if x.Multi then Y=y.Value[U]else Y=y.Value==U end X.TextColor3=Y
and p.AccentColor or p.FontColor p.RegistryMap[X].Properties.TextColor3=Y and
'AccentColor'or'FontColor'end X.InputBegan:Connect(function(Z)if Z.UserInputType
==Enum.UserInputType.MouseButton1 then local _=not Y if y:GetActiveValues()==1
and(not _)and(not x.AllowNull)then else if x.Multi then Y=_ if Y then y.Value[U]
=true else y.Value[U]=nil end else Y=_ if Y then y.Value=U else y.Value=nil end
for ab,ac in next,P do ac:UpdateButton()end end V:UpdateButton()y:Display()p:
SafeCallback(y.Callback,y.Value)p:SafeCallback(y.Changed,y.Value)p:AttemptSave()
end end end)V:UpdateButton()y:Display()P[W]=V end N.CanvasSize=UDim2.fromOffset(
0,(S*20)+1)local ab=math.clamp(S*20,0,I*20)+1 L(ab)end function y:SetValues(ab)
if ab then y.Values=ab end y:BuildDropdownList()end function y:OpenDropdown()J.
Visible=true p.OpenedFrames[J]=true G.Rotation=180 end function y:CloseDropdown(
)J.Visible=false p.OpenedFrames[J]=nil G.Rotation=0 end function y:OnChanged(ab)
y.Changed=ab ab(y.Value)end function y:SetValue(ab)if y.Multi then local ac={}
for O,P in next,ab do if table.find(y.Values,O)then ac[O]=true end end y.Value=
ac else if(not ab)then y.Value=nil elseif table.find(y.Values,ab)then y.Value=ab
end end y:BuildDropdownList()p:SafeCallback(y.Callback,y.Value)p:SafeCallback(y.
Changed,y.Value)end E.InputBegan:Connect(function(ab)if ab.UserInputType==Enum.
UserInputType.MouseButton1 and not p:MouseIsOverOpenedFrame()then if J.Visible
then y:CloseDropdown()else y:OpenDropdown()end end end)e.InputBegan:Connect(
function(ab)if ab.UserInputType==Enum.UserInputType.MouseButton1 then local ac,O
=J.AbsolutePosition,J.AbsoluteSize if n.X<ac.X or n.X>ac.X+O.X or n.Y<(ac.Y-20-1
)or n.Y>ac.Y+O.Y then y:CloseDropdown()end end end)y:BuildDropdownList()y:
Display()local ab={}if type(x.Default)=='string'then local ac=table.find(y.
Values,x.Default)if ac then table.insert(ab,ac)end elseif type(x.Default)==
'table'then for ac,O in next,x.Default do local P=table.find(y.Values,O)if P
then table.insert(ab,P)end end elseif type(x.Default)=='number'and y.Values[x.
Default]~=nil then table.insert(ab,x.Default)end if next(ab)then for ac=1,#ab do
local O=ab[ac]if x.Multi then y.Value[y.Values[O] ]=true else y.Value=y.Values[O
]end if(not x.Multi)then break end end y:BuildDropdownList()y:Display()end z:
AddBlank(x.BlankSize or 5)z:Resize()p.Options[w]=y return y end function v:
AddDependencyBox()local ab,ac={Dependencies={}},self local w=ac.Container local
x=p:Create('Frame',{BackgroundTransparency=1,Size=UDim2.new(1,0,0,0),Visible=
false,Parent=w})local y=p:Create('Frame',{BackgroundTransparency=1,Size=UDim2.
new(1,0,1,0),Visible=true,Parent=x})local z=p:Create('UIListLayout',{
FillDirection=Enum.FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,
Parent=y})function ab:Resize()x.Size=UDim2.new(1,0,0,z.AbsoluteContentSize.Y)ac:
Resize()end z:GetPropertyChangedSignal'AbsoluteContentSize':Connect(function()ab
:Resize()end)x:GetPropertyChangedSignal'Visible':Connect(function()ab:Resize()
end)function ab:Update()for A,B in next,ab.Dependencies do local C,D=B[1],B[2]if
C.Type=='Toggle'and C.Value~=D then x.Visible=false ab:Resize()return end end x.
Visible=true ab:Resize()end function ab:SetupDependencies(A)for B,C in next,A do
assert(type(C)=='table','SetupDependencies: Dependency is not of type `table`.')
assert(C[1],'SetupDependencies: Dependency is missing element argument.')assert(
C[2]~=nil,'SetupDependencies: Dependency is missing value argument.')end ab.
Dependencies=A ab:Update()end ab.Container=y setmetatable(ab,aa)table.insert(p.
DependencyBoxes,ab)return ab end aa.__index=v aa.__namecall=function(ab,ac,...)
return v[ac](...)end end do p.NotificationArea=p:Create('Frame',{
BackgroundTransparency=1,Position=UDim2.new(0,0,0,40),Size=UDim2.new(0,300,0,200
),ZIndex=100,Parent=o})p:Create('UIListLayout',{Padding=UDim.new(0,4),
FillDirection=Enum.FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,
Parent=p.NotificationArea})local ab=p:Create('Frame',{BorderColor3=Color3.new(0,
0,0),Position=UDim2.new(0,100,0,-25),Size=UDim2.new(0,213,0,20),ZIndex=200,
Visible=false,Parent=o})local ac=p:Create('Frame',{BackgroundColor3=p.MainColor,
BorderColor3=p.AccentColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1
,0),ZIndex=201,Parent=ab})p:AddToRegistry(ac,{BorderColor3='AccentColor'})local
v=p:Create('Frame',{BackgroundColor3=Color3.new(1,1,1),BorderSizePixel=0,
Position=UDim2.new(0,1,0,1),Size=UDim2.new(1,-2,1,-2),ZIndex=202,Parent=ac})
local w=p:Create('UIGradient',{Color=ColorSequence.new{ColorSequenceKeypoint.
new(0,p:GetDarkerColor(p.MainColor)),ColorSequenceKeypoint.new(1,p.MainColor)},
Rotation=-90,Parent=v})p:AddToRegistry(w,{Color=function()return ColorSequence.
new{ColorSequenceKeypoint.new(0,p:GetDarkerColor(p.MainColor)),
ColorSequenceKeypoint.new(1,p.MainColor)}end})local x=p:CreateLabel{Position=
UDim2.new(0,5,0,0),Size=UDim2.new(1,-4,1,0),TextSize=14,TextXAlignment=Enum.
TextXAlignment.Left,ZIndex=203,Parent=v}p.Watermark=ab p.WatermarkText=x p:
MakeDraggable(p.Watermark)local y=p:Create('Frame',{AnchorPoint=Vector2.new(0,
0.5),BorderColor3=Color3.new(0,0,0),Position=UDim2.new(0,10,0.5,0),Size=UDim2.
new(0,210,0,20),Visible=false,ZIndex=100,Parent=o})local z=p:Create('Frame',{
BackgroundColor3=p.MainColor,BorderColor3=p.OutlineColor,BorderMode=Enum.
BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=101,Parent=y})p:AddToRegistry(z,
{BackgroundColor3='MainColor',BorderColor3='OutlineColor'},true)local A=p:
Create('Frame',{BackgroundColor3=p.AccentColor,BorderSizePixel=0,Size=UDim2.new(
1,0,0,2),ZIndex=102,Parent=z})p:AddToRegistry(A,{BackgroundColor3='AccentColor'}
,true)p:CreateLabel{Size=UDim2.new(1,0,0,20),Position=UDim2.fromOffset(5,2),
TextXAlignment=Enum.TextXAlignment.Left,Text='Keybinds',ZIndex=104,Parent=z}
local B=p:Create('Frame',{BackgroundTransparency=1,Size=UDim2.new(1,0,1,-20),
Position=UDim2.new(0,0,0,20),ZIndex=1,Parent=z})p:Create('UIListLayout',{
FillDirection=Enum.FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,
Parent=B})p:Create('UIPadding',{PaddingLeft=UDim.new(0,5),Parent=B})p.
KeybindFrame=y p.KeybindContainer=B p:MakeDraggable(y)end function p:
SetWatermarkVisibility(ab)p.Watermark.Visible=ab end function p:SetWatermark(ab)
local ac,v=p:GetTextBounds(ab,p.Font,14)p.Watermark.Size=UDim2.new(0,ac+15,0,(v*
1.5)+3)p:SetWatermarkVisibility(true)p.WatermarkText.Text=ab end function p:
Notify(ab,ac)local v,w=p:GetTextBounds(ab,p.Font,14)w=w+7 local x=p:Create(
'Frame',{BorderColor3=Color3.new(0,0,0),Position=UDim2.new(0,100,0,10),Size=
UDim2.new(0,0,0,w),ClipsDescendants=true,ZIndex=100,Parent=p.NotificationArea})
local y=p:Create('Frame',{BackgroundColor3=p.MainColor,BorderColor3=p.
OutlineColor,BorderMode=Enum.BorderMode.Inset,Size=UDim2.new(1,0,1,0),ZIndex=101
,Parent=x})p:AddToRegistry(y,{BackgroundColor3='MainColor',BorderColor3=
'OutlineColor'},true)local z=p:Create('Frame',{BackgroundColor3=Color3.new(1,1,1
),BorderSizePixel=0,Position=UDim2.new(0,1,0,1),Size=UDim2.new(1,-2,1,-2),ZIndex
=102,Parent=y})local A=p:Create('UIGradient',{Color=ColorSequence.new{
ColorSequenceKeypoint.new(0,p:GetDarkerColor(p.MainColor)),ColorSequenceKeypoint
.new(1,p.MainColor)},Rotation=-90,Parent=z})p:AddToRegistry(A,{Color=function()
return ColorSequence.new{ColorSequenceKeypoint.new(0,p:GetDarkerColor(p.
MainColor)),ColorSequenceKeypoint.new(1,p.MainColor)}end})p:CreateLabel{Position
=UDim2.new(0,4,0,0),Size=UDim2.new(1,-4,1,0),Text=ab,TextXAlignment=Enum.
TextXAlignment.Left,TextSize=14,ZIndex=103,Parent=z}local B=p:Create('Frame',{
BackgroundColor3=p.AccentColor,BorderSizePixel=0,Position=UDim2.new(0,-1,0,-1),
Size=UDim2.new(0,3,1,2),ZIndex=104,Parent=x})p:AddToRegistry(B,{BackgroundColor3
='AccentColor'},true)pcall(x.TweenSize,x,UDim2.new(0,v+8+4,0,w),'Out','Quad',0.4
,true)task.spawn(function()wait(ac or 5)pcall(x.TweenSize,x,UDim2.new(0,0,0,w),
'Out','Quad',0.4,true)wait(0.4)x:Destroy()end)end function p:CreateWindow(...)
local ab,ac={...},{AnchorPoint=Vector2.zero}if type(...)=='table'then ac=...else
ac.Title=ab[1]ac.AutoShow=ab[2]or false end if type(ac.Title)~='string'then ac.
Title='No title'end if type(ac.TabPadding)~='number'then ac.TabPadding=0 end if
type(ac.MenuFadeTime)~='number'then ac.MenuFadeTime=0.2 end if typeof(ac.
Position)~='UDim2'then ac.Position=UDim2.fromOffset(175,50)end if typeof(ac.Size
)~='UDim2'then ac.Size=UDim2.fromOffset(550,600)end if ac.Center then ac.
AnchorPoint=Vector2.new(0.5,0.5)ac.Position=UDim2.fromScale(0.5,0.5)end local v,
w={Tabs={}},p:Create('Frame',{AnchorPoint=ac.AnchorPoint,BackgroundColor3=Color3
.new(0,0,0),BorderSizePixel=0,Position=ac.Position,Size=ac.Size,Visible=false,
ZIndex=1,Parent=o})p:MakeDraggable(w,25)local x=p:Create('Frame',{
BackgroundColor3=p.MainColor,BorderColor3=p.AccentColor,BorderMode=Enum.
BorderMode.Inset,Position=UDim2.new(0,1,0,1),Size=UDim2.new(1,-2,1,-2),ZIndex=1,
Parent=w})p:AddToRegistry(x,{BackgroundColor3='MainColor',BorderColor3=
'AccentColor'})local y,z=p:CreateLabel{Position=UDim2.new(0,7,0,0),Size=UDim2.
new(0,0,0,25),Text=ac.Title or'',TextXAlignment=Enum.TextXAlignment.Left,ZIndex=
1,Parent=x},p:Create('Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=p.
OutlineColor,Position=UDim2.new(0,8,0,25),Size=UDim2.new(1,-16,1,-33),ZIndex=1,
Parent=x})p:AddToRegistry(z,{BackgroundColor3='BackgroundColor',BorderColor3=
'OutlineColor'})local A=p:Create('Frame',{BackgroundColor3=p.BackgroundColor,
BorderColor3=Color3.new(0,0,0),BorderMode=Enum.BorderMode.Inset,Position=UDim2.
new(0,0,0,0),Size=UDim2.new(1,0,1,0),ZIndex=1,Parent=z})p:AddToRegistry(A,{
BackgroundColor3='BackgroundColor'})local B=p:Create('Frame',{
BackgroundTransparency=1,Position=UDim2.new(0,8,0,8),Size=UDim2.new(1,-16,0,21),
ZIndex=1,Parent=A})local C,D=p:Create('UIListLayout',{Padding=UDim.new(0,ac.
TabPadding),FillDirection=Enum.FillDirection.Horizontal,SortOrder=Enum.SortOrder
.LayoutOrder,Parent=B}),p:Create('Frame',{BackgroundColor3=p.MainColor,
BorderColor3=p.OutlineColor,Position=UDim2.new(0,8,0,30),Size=UDim2.new(1,-16,1,
-38),ZIndex=2,Parent=A})p:AddToRegistry(D,{BackgroundColor3='MainColor',
BorderColor3='OutlineColor'})function v:SetWindowTitle(E)y.Text=E end function v
:AddTab(E)local F,G={Groupboxes={},Tabboxes={}},p:GetTextBounds(E,p.Font,16)
local H=p:Create('Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=p.
OutlineColor,Size=UDim2.new(0,G+8+4,1,0),ZIndex=1,Parent=B})p:AddToRegistry(H,{
BackgroundColor3='BackgroundColor',BorderColor3='OutlineColor'})p:CreateLabel{
Position=UDim2.new(0,0,0,0),Size=UDim2.new(1,0,1,-1),Text=E,ZIndex=1,Parent=H}
local I=p:Create('Frame',{BackgroundColor3=p.MainColor,BorderSizePixel=0,
Position=UDim2.new(0,0,1,0),Size=UDim2.new(1,0,0,1),BackgroundTransparency=1,
ZIndex=3,Parent=H})p:AddToRegistry(I,{BackgroundColor3='MainColor'})local J=p:
Create('Frame',{Name='TabFrame',BackgroundTransparency=1,Position=UDim2.new(0,0,
0,0),Size=UDim2.new(1,0,1,0),Visible=false,ZIndex=2,Parent=D})local K,L=p:
Create('ScrollingFrame',{BackgroundTransparency=1,BorderSizePixel=0,Position=
UDim2.new(0,7,0,7),Size=UDim2.new(0.5,-10,0,509),CanvasSize=UDim2.new(0,0,0,0),
BottomImage='',TopImage='',ScrollBarThickness=0,ZIndex=2,Parent=J}),p:Create(
'ScrollingFrame',{BackgroundTransparency=1,BorderSizePixel=0,Position=UDim2.new(
0.5,5,0,7),Size=UDim2.new(0.5,-10,0,509),CanvasSize=UDim2.new(0,0,0,0),
BottomImage='',TopImage='',ScrollBarThickness=0,ZIndex=2,Parent=J})p:Create(
'UIListLayout',{Padding=UDim.new(0,8),FillDirection=Enum.FillDirection.Vertical,
SortOrder=Enum.SortOrder.LayoutOrder,HorizontalAlignment=Enum.
HorizontalAlignment.Center,Parent=K})p:Create('UIListLayout',{Padding=UDim.new(0
,8),FillDirection=Enum.FillDirection.Vertical,SortOrder=Enum.SortOrder.
LayoutOrder,HorizontalAlignment=Enum.HorizontalAlignment.Center,Parent=L})for M,
N in next,{K,L}do N:WaitForChild'UIListLayout':GetPropertyChangedSignal
'AbsoluteContentSize':Connect(function()N.CanvasSize=UDim2.fromOffset(0,N.
UIListLayout.AbsoluteContentSize.Y)end)end function F:ShowTab()for O,P in next,v
.Tabs do P:HideTab()end I.BackgroundTransparency=0 H.BackgroundColor3=p.
MainColor p.RegistryMap[H].Properties.BackgroundColor3='MainColor'J.Visible=true
end function F:HideTab()I.BackgroundTransparency=1 H.BackgroundColor3=p.
BackgroundColor p.RegistryMap[H].Properties.BackgroundColor3='BackgroundColor'J.
Visible=false end function F:SetLayoutOrder(O)H.LayoutOrder=O C:ApplyLayout()end
function F:AddGroupbox(O)local P,Q={},p:Create('Frame',{BackgroundColor3=p.
BackgroundColor,BorderColor3=p.OutlineColor,BorderMode=Enum.BorderMode.Inset,
Size=UDim2.new(1,0,0,509),ZIndex=2,Parent=O.Side==1 and K or L})p:AddToRegistry(
Q,{BackgroundColor3='BackgroundColor',BorderColor3='OutlineColor'})local R=p:
Create('Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=Color3.new(0,0,0
),Size=UDim2.new(1,-2,1,-2),Position=UDim2.new(0,1,0,1),ZIndex=4,Parent=Q})p:
AddToRegistry(R,{BackgroundColor3='BackgroundColor'})local S=p:Create('Frame',{
BackgroundColor3=p.AccentColor,BorderSizePixel=0,Size=UDim2.new(1,0,0,2),ZIndex=
5,Parent=R})p:AddToRegistry(S,{BackgroundColor3='AccentColor'})p:CreateLabel{
Size=UDim2.new(1,0,0,18),Position=UDim2.new(0,4,0,2),TextSize=14,Text=O.Name,
TextXAlignment=Enum.TextXAlignment.Left,ZIndex=5,Parent=R}local T=p:Create(
'Frame',{BackgroundTransparency=1,Position=UDim2.new(0,4,0,20),Size=UDim2.new(1,
-4,1,-20),ZIndex=1,Parent=R})p:Create('UIListLayout',{FillDirection=Enum.
FillDirection.Vertical,SortOrder=Enum.SortOrder.LayoutOrder,Parent=T})function P
:Resize()local U=0 for V,W in next,P.Container:GetChildren()do if(not W:IsA
'UIListLayout')and W.Visible then U=U+W.Size.Y.Offset end end Q.Size=UDim2.new(1
,0,0,20+U+2+2)end P.Container=T setmetatable(P,aa)P:AddBlank(3)P:Resize()F.
Groupboxes[O.Name]=P return P end function F:AddLeftGroupbox(O)return F:
AddGroupbox{Side=1,Name=O}end function F:AddRightGroupbox(O)return F:AddGroupbox
{Side=2,Name=O}end function F:AddTabbox(O)local P,Q={Tabs={}},p:Create('Frame',{
BackgroundColor3=p.BackgroundColor,BorderColor3=p.OutlineColor,BorderMode=Enum.
BorderMode.Inset,Size=UDim2.new(1,0,0,0),ZIndex=2,Parent=O.Side==1 and K or L})p
:AddToRegistry(Q,{BackgroundColor3='BackgroundColor',BorderColor3='OutlineColor'
})local R=p:Create('Frame',{BackgroundColor3=p.BackgroundColor,BorderColor3=
Color3.new(0,0,0),Size=UDim2.new(1,-2,1,-2),Position=UDim2.new(0,1,0,1),ZIndex=4
,Parent=Q})p:AddToRegistry(R,{BackgroundColor3='BackgroundColor'})local S=p:
Create('Frame',{BackgroundColor3=p.AccentColor,BorderSizePixel=0,Size=UDim2.new(
1,0,0,2),ZIndex=10,Parent=R})p:AddToRegistry(S,{BackgroundColor3='AccentColor'})
local T=p:Create('Frame',{BackgroundTransparency=1,Position=UDim2.new(0,0,0,1),
Size=UDim2.new(1,0,0,18),ZIndex=5,Parent=R})p:Create('UIListLayout',{
FillDirection=Enum.FillDirection.Horizontal,HorizontalAlignment=Enum.
HorizontalAlignment.Left,SortOrder=Enum.SortOrder.LayoutOrder,Parent=T})function
P:AddTab(U)local V,W={},p:Create('Frame',{BackgroundColor3=p.MainColor,
BorderColor3=Color3.new(0,0,0),Size=UDim2.new(0.5,0,1,0),ZIndex=6,Parent=T})p:
AddToRegistry(W,{BackgroundColor3='MainColor'})p:CreateLabel{Size=UDim2.new(1,0,
1,0),TextSize=14,Text=U,TextXAlignment=Enum.TextXAlignment.Center,ZIndex=7,
Parent=W}local X=p:Create('Frame',{BackgroundColor3=p.BackgroundColor,
BorderSizePixel=0,Position=UDim2.new(0,0,1,0),Size=UDim2.new(1,0,0,1),Visible=
false,ZIndex=9,Parent=W})p:AddToRegistry(X,{BackgroundColor3='BackgroundColor'})
local Y=p:Create('Frame',{BackgroundTransparency=1,Position=UDim2.new(0,4,0,20),
Size=UDim2.new(1,-4,1,-20),ZIndex=1,Visible=false,Parent=R})p:Create(
'UIListLayout',{FillDirection=Enum.FillDirection.Vertical,SortOrder=Enum.
SortOrder.LayoutOrder,Parent=Y})function V:Show()for Z,_ in next,P.Tabs do _:
Hide()end Y.Visible=true X.Visible=true W.BackgroundColor3=p.BackgroundColor p.
RegistryMap[W].Properties.BackgroundColor3='BackgroundColor'_:Resize()end
function V:Hide()Y.Visible=false X.Visible=false W.BackgroundColor3=p.MainColor
p.RegistryMap[W].Properties.BackgroundColor3='MainColor'end function V:Resize()
local Z=0 for _,ad in next,P.Tabs do Z=Z+1 end for ae,af in next,T:GetChildren()
do if not af:IsA'UIListLayout'then af.Size=UDim2.new(1/Z,0,1,0)end end if(not Y.
Visible)then return end local ag=0 for ah,ai in next,ad.Container:GetChildren()
do if(not ai:IsA'UIListLayout')and ai.Visible then ag=ag+ai.Size.Y.Offset end
end Q.Size=UDim2.new(1,0,0,20+ag+2+2)end W.InputBegan:Connect(function(ad)if ad.
UserInputType==Enum.UserInputType.MouseButton1 and not p:MouseIsOverOpenedFrame(
)then V:Show()V:Resize()end end)V.Container=Y P.Tabs[U]=V setmetatable(V,aa)V:
AddBlank(3)V:Resize()if#T:GetChildren()==2 then V:Show()end return V end F.
Tabboxes[O.Name or'']=P return P end function F:AddLeftTabbox(ad)return F:
AddTabbox{Name=ad,Side=1}end function F:AddRightTabbox(ad)return F:AddTabbox{
Name=ad,Side=2}end H.InputBegan:Connect(function(ad)if ad.UserInputType==Enum.
UserInputType.MouseButton1 then F:ShowTab()end end)if#D:GetChildren()==1 then F:
ShowTab()end v.Tabs[E]=F return F end local ad,af,ag,ah=p:Create('TextButton',{
BackgroundTransparency=1,Size=UDim2.new(0,0,0,0),Visible=true,Text='',Modal=
false,Parent=o}),{},false,false function p:Toggle()if ah then return end local
ai=ac.MenuFadeTime ah=true ag=(not ag)ad.Modal=ag if ag then w.Visible=true task
.spawn(function()local E,F=e.MouseIconEnabled,Drawing.new'Triangle'F.Thickness=1
F.Filled=true F.Visible=true local G=Drawing.new'Triangle'G.Thickness=1 G.Filled
=false G.Color=Color3.new(0,0,0)G.Visible=true while ag and o.Parent do e.
MouseIconEnabled=false local H=e:GetMouseLocation()F.Color=p.AccentColor F.
PointA=Vector2.new(H.X,H.Y)F.PointB=Vector2.new(H.X+16,H.Y+6)F.PointC=Vector2.
new(H.X+6,H.Y+16)G.PointA=F.PointA G.PointB=F.PointB G.PointC=F.PointC l:Wait()
end e.MouseIconEnabled=E F:Remove()G:Remove()end)end for E,F in next,w:
GetDescendants()do local G={}if F:IsA'ImageLabel'then table.insert(G,
'ImageTransparency')table.insert(G,'BackgroundTransparency')elseif F:IsA
'TextLabel'or F:IsA'TextBox'then table.insert(G,'TextTransparency')elseif F:IsA
'Frame'or F:IsA'ScrollingFrame'then table.insert(G,'BackgroundTransparency')
elseif F:IsA'UIStroke'then table.insert(G,'Transparency')end local H=af[F]if(not
H)then H={}af[F]=H end for I,J in next,G do if not H[J]then H[J]=F[J]end if H[J]
==1 then continue end k:Create(F,TweenInfo.new(ai,Enum.EasingStyle.Linear),{[J]=
ag and H[J]or 1}):Play()end end task.wait(ai)w.Visible=ag ah=false end p:
GiveSignal(e.InputBegan:Connect(function(ai,E)if type(p.ToggleKeybind)=='table'
and p.ToggleKeybind.Type=='KeyPicker'then if ai.UserInputType==Enum.
UserInputType.Keyboard and ai.KeyCode.Name==p.ToggleKeybind.Value then task.
spawn(p.Toggle)end elseif ai.KeyCode==Enum.KeyCode.RightControl or(ai.KeyCode==
Enum.KeyCode.RightShift and(not E))then task.spawn(p.Toggle)end end))if ac.
AutoShow then task.spawn(p.Toggle)end v.Holder=w return v end local ab=function(
)local ab=s()for ac,ad in next,p.Options do if ad.Type=='Dropdown'and ad.
SpecialType=='Player'then ad:SetValues(ab)end end end i.PlayerAdded:Connect(ab)i
.PlayerRemoving:Connect(ab)return p end function a.c()local aa=a.load'a'local ab
=aa.SecureService local ac,ad=ab'HttpService',{}do ad.Folder=
'LinoriaLibSettings'ad.Ignore={}ad.Parser={Toggle={Save=function(af,ag)return{
type='Toggle',idx=af,value=ag.Value}end,Load=function(af,ag)if ad.Library.
Toggles[af]then ad.Library.Toggles[af]:SetValue(ag.value)end end},Slider={Save=
function(af,ag)return{type='Slider',idx=af,value=tostring(ag.Value)}end,Load=
function(af,ag)if ad.Library.Options[af]then ad.Library.Options[af]:SetValue(ag.
value)end end},Dropdown={Save=function(af,ag)return{type='Dropdown',idx=af,value
=ag.Value,mutli=ag.Multi}end,Load=function(af,ag)if ad.Library.Options[af]then
ad.Library.Options[af]:SetValue(ag.value)end end},ColorPicker={Save=function(af,
ag)return{type='ColorPicker',idx=af,value=ag.Value:ToHex(),transparency=ag.
Transparency}end,Load=function(af,ag)if ad.Library.Options[af]then ad.Library.
Options[af]:SetValueRGB(Color3.fromHex(ag.value),ag.transparency)end end},
KeyPicker={Save=function(af,ag)return{type='KeyPicker',idx=af,mode=ag.Mode,key=
ag.Value}end,Load=function(af,ag)if ad.Library.Options[af]then ad.Library.
Options[af]:SetValue{ag.key,ag.mode}end end},Input={Save=function(af,ag)return{
type='Input',idx=af,text=ag.Value}end,Load=function(af,ag)if ad.Library.Options[
af]and type(ag.text)=='string'then ad.Library.Options[af]:SetValue(ag.text)end
end}}function ad:SetIgnoreIndexes(af)for ag,ah in next,af do self.Ignore[ah]=
true end end function ad:SetFolder(af)self.Folder=af self:BuildFolderTree()end
function ad:Save(af)if(not af)then return false,'no config file is selected'end
local ag,ah=self.Folder..'/settings/'..af..'.json',{objects={}}for ai,b in next,
ad.Library.Toggles do if self.Ignore[ai]then continue end table.insert(ah.
objects,self.Parser[b.Type].Save(ai,b))end for c,d in next,ad.Library.Options do
if not self.Parser[d.Type]then continue end if self.Ignore[c]then continue end
table.insert(ah.objects,self.Parser[d.Type].Save(c,d))end local e,f=pcall(ac.
JSONEncode,ac,ah)if not e then return false,'failed to encode data'end
writefile(ag,f)return true end function ad:Load(af)if(not af)then return false,
'no config file is selected'end local ag=self.Folder..'/settings/'..af..'.json'
if not isfile(ag)then return false,'invalid file'end local ah,b=pcall(ac.
JSONDecode,ac,readfile(ag))if not ah then return false,'decode error'end for c,d
in next,b.objects do if self.Parser[d.type]then task.spawn(function()self.Parser
[d.type].Load(d.idx,d)end)end end return true end function ad:
IgnoreThemeSettings()self:SetIgnoreIndexes{'BackgroundColor','MainColor',
'AccentColor','OutlineColor','FontColor','ThemeManager_ThemeList',
'ThemeManager_CustomThemeList','ThemeManager_CustomThemeName'}end function ad:
BuildFolderTree()local af={self.Folder,self.Folder..'/themes',self.Folder..
'/settings'}for ag=1,#af do local ah=af[ag]if not isfolder(ah)then makefolder(ah
)end end end function ad:RefreshConfigList()local af,ag=listfiles(self.Folder..
'/settings'),{}for ah=1,#af do local b=af[ah]if b:sub(-5)=='.json'then local c=b
:find('.json',1,true)local d,e=c,b:sub(c,c)while e~='/'and e~='\\'and e~=''do c=
c-1 e=b:sub(c,c)end if e=='/'or e=='\\'then table.insert(ag,b:sub(c+1,d-1))end
end end return ag end function ad:SetLibrary(af)self.Library=af end function ad:
LoadAutoloadConfig()if isfile(self.Folder..'/settings/autoload.txt')then local
af=readfile(self.Folder..'/settings/autoload.txt')local ag,ah=self:Load(af)if
not ag then return self.Library:Notify('Failed to load autoload config: '..ah)
end self.Library:Notify(string.format('Auto loaded config %q',af))end return nil
end function ad:BuildConfigSection(af)assert(self.Library,
'Must set SaveManager.Library')local ag=af:AddRightGroupbox'Configuration'ag:
AddInput('SaveManager_ConfigName',{Text='Config name'})ag:AddDropdown(
'SaveManager_ConfigList',{Text='Config list',Values=self:RefreshConfigList(),
AllowNull=true})ag:AddDivider()ag:AddButton('Create config',function()local ah=
ad.Library.Options.SaveManager_ConfigName.Value if ah:gsub(' ','')==''then
return self.Library:Notify('Invalid config name (empty)',2)end local b,c=self:
Save(ah)if not b then return self.Library:Notify('Failed to save config: '..c)
end self.Library:Notify(string.format('Created config %q',ah))ad.Library.Options
.SaveManager_ConfigList:SetValues(self:RefreshConfigList())ad.Library.Options.
SaveManager_ConfigList:SetValue(nil)return nil end):AddButton('Load config',
function()local ah=ad.Library.Options.SaveManager_ConfigList.Value local b,c=
self:Load(ah)if not b then return self.Library:Notify('Failed to load config: '
..c)end self.Library:Notify(string.format('Loaded config %q',ah))return nil end)
ag:AddButton('Overwrite config',function()local ah=ad.Library.Options.
SaveManager_ConfigList.Value local b,c=self:Save(ah)if not b then return self.
Library:Notify('Failed to overwrite config: '..c)end self.Library:Notify(string.
format('Overwrote config %q',ah))return nil end)ag:AddButton('Refresh list',
function()ad.Library.Options.SaveManager_ConfigList:SetValues(self:
RefreshConfigList())ad.Library.Options.SaveManager_ConfigList:SetValue(nil)end)
ag:AddButton('Set as autoload',function()local ah=ad.Library.Options.
SaveManager_ConfigList.Value writefile(self.Folder..'/settings/autoload.txt',ah)
ad.AutoloadLabel:SetText('Current autoload config: '..ah)self.Library:Notify(
string.format('Set %q to auto load',ah))end)ad.AutoloadLabel=ag:AddLabel(
'Current autoload config: none',true)if isfile(self.Folder..
'/settings/autoload.txt')then local ah=readfile(self.Folder..
'/settings/autoload.txt')ad.AutoloadLabel:SetText('Current autoload config: '..
ah)end ad:SetIgnoreIndexes{'SaveManager_ConfigList','SaveManager_ConfigName'}end
ad:BuildFolderTree()end return ad end function a.d()local aa=a.load'a'local ab=
aa.SecureService local ac,ad=ab'HttpService',{}do ad.Folder='LinoriaLibSettings'
ad.Library=nil ad.BuiltInThemes={Default={1,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"1c1c1c","AccentColor":"0055ff","BackgroundColor":"141414","OutlineColor":"323232"}]]
},BBot={2,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"1e1e1e","AccentColor":"7e48a3","BackgroundColor":"232323","OutlineColor":"141414"}]]
},Fatality={3,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"1e1842","AccentColor":"c50754","BackgroundColor":"191335","OutlineColor":"3c355d"}]]
},Jester={4,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"242424","AccentColor":"db4467","BackgroundColor":"1c1c1c","OutlineColor":"373737"}]]
},Mint={5,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"242424","AccentColor":"3db488","BackgroundColor":"1c1c1c","OutlineColor":"373737"}]]
},['Tokyo Night']={6,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"191925","AccentColor":"6759b3","BackgroundColor":"16161f","OutlineColor":"323232"}]]
},Ubuntu={7,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"3e3e3e","AccentColor":"e2581e","BackgroundColor":"323232","OutlineColor":"191919"}]]
},Quartz={8,ac:JSONDecode
[[{"FontColor":"ffffff","MainColor":"232330","AccentColor":"426e87","BackgroundColor":"1d1b26","OutlineColor":"27232f"}]]
}}function ad:ApplyTheme(af)local ag=self:GetCustomTheme(af)local ah=ag or self.
BuiltInThemes[af]if not ah then return end local b=ah[2]for c,d in next,ag or b
do self.Library[c]=Color3.fromHex(d)if ad.Library and ad.Library.Options[c]then
ad.Library.Options.Library.Options[c]:SetValueRGB(Color3.fromHex(d))end end self
:ThemeUpdate()end function ad:ThemeUpdate()local af={'FontColor','MainColor',
'AccentColor','BackgroundColor','OutlineColor'}for ag,ah in next,af do if ad.
Library and ad.Library.Options and ad.Library.Options[ah]then self.Library[ah]=
ad.Library.Options[ah].Value end end self.Library.AccentColorDark=self.Library:
GetDarkerColor(self.Library.AccentColor)self.Library:UpdateColorsUsingRegistry()
end function ad:LoadDefault()local af,ag,ah='Default',isfile(self.Folder..
'/themes/default.txt')and readfile(self.Folder..'/themes/default.txt'),true if
ag then if self.BuiltInThemes[ag]then af=ag elseif self:GetCustomTheme(ag)then
af=ag ah=false end elseif self.BuiltInThemes[self.DefaultTheme]then af=self.
DefaultTheme end if ah and ad.Library then ad.Library.Options.
ThemeManager_ThemeList:SetValue(af)else self:ApplyTheme(af)end end function ad:
SaveDefault(af)writefile(self.Folder..'/themes/default.txt',af)end function ad:
CreateThemeManager(af)af:AddLabel'Background color':AddColorPicker(
'BackgroundColor',{Default=self.Library.BackgroundColor})af:AddLabel'Main color'
:AddColorPicker('MainColor',{Default=self.Library.MainColor})af:AddLabel
'Accent color':AddColorPicker('AccentColor',{Default=self.Library.AccentColor})
af:AddLabel'Outline color':AddColorPicker('OutlineColor',{Default=self.Library.
OutlineColor})af:AddLabel'Font color':AddColorPicker('FontColor',{Default=self.
Library.FontColor})local ag={}for ah,b in next,self.BuiltInThemes do table.
insert(ag,ah)end table.sort(ag,function(c,d)return self.BuiltInThemes[c][1]<self
.BuiltInThemes[d][1]end)af:AddDivider()af:AddDropdown('ThemeManager_ThemeList',{
Text='Theme list',Values=ag,Default=1})af:AddButton('Set as default',function()
self:SaveDefault(ad.Library.Options.ThemeManager_ThemeList.Value)self.Library:
Notify(string.format('Set default theme to %q',ad.Library.Options.
ThemeManager_ThemeList.Value))end)ad.Library.Options.ThemeManager_ThemeList:
OnChanged(function()self:ApplyTheme(ad.Library.Options.ThemeManager_ThemeList.
Value)end)af:AddDivider()af:AddInput('ThemeManager_CustomThemeName',{Text=
'Custom theme name'})af:AddDropdown('ThemeManager_CustomThemeList',{Text=
'Custom themes',Values=self:ReloadCustomThemes(),AllowNull=true,Default=1})af:
AddDivider()af:AddButton('Save theme',function()self:SaveCustomTheme(ad.Library.
Options.ThemeManager_CustomThemeName.Value)ad.Library.Options.
ThemeManager_CustomThemeList:SetValues(self:ReloadCustomThemes())ad.Library.
Options.ThemeManager_CustomThemeList:SetValue(nil)end):AddButton('Load theme',
function()self:ApplyTheme(ad.Library.Options.ThemeManager_CustomThemeList.Value)
end)af:AddButton('Refresh list',function()if ad.Library then ad.Library.Options.
ThemeManager_CustomThemeList:SetValues(self:ReloadCustomThemes())ad.Library.
Options.ThemeManager_CustomThemeList:SetValue(nil)end end)af:AddButton(
'Set as default',function()if ad.Library and ad.Library.Options.
ThemeManager_CustomThemeList.Value~=nil and ad.Library.Options.
ThemeManager_CustomThemeList.Value~=''then self:SaveDefault(ad.Library.Options.
ThemeManager_CustomThemeList.Value)self.Library:Notify(string.format(
'Set default theme to %q',ad.Library.Options.ThemeManager_CustomThemeList.Value)
)end end)ad:LoadDefault()local c=function()self:ThemeUpdate()end ad.Library.
Options.BackgroundColor:OnChanged(c)ad.Library.Options.MainColor:OnChanged(c)ad.
Library.Options.AccentColor:OnChanged(c)ad.Library.Options.OutlineColor:
OnChanged(c)ad.Library.Options.FontColor:OnChanged(c)end function ad:
GetCustomTheme(af)local ag=self.Folder..'/themes/'..af if not isfile(ag)then
return nil end local ah=readfile(ag)local b,c=pcall(ac.JSONDecode,ac,ah)if not b
then return nil end return c end function ad:SaveCustomTheme(af)if af:gsub(' ',
'')==''then return self.Library:Notify('Invalid file name for theme (empty)',3)
end local ag,ah={},{'FontColor','MainColor','AccentColor','BackgroundColor',
'OutlineColor'}for b,c in next,ah do ag[c]=ad.Library.Options[c].Value:ToHex()
end writefile(self.Folder..'/themes/'..af..'.json',ac:JSONEncode(ag))return nil
end function ad:ReloadCustomThemes()local af,ag=listfiles(self.Folder..'/themes'
),{}for ah=1,#af do local b=af[ah]if b:sub(-5)=='.json'then local c=b:find(
'.json',1,true)local d=b:sub(c,c)while d~='/'and d~='\\'and d~=''do c=c-1 d=b:
sub(c,c)end if d=='/'or d=='\\'then table.insert(ag,b:sub(c+1))end end end
return ag end function ad:SetLibrary(af)self.Library=af end function ad:
BuildFolderTree()local af,ag={},self.Folder:split'/'for ah=1,#ag do af[#af+1]=
table.concat(ag,'/',1,ah)end table.insert(af,self.Folder..'/themes')table.
insert(af,self.Folder..'/settings')for ah=1,#af do local b=af[ah]if not
isfolder(b)then makefolder(b)end end end function ad:SetFolder(af)self.Folder=af
self:BuildFolderTree()end function ad:CreateGroupBox(af)assert(self.Library,
'Must set ThemeManager.Library first!')return af:AddLeftGroupbox'Themes'end
function ad:ApplyToTab(af)assert(self.Library,
'Must set ThemeManager.Library first!')local ag=self:CreateGroupBox(af)self:
CreateThemeManager(ag)end function ad:ApplyToGroupbox(af)assert(self.Library,
'Must set ThemeManager.Library first!')self:CreateThemeManager(af)end ad:
BuildFolderTree()end return ad end end local aa={}aa.GetUI=function()return a.
load'b'end aa.GetSaveManager=function()return a.load'c'end aa.GetThemeManager=
function()return a.load'd'end return aa
