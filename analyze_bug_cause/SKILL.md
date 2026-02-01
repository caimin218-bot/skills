  "name": "analyze_bug_cause",
  "description": "对代码中的 Bug 进行深度根因分析 (Root Cause Analysis)。该工具会扫描代码逻辑、状态流转和潜在的边界条件，输出详细的故障诊断报告。注意：该工具不执行任何修复操作。",
  "input_schema": {
    "type": "object",
    "properties": {
      "bug_description": {
        "type": "string",
        "description": "对 Bug 现象的描述，包括预期行为与实际行为的差异。"
      },
      "relevant_files": {
        "type": "array",
        "items": {
          "type": "string"
        },
        "description": "涉及该 Bug 的相关源文件路径列表。"
      },
      "error_logs": {
        "type": "string",
        "description": "可选：运行时产生的错误日志或堆栈追踪信息。"
      }
    },
    "required": ["bug_description", "relevant_files"]
  }

