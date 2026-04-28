# 固定位置候选窗口配置

## 功能说明

候选窗口可以固定在屏幕的指定位置，而不是跟随光标移动。

## 配置方法

编辑 `~/Library/Rime/squirrel.custom.yaml`，添加以下配置：

```yaml
patch:
  style:
    # 启用固定位置
    fixed_position: true
    # X 坐标（距离屏幕左边缘的像素）
    fixed_position_x: 100
    # Y 坐标（距离屏幕底边缘的像素）
    fixed_position_y: 100
```

## 坐标说明

- `fixed_position_x`: 候选窗口左边缘距离屏幕左边缘的距离（像素）
- `fixed_position_y`: 候选窗口底边缘距离屏幕底边缘的距离（像素）

## 示例配置

### 左下角
```yaml
patch:
  style:
    fixed_position: true
    fixed_position_x: 20
    fixed_position_y: 20
```

### 右下角
```yaml
patch:
  style:
    fixed_position: true
    fixed_position_x: 1700  # 根据屏幕宽度调整
    fixed_position_y: 20
```

### 屏幕中央底部
```yaml
patch:
  style:
    fixed_position: true
    fixed_position_x: 800  # 屏幕宽度的一半
    fixed_position_y: 100
```

## 注意事项

1. 修改配置后需要重新部署：点击输入法菜单 → 重新部署
2. 坐标值需要根据你的屏幕分辨率调整
3. 设置 `fixed_position: false` 可恢复跟随光标模式
