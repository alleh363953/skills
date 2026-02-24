# CLAUDE.md - Project Constitution & Rules

> [!IMPORTANT]
> 此檔案為本專案的最高開發憲章。Agent 必須在任何操作前優先閱讀並嚴格遵守以下所有規範。

1.核心溝通原則 (Communication)
語言規範：**全時段強制使用「繁體中文」**進行所有對話、註釋、文件撰寫及任務說明。

精準度要求：優先使用台灣技術術語（如：佈署、回測、實作、上下文）。

透明化思考：在執行複雜變更前，需先以繁體中文說明你的思考邏輯與預期影響。

2. Quantitative & Modeling Standards (量化與模型規範)
**Applies to all backtesting, model training, and data analysis.**

Methodology & Integrity
Rolling Window Mandatory**: All backtesting and training must utilize **Rolling Window / Walk-Forward Analysis** (滾動式回測). Static train/test splits are prohibited unless explicitly requested.
No Look-ahead Bias**: Strictly separate data chronologically. Ensure no future data leaks into the training set (嚴禁未來視).
Anti-Overfitting**: Implement robust cross-validation and regularization techniques to prevent model overfitting (無過度擬合).

File Management
No Overwriting**: **Never overwrite** existing model weights, training logs, or historical datasets (防止舊檔案覆蓋).
Versioning**: Always save new training results or model checkpoints with timestamps or version tags.
