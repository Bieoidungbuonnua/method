repeat wait()
until game:IsLoaded()
wait()
local TableChat = {"Mọi người ơi","Ai chỉ mình chơi với","Mình mới chơi á","game này có trái ác quỷ đúng không mọi người?","ai cho mình xin trái ác quỷ với","Ai kết bạn với mình đi"}
spawn(function()
    while wait() do 
        pcall(function()
            game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(TableChat[math.random(0,#TableChat)],"All")
            wait(12)
        end)
    end
end)
