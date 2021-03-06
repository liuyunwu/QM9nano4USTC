# QM9nano4USTC
中科大数据科学导论课程实验-QM9数据集

**注意： 本数据集仅供中科大数据科学导论的课程实验使用，其他用途请以[原始数据集](https://www.nature.com/articles/sdata201422)为准**

本项目为中国科学技术大学数据科学导论课程实验中QM9数据集的介绍:
QM9数据集包括了13万有机分子的构成,空间信息及其对应的属性. 它被广泛应用于各类数据驱动的分子属性预测方法的实验和对比.  
除了原始数据外,本项目整理了一些有效的预处理/特征工程方案,如CM,BOB,BAML等.   
下载地址:  
**百度云** 链接：https://pan.baidu.com/s/1l2inzj8HfdjG0bLdzIDJwg 密码：kv7w  
**科大校内睿客网** 链接：http://rec.ustc.edu.cn/share/f1cb7d40-d784-11e8-9b9f-9956ec9638a8 

[原始数据集](https://www.nature.com/articles/sdata201422)给出了133,885个分子的相关信息,由于缺失值等原因,本项目给出130,462个分子的信息,具体文件如下:

+ QM9_nano.npz 文件 该文件需要用`numpy`读取,其中包含三个字段:
  + 'ID' 分子的id,如:qm9:000001 
  + 'Atom' 分子的原子构成,为一个由原子序数的列表构成,如[6,1,1,1,1]表示该分子由一个碳(C)原子和4个氢(H)原子构成.
  + 'Distance' 分子中原子的距离矩阵,以上面[6,1,1,1,1]分子为例,它的距离矩阵即为一个5x5的矩阵,其中行列的顺序和上述列表一致,即矩阵的第N行/列对应的是列表的第N个原子信息.
  + 'U0' 分子的能量属性(温度为0K时),也是我们需要预测的值

除了上述数据外,我们还提供了一些以及做好的特征工程结果,这些数据均为tsv格式,建议使用`pandas`读取.
每行一条数据,第一列为分子的ID,这些特征有:

+ BOB.tsv
+ BAML.tsv
+ CM.tsv
+ ECFP4.tsv   

具体的特征工程方法以及表征的意义参见[Faber的论文](https://pubs.acs.org/doi/10.1021/acs.jctc.7b00577), [中文解释](https://ajz34.github.io/post/Faber-Repetition/). 



