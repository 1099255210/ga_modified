

# Generative Agents: Interactive Simulacra of Human Behavior 

***注：这是一个修改过的版本，主要根据issues修改了一些原仓库的问题，以及将一些过时的昂贵模型替换为当前官网上的平价模型，对代码结构并没有做出什么改变***

## 使用指南

### 配置 api_key

在 `utils.py` 中设置 `openai_api_key = ""`
 
### 安装依赖

Python==3.9.12

```shell
pip install -r requirements.txt
```

### 启动前后端

后端

```shell
cd environment/frontend_server
python manage.py runserver
```

然后在浏览器打开提示的网址 <http://127.0.0.1:8000/>，注意这个页面要保持开启状态，不知道为什么作者的后端和前端有如此紧密的联系（建议使用 chrome）。

接着开启后端：

```shell
cd reverie/backend_server
python reverie.py
```

选择一个存档，然后会显示 Enter option: 

这时后端已经开启，输入 `run 10` 就可以向后运行十个 steps。

网页上打开 <http://127.0.0.1:8000/simulator_home> 可以看到当前的模拟情况

### 查看回放

如果想要查看当前存档的回放，可以在浏览器中输入：```http://127.0.0.1:8000/[存档名]/[step]```

这里存档名就是之前选择的存档，step 就是想要从这个存档的哪个点开始回放，例如存档名为：`20240115_140054_test` 那么网址为 `http://127.0.0.1:8000/replay/20240115_140054_test/0/` 表示从第 0 个 step 开始回放这个存档。

## 其余内容

需要更多的信息查看原仓库： <https://github.com/joonspk-research/generative_agents>
