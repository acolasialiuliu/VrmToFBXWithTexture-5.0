# VrmToFBXWithTexture plugin


## Introduction to Plugins


VrmToFBXWithTexture is a Blender plugin for converting and exporting VRM models to FBX format files with textures. This plugin addresses texture loss and material display anomalies that can occur with the default VRM to FBX conversion in Blender 5.0. <img style="margin-right: 30px;" align="left" src="images/VrmToFBXWithTexture.png"/>


## Features


- **One-click copy VRM model**: Automatically copy imported VRM models to a new collection, preserving materials and textures
- **Intelligent Texture Processing**: Supports multiple texture extraction methods, ensuring that textures from different VRM models are correctly identified and processed
- **FBX Export Optimization**: Automatically sets export parameters, ensuring textures are properly embedded in FBX files
- **Transparent Channel Support**: Automatically detects and processes transparent textures, maintaining the transparency of the model
- **Safe Cleanup**: Provides a cleanup feature to remove temporarily created models, materials, and textures without affecting the original file


## Installation Method


1. Download the 'VrmToFBXWithTexture_fixed.py' file
2. Open Blender
3. Click on 'Edit' -> 'Preferences' in the menu bar
4. Select 'Plugins' in the left panel
5. Click on the 'Install' button in the top right corner
6. Select the downloaded fileVrmToFBXWithTexture_fixed.py
7. Check the box next to the plugin name to enable the plugin


## Instructions for use


### Preparation


