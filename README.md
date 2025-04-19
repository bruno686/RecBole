![RecBole Logo](asset/logo.png)

--------------------------------------------------------------------------------

# Scaling CF

### Install from conda

```bash
conda install -c aibox recbole
```

### Install from pip

```bash
pip install recbole
```

### Install from source
```bash
git clone https://github.com/RUCAIBox/RecBole.git && cd RecBole
pip install -e . --verbose
```

## Quick-Start
With the source code, you can use the provided script for initial usage of our library:

```bash
python run_recbole.py
```

## Tutorial (2025 April 19)
1.amazon-beauty：首次运行会出现`ValueError: Default process group has not been initialized, please make sure to call init_process_group.` 但是只要再运行一次即可。
```
python run_recbole.py --dataset=amazon-beauty --model=SGL --embedding_size=2 --gpu_id=0
```

2.amazon-books：首次运行会出现`ValueError: Default process group has not been initialized, please make sure to call init_process_group.` 但是只要再运行一次即可。
```
python run_recbole.py --dataset=amazon-books --model=SGL --embedding_size=2 --gpu_id=0
```

3.amazon-baby：首次运行会出现`ValueError: Default process group has not been initialized, please make sure to call init_process_group.` 但是只要再运行一次即可。
```
python run_recbole.py --dataset=amazon-baby --model=SGL --embedding_size=2 --gpu_id=0
```

4.gowalla-merged：首次运行会出现`ValueError: Default process group has not been initialized, please make sure to call init_process_group.` 但是只要再运行一次即可。
```
python run_recbole.py --dataset=gowalla-merged --model=SGL --embedding_size=2 --gpu_id=0
```

5.yelp2018
```
python run_recbole.py --dataset=yelp-2018 --model=SGL --embedding_size=2 --gpu_id=0
```
首次运行会出现 ValueError: File dataset/yelp-2018/yelp-2018.inter not exist.
把dataset里面的子文件夹内的数据集往前移动，把yelp-2018改为yelp2018

6.pinterest：首次运行会出现`ValueError: Default process group has not been initialized, please make sure to call init_process_group.` 但是只要再运行一次即可。
```
python run_recbole.py --dataset=pinterest --model=SGL --embedding_size=2 --gpu_id=0
```

7.ml-1m，douban也会`ValueError: Default process group has not been initialized, please make sure to call init_process_group.` 但是只要再运行一次即可。
```
python run_recbole.py --dataset=ml-1m --model=BPR --embedding_size=2 --gpu_id=0
python run_recbole.py --dataset=ml-100k --model=BPR --embedding_size=2 --gpu_id=0
python run_recbole.py --dataset=douban --model=BPR --embedding_size=2 --gpu_id=0

```

AttributeError: 'NoneType' object has no attribute 'keys' 是因为yaml文件为空
优先跑初bash_neumf.sh以外的