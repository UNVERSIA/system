# 污水处理甲烷智能监测与调控系统

## Streamlit Cloud 部署说明

### 修复内容

1. **添加 TensorFlow 依赖**: 在 `requirements.txt` 中添加了 `tensorflow-cpu>=2.15.0`
2. **添加容错处理**: 修改 `lstm_predictor.py`，当 TensorFlow 导入失败时自动切换到备用统计预测模式
3. **添加系统依赖**: 创建 `packages.txt` 包含必要的系统级库
4. **文件结构优化**: 将所有代码文件移到仓库根目录

### 部署步骤

1. 推送代码到 GitHub
2. 访问 https://streamlit.io/cloud
3. 创建新应用，选择此仓库
4. 主文件路径设置为 `app.py`
5. 点击部署

### 注意事项

- 如果 TensorFlow 安装失败，系统会自动使用基于统计的备用预测模式
- 所有核心功能在备用模式下仍然可用