1. Import VRM models in Blender (tools such as [VRM Add-on](https://github.com/saturday06/VRM-Addon-for-Blender)) are available)
2. Make sure the model is fully loaded, including materials and textures


### Plugin interface


The plugin panel is located in the right sidebar of the 3D window (press the 'N' key to display), under the "Vrm to FBX" tab.


### Function buttons


#### 1. Copy


- **Function**: Copy the VRM model from the current scene to a new collection
- **Action**: Click the "Copy" button
- **Results**:
  - Create a new collection called "VrmToFBX_Collection"
  - Create a copy of the model in that collection
  - Automatically handles materials and textures to ensure they display correctly in Blender


#### 2. Export


- **Functions**: Export the copied model as an FBX file
- **Actions**: Click the "Export" button
- **Results**:
  - A pop-up FBX export window
  - Automatically select the replicated model
  - Automatically set export parameters (embed textures, path_mode=COPY)
  - Select the save path and click "Export FBX"


#### 3. Clear


- **Function**: Clean up copied models and temporary files
- **Action**: Click the "Clear" button
- **Results**:
  - Delete the "VrmToFBX_Collection" collection and the models in it
  - Delete temporarily created materials and textures
  - Clean up temporary folders (only delete files created by plugins)


#### 4. One key for all


- **Function**: Automates the complete process of copy->export-> purge
- **Operation**:
  1. Set the FBX save path in the "Export Path" input box
  2. Click on the "One key for all" button
- **Results**:
  - Automatically copy models
  - Export the FBX file to the specified path
  - Automatically clean up temporary files


## Considerations


1. **VRM Import**: Ensure that the model has been imported into Blender using a compatible VRM import tool
2. **Texture Processing**: The plugin automatically handles the packaged texture, unpacking it into a temporary location
3. **Export Path**: When using the "One key for all" function, you need to set a valid export path in advance
4. **Version Compatibility**: The plugin is compatible with Blender 5.0 and is compatible with Blender 2.80 and above
5. **Complex Materials**: For complex PBR materials, the plugin extracts the base color texture, and other material properties may need to be manually adjusted


## FAQs


### Problem: The model turns white after copying


Resolved: The plugin has fixed this issue to ensure that the material nodes are properly connected


### Problem: Exported FBX has no textures


**Solved**: The plugin automatically sets the FBX export parameters, ensuring that the texture is embedded in the file


### Problem: Blender Error "Principled BSDF node not found"


**Solution**: The plugin has added a node existence check to automatically create the necessary nodes


## Version information


- **Current Version**: 1.0.1
- **Updated**: 2025-12-16
- **Fixes**:
  - Resolved an issue with the Principled BSDF node in Blender 5.0
  - Improved texture extraction logic
  - Fixed material node connections
  - Supports transparent texture processing


## Author Information


- **Original author**:D 3LN
- **Fixes and Improvements**: Liufen 792818521@qq.com


## License


This plugin is licensed under the MIT license and is free to use and modify.


---


**Usage Tips**: If you encounter issues during use, it is recommended to first check that the VRM model is imported correctly and ensure that all textures are loaded correctly.

# VrmToFBXWithTexture 插件

## 插件简介

VrmToFBXWithTexture 是一个 Blender 插件，用于将 VRM 模型转换并导出为带有纹理的 FBX 格式文件。该插件解决了 Blender 5.0 中默认 VRM 到 FBX 转换可能出现的纹理丢失和材质显示异常问题。<img style="margin-right: 30px;" align="left" src="images/VrmToFBXWithTexture.png"/>

## 功能特点

- **一键复制 VRM 模型**：自动复制导入的 VRM 模型到新集合，保留材质和纹理
- **智能纹理处理**：支持多种纹理提取方式，确保正确识别和处理不同 VRM 模型的纹理
- **FBX 导出优化**：自动设置导出参数，确保纹理正确嵌入到 FBX 文件中
- **透明通道支持**：自动检测并处理透明纹理，保持模型的透明效果
- **安全清理**：提供清理功能，移除临时创建的模型、材质和纹理，不影响原始文件

## 安装方法

1. 下载 `VrmToFBXWithTexture_fixed.py` 文件
2. 打开 Blender
3. 点击菜单栏的 `编辑` -> `首选项`
4. 在左侧面板选择 `插件`
5. 点击右上角的 `安装` 按钮
6. 选择下载的 `VrmToFBXWithTexture_fixed.py` 文件
7. 勾选插件名称旁的复选框启用插件

## 使用说明

### 准备工作

1. 在 Blender 中导入 VRM 模型（可使用 [VRM Add-on](https://github.com/saturday06/VRM-Addon-for-Blender) 等工具）
2. 确保模型已完全加载，包括材质和纹理

### 插件界面

插件面板位于 3D 视窗的右侧边栏（按 `N` 键显示），在 "Vrm to FBX" 标签下。

### 功能按钮

#### 1. Copy（复制）

- **功能**：复制当前场景中的 VRM 模型到新集合
- **操作**：点击 "Copy" 按钮
- **结果**：
  - 创建名为 "VrmToFBX_Collection" 的新集合
  - 在该集合中创建模型副本
  - 自动处理材质和纹理，确保在 Blender 中正确显示

#### 2. Export（导出）

- **功能**：导出复制的模型为 FBX 文件
- **操作**：点击 "Export" 按钮
- **结果**：
  - 弹出 FBX 导出窗口
  - 自动选择复制的模型
  - 自动设置导出参数（嵌入纹理，path_mode=COPY）
  - 选择保存路径并点击 "导出 FBX"

#### 3. Clear（清除）

- **功能**：清理复制的模型和临时文件
- **操作**：点击 "Clear" 按钮
- **结果**：
  - 删除 "VrmToFBX_Collection" 集合及其中的模型
  - 删除临时创建的材质和纹理
  - 清理临时文件夹（仅删除插件创建的文件）

#### 4. One key for all（一键导出）

- **功能**：自动执行复制 -> 导出 -> 清除的完整流程
- **操作**：
  1. 在 "Export Path" 输入框中设置 FBX 保存路径
  2. 点击 "One key for all" 按钮
- **结果**：
  - 自动复制模型
  - 导出 FBX 文件到指定路径
  - 自动清理临时文件

## 注意事项

1. **VRM 导入**：确保已使用兼容的 VRM 导入工具将模型导入 Blender
2. **纹理处理**：插件会自动处理打包纹理，将其解包到临时位置
3. **导出路径**：使用 "One key for all" 功能时，需提前设置有效的导出路径
4. **版本兼容**：该插件已适配 Blender 5.0，同时兼容 Blender 2.80 及以上版本
5. **复杂材质**：对于复杂的 PBR 材质，插件会提取基础颜色纹理，其他材质属性可能需要手动调整

## 常见问题

### 问题：模型复制后变成白色

**解决**：插件已修复此问题，确保正确连接材质节点

### 问题：导出的 FBX 没有纹理

**解决**：插件会自动设置 FBX 导出参数，确保纹理嵌入到文件中

### 问题：Blender 报错 "Principled BSDF node not found"

**解决**：插件已添加节点存在性检查，自动创建必要的节点

## 版本信息

- **当前版本**：1.0.1
- **更新日期**：2025-12-16
- **修复内容**：
  - 解决 Blender 5.0 中的 Principled BSDF 节点问题
  - 改进纹理提取逻辑
  - 修复材质节点连接
  - 支持透明纹理处理

## 作者信息

- **原作者**：D3LN
- **修复与改进**：Liufen 792818521@qq.com

## 许可证

本插件采用 MIT 许可证，可自由使用和修改。

---

**使用提示**：如果您在使用过程中遇到问题，建议先检查 VRM 模型的导入是否正确，确保所有纹理已正确加载。
