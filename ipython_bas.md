
# ipython 的一些功能介绍
   - **内省 ? 字符串或函数可以显示其功能**


```python
test_one = 'xihua?'
test_one?
test_two = 15615
test_two?
```

#### 函数或者实例的话可以显示信息
   - **如果是？？ 俩个的话，可以显示源代码**


```python
def func_test():
    '''这个是docstring'''
    print('test1')
func_test??
```

#### 还有一种用法就是
   - 查看一个库的命名空间的所有函数
   - **模块.*load*?**


```python
import numpy as np
np.*load*?
```

#### %run 模块名.py 可以运行一个模块


```python
# %run test_list.ipynb
```

### 测试函数运行使用了多长时间
   - **%time  或者  %timeit**
   - **%timeit比较精确，可以精确到毫秒，纳秒，推荐使用**


```python
laji = [i**2 for i in range(1,100)]

# %time laji = [i**2 for i in range(1,10000)]

# %timeit [i**2 for i in range(1,10000)]
```

    Wall time: 13 ms
    12.3 ms ± 1.01 ms per loop (mean ± std. dev. of 7 runs, 100 loops each)
    


```python
xihua = 'fooder'
food = 'foo'
# %timeit xihua.startswith(food)
```

    466 ns ± 19.7 ns per loop (mean ± std. dev. of 7 runs, 1000000 loops each)
    

### 分析性能代码  cProfile
   - python -m cProfile 模块名.py

## 还需要查看更多细节可以查看数据分析这本书
