# 自定义组件
## 什么是自定义组件?

Layotto 中的组件分为两种：
- 预置组件

比如 `PubSub` 组件，比如 `state.Store` 组件

- 自定义组件

允许您自己扩展自己的组件，比如[使用指南](zh/design/api_plugin/design?id=_24-使用指南) 中的 `HelloWorld` 组件。

## 配置文件结构
```json
  "custom_component": {
    "<Component Type>": {
      "<Component A Name>": {
        "metadata": {
          "<KEY>": "<VALUE>",
          "<KEY>": "<VALUE>"
        }
      },
      "<Component B Name>": {
        "metadata": {
          "<KEY>": "<VALUE>",
          "<KEY>": "<VALUE>"
        }
      }
    }
  },
```

您可以在metadata里配置组件关心的key/value配置。

## 示例
例如，在`configs/config_in_memory.json` 中，配置了类型是`helloworld` 的 `CustomComponent`，只有一个组件，其组件名是 `in-memory`:

```json
  "custom_component": {
    "helloworld": {
      "in-memory": {
        "metadata": {}
      }
    }
  },
```


## 如何使用"自定义组件"?
详见 [使用指南](zh/design/api_plugin/design?id=_24-使用指南) 