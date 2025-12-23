# XToys 配置記錄

## 振動玩具

### Vibe Intensity

- 振動等級：`[關閉, 低, 一般, 高, 最多]` <=> `[0, 0.5, 0.7, 0.9, 1.0]`
- 低級輸出設高一點，確保最低輸出時，玩具能帶來快感

### Toy Events

- 用於合成輸出的插槽，即何處的振動玩具可以參與輸出數值的合成
- 每一項的作用
  - `Name`            插槽名称
  - `Weight`          該處輸出時的佔比
  - `RampTimeMS`      到達目標數值所需要的時間

## 動作輸出(actions)

- 設置可以用於輸出的動作及其所輸出的大小
- 各項作用
  - `Type` 只能使用 `OnSelf` 和 `OnOther` 兩箇字符串
    - `OnSelf`      自己對自己和別人對自己的動作都能產生輸出
    - `OnOther`     僅自己對別人的動作纔產生輸出，任何對自己的動作均不作響應
  - `Intensity`       該動作的輸出的等級，取值 `[1, 100]`
  - `DurationMS`      該動作從開始輸出到開始降低的時間，當比 `RampTimeMS` 大
  - `RampTimeMS`      用多長時間到達輸出等級
  - `Names`           可以處理動作的位置
  - `Actions`         可以處理的動作
  - `Item`            該動作觸發時的道具，無道具是 `none`

### 動作名（Actions）

- 電繫
  - `ShockLow`          低强度
  - `ShockMed`          中强度
  - `ShockHigh`         高强度
  - `ShockItem`         使用物品電繫某處

### 打
  - `Slap`              扇
  - `Spank`             拍
  - `SpankItem`         用物鞭打

