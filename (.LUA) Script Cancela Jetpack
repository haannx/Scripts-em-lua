# Scripts-em-lua
Alguns dos meus trabalhos em .lua, principalmente para jogos como MTA

#Script que determina uma área onde os jogadores não podem usar o jetpack(mochila voadora)

local jetpackArea = createColRectangle(x1, y1, x2, y2) --


function onPlayerEnterArea(player)
    if getPedControlState(player, "jump") and isElementWithinColShape(player, jetpackArea) then
        removePedJetPack(player) -- 
        outputChatBox("O uso de Jetpack está bloqueado nesta área.", player) --
    end
end
addEventHandler("onColShapeHit", jetpackArea, onPlayerEnterArea)

function onPlayerInsideArea(player)
    if getPedControlState(player, "jump") and isElementWithinColShape(player, jetpackArea) then
        toggleControl(player, "jump", false) --
    end
end
addEventHandler("onPlayerStealthKill", root, onPlayerInsideArea)
addEventHandler("onPlayerMeleeAttack", root, onPlayerInsideArea)
addEventHandler("onPlayerJoin", root, onPlayerInsideArea)
Substitua x1, y1, x2, y2 pelas coordenadas
