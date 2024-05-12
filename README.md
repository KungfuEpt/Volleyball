# Все изменения
Я (KungfuEpt) переделал этот плагин, чтобы он работал на 1.20.4 и выше. **НЕ ИСПОЛЬЗУЙТЕ ДАННЫЙ ПЛАГИН НА ВЕРСИЯХ НИЖЕ, ВРЯД ЛИ БУДЕТ РАБОТАТЬ.**


# Волейбольные мячи

![gif](volleyball.gif)

Простой плагин, ориентированный на приватные сервера, добавляющий волейбольные мячи

# Использование
* Для создания мяча необходимо, по живой рыбе-фугу, кликнуть правой кнопкой мыши, держа 8 кожи в руке
* Бросить мяч - ЛКМ
* Бросить мяч сильнее - ЛКМ при беге или в прыжке.
* Ползунок силы броска - SHIFT
* Подобрать мяч - SHIFT рядом с мячем
* /ballskin - смена скина мяча
* /ballsreload - перезагрузка плагина. Требуется право `volleyball.reload`

# Конфигурация

**Основная конфигурация:**
```yaml
# Вся скорость измеряется в BPS - блоках в секунду

IPT: 20 # Количество итераций обратоки физики за тик. Не советуется менять

GRAVITY: -0.05 # гравитация

DEFAULT_BOUNCE_ENERGY_LOSS: 2 # Стандартная потеря энергии при отскоке. Energy / DEFAULT_BOUNCE_ENERGY_LOSS

MAX_SPEED: 40 # Максимальная скорость мяча
MAX_ROT_SPEED: 100 # Максимальная скорость врящения мяча
ROT_BREAKING_SPEED: 1000 # Максимальная скорость торможения вращения мяча
ROT_SPEED_PROPORTION: 1000 # Пропорция ускорения вращения от скорости. При отскоке мяча

THROW_CHECKING_SPEED: 0.06 # Скорость ползунка силы броска
MAX_THROW_POWER: 17 # Максимальная сила броска (В BPS)
MIN_THROW_POWER: 8 # Минимальная сила броска (В BPS)

DESPAWN_TIME: 10000 # Время(в тиках), по истечения которого лежащий неподвижно мяч будет дропнут
DEFAULT_SKULLSKIN: ball # Стандартный скин мяча

# Натсройки для блоков

TRANSPARENT_BLOCKS: # Блоки, через которые может проходить мяч
  - AIR
  - VOID_AIR
  - CAVE_AIR
  - GRASS

BLOCKS_ENERGY_LOSSES: # Индивидуальные потери энергии для блоков
  WATER: 5
  SLIME_BLOCK: 1
  MOSS_BLOCK: 3
  HAY_BLOCK: 5
  HONEY_BLOCK: 100
  ICE: 1.2
  PACKED_ICE: 1.1
  BLUE_ICE: 0.9
```

**конфигурация скинов:**

```yaml
# skin:
#   name: <имя>
#   url: <url скина. Прописывать url полностью не надо. Только id в конце url>
#   perm: <Пермишон для мяча>                                         *Опционально
#   lock_msg: <Сообщения под мячем, для тех, кто не имеет пермишона>  *Опционально

ball:
  name: Мяч
  url: 93c2f1c5d2c8f0e33730c14dca1c1d1e1abd8596b0839d6738d18f46432b6fa6
```

# Некотрое пояснение
Этот плагин изначально разрабатывался для сервера [Schalker Vanilla](https://schalker.ru/) На коем я был сначала разрабом, а потом встал на руководство.
После некоторых действий со стороны главного руководителя - Ромы, я по собственному желанию покидаю пост, как и большая часть администрации/разработчиков.
Через некоторое время, я узнаю, что студия [Box](https://vk.com/boxbuild), в котрой находится тот самый Рома, продала плагин без моего ведома уже 2 серверам.
По сему я и выложил его в открытый доступ.
Сам плагин они выдрали из системы "как есть". Поэтому он и поставлялся в 2-х плагинах - "bbnb" и "OblivionGU".
Здесь же лежит независимая версия, удобная для использования.
