# 确保我们已安装最新setuptools 和 wheel和twine
下面是安装/更新命令
```bash
python -m pip install --user --upgrade setuptools wheel twine
```

# 打包项目
```bash
python setup.py sdist bdist_wheel
```

# 使用 twine 将打包好的库/项目上传到PYPI

[登录pypi](https://pypi.org/)，用户名Wayne_jiang，获取api key

需用到PYPI帐号密码，此时只是上传到PYPI测试服，还不能 pip install 这个库/项目）。
https://test.pypi.org/
```bash
python -m twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```

将库上传到 PYPI正式服：
```bash
twine upload dist/*
```

# 版本更新
修改setup中的版本号，到根目录，打包、上传即可

