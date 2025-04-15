# Button Animation
Roblox Studio'da, oluşturulmuş bir butona LocalScript yolu ile animasyon ekleyebiliriz.

```
local button = script.Parent

local animTime = 0.5

local startCoordination = button.Rotation

local TweenService = game:GetService("TweenService")

local TweenInfo1 = TweenInfo.new(
    animTime,
    Enum.EasingStyle.Quint,
    Enum.EasingDirection.Out
)

local animation1 = TweenSevice:Create(button, TweenInfo1, {Rotation = 4})

local animation2 = TweenSevice:Create(button, TweenInfo1, {Rotation = startCoordination})

local function onMouse()
    animation1:Play()
    wait(1)    
end

local function outMouse()
    animation2:Play()
    wait(1)
end

button.MouseEnter:Connect(onMouse)

button.MouseLeave:Connect(outMouse)
```

Oluşturduğunuz butona **LocalScript** ekleyin, yukarıdaki kodu içerisine yapıştırın. Bu kod, butonu kendi ekseni etrafında dönmesi için bir animasyon oluşturacak.

```local animation1 = TweenSevice:Create(button, TweenInfo1, {Rotation = 4})```

Yukardaki satırda bulunan **Rotation** satırındaki değeri arttırarak eksen etrafında dönme büyüklüğünü ayarlayabilirsiniz.
