# 如何將寫好的package上傳到pypi供人安裝使用

[參考網站](https://medium.com/%E8%B3%87%E5%B7%A5%E7%AD%86%E8%A8%98/%E6%89%93%E5%8C%85python-module-%E5%88%B0pypi-%E4%B8%8A-aef1f73e1774)

# 如何更新
### 把package整理成如下形式
```
/example_pkg
  /example_pkg
    __init__.py
  setup.py
  LICENSE
  README.md
```

### 編輯setup.py
每次都要更新版本號

### 刪除dist資料夾

### 生成distribution archives
```
python setup.py sdist bdist_wheel
```
若未刪除dist 可以用
```
twine upload --skip-existing dist/*
```
忽略已建立的dist

[參考網站](https://ganjinzero.github.io/2019/01/17/%E5%9C%A8PyPI%E4%B8%8A%E5%8F%91%E5%B8%83%E5%B9%B6%E6%9B%B4%E6%96%B0%E8%87%AA%E5%B7%B1%E7%9A%84python-package/)
