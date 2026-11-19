# ServeTrace · 模型调用网关

ServeTrace 为 AppliedAI 提供非流式模型转发。调用方用 Key 访问模型，超限时依据 `Retry-After` 安排重试，并可用请求 ID 在控制台定位本次调用。

[查看完整案例中的网关规则、耗时说明和日志截图](appliedai-platform.md#servetrace) · [返回案例目录](README.md)
