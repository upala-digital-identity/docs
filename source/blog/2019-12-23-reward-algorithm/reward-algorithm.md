ТЗ на алготиртм.

# Обязательно:
## buffer
Возможность создавать группы буферы

## Инициатива поднимать цену за бота
Чем выше группа, тем должна быть выше цена за бота. 



# Подумать
## 0-payment
Возможность создавать группы с нулевой наградой. Или может быть эта награда будет равна награде нижестоящей группы?

Такая группа ничем не рискует. Нужна ли такая группа в принципе? Это может быть приложение. __Приложениям должно быть легко добавлять группы__, которым они доверяют. Пока на этой возможности планируется строить различные схемы оплаты. 

Или это группы, которые не планируют вступать куда-то дальше. Информация для себя. Ну, приложения, для простоты.

## botnet-reward
Возможность целой ветке взорваться. Супер-наказание. 

## invite-free
Невозможно включить члена в группу без его ведома и навариться на этом. При таком алгоритме нет необходимости подтверждать приглашения. 

Например. Появляется более дорогая группа сверху. Она определяет "надбавку" за бота. Добавляя более дешевую группу, она рискует. 
Ну, а более низкая группа рискует тем, что кто-то теперь решит взорваться. Нормально. Но никому из этих групп нет смысла создавать более дорогую группу сверху ради наживы, потому что они ничего не получат сверх.  


# Примеры
## Алгоритм 1. invite-free. 
Вычисляем bot_reward в верхней группе:
    bot_reward = max_bot_reward * user_score
В этой группе выплачиваем current_bot_reward: 
    current_bot_reward = bot_reward - bot_reward всех нижестоящих. 

## Алгоритм 2. buffer, 0-payment
Максимальные выплаты внизу.

    function attack(address[] calldata path, address payable bot, uint remainingReward) external onlyMember {
        // calculate maxBotReward and payout the sum starting from the bottom. Stop when the sum is payed.
        uint currentGroupReward = maxBotReward * membersScores[msg.sender];  // todo is this simplification correct?
        IUpalaGroup nextUpalaGroup = IUpalaGroup(path[path.length-1]);
        
        _rewardBot(bot, currentGroupReward);
        
        address[] memory newPath = path;
        nextUpalaGroup.attack(popFromMemoryArray_Hacked(newPath), bot, remainingReward - currentGroupReward);
    }

## Алгоритм 3.