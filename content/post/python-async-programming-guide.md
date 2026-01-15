+++
date = '2025-01-14'
draft = false
title = 'Python异步编程入门指南'
tags = ['python', 'async', 'programming', 'tutorial']
categories = ['programming']
+++

# Python异步编程入门指南

异步编程是现代Python开发中的重要技能。本文将带你从基础概念到实际应用，掌握asyncio的核心用法。

## 为什么需要异步编程

在传统的同步编程中，程序按顺序执行每个任务。当遇到I/O操作（如网络请求、文件读写）时，程序会阻塞等待完成。这在高并发场景下效率很低。

异步编程允许程序在等待I/O时继续执行其他任务，大大提高并发性能。

## 基本概念

### 协程 (Coroutine)
协程是异步编程的核心。使用 `async def` 定义：

```python
async def hello():
    print("Hello")
    await asyncio.sleep(1)
    print("World")
```

### await 关键字
`await` 用于等待异步操作完成：

```python
import asyncio

async def fetch_data():
    # 模拟网络请求
    await asyncio.sleep(2)
    return "数据获取完成"

async def main():
    result = await fetch_data()
    print(result)

asyncio.run(main())
```

## 并发执行任务

使用 `asyncio.gather()` 并发执行多个异步任务：

```python
import asyncio

async def task1():
    await asyncio.sleep(1)
    return "任务1完成"

async def task2():
    await asyncio.sleep(2)
    return "任务2完成"

async def main():
    results = await asyncio.gather(task1(), task2())
    print(results)

asyncio.run(main())
```

## 实际应用示例

### 异步HTTP请求

```python
import aiohttp
import asyncio

async def fetch_url(session, url):
    async with session.get(url) as response:
        return await response.text()

async def main():
    urls = [
        'https://api.github.com/users/asdevao',
        'https://api.github.com/repos/asdevao/myrepo'
    ]
    
    async with aiohttp.ClientSession() as session:
        tasks = [fetch_url(session, url) for url in urls]
        results = await asyncio.gather(*tasks)
        
        for i, result in enumerate(results):
            print(f"URL {i+1}: {len(result)} 字符")

asyncio.run(main())
```

## 注意事项

1. **不要在循环中滥用await**：会导致顺序执行失去异步优势
2. **正确处理异常**：异步代码的异常处理与同步不同
3. **避免阻塞操作**：不要在异步函数中使用同步I/O

## 总结

异步编程让Python能够高效处理并发任务。掌握asyncio后，你可以构建高性能的网络应用、API服务和数据处理程序。

在下一个教程中，我们将探讨更高级的异步模式和最佳实践。

有什么问题欢迎在评论区讨论！