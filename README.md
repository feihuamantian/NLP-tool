# NLP-tool
## （1）中文分词，词性标注，命名实体识别，新词发现，关键词，文本摘要，文本相似度，科学计算器，中文数字阿拉伯数字(罗马数字)转换，中文繁简转换，拼音转换。
github url: https://github.com/yongzhuo/Macropodus
About 自然语言处理工具Macropodus，基于Albert+BiLSTM+CRF深度学习网络架构，中文分词，词性标注，命名实体识别，新词发现，关键词，文本摘要，文本相似度，科学计算器，中文数字阿拉伯数字(罗马数字)转换，中文繁简转换，拼音转换。

## （2）时间转换工具：
github url : https://github.com/zhanzecheng/Time_NLP

### pip install arrow==0.14.0
用于句子中时间词的抽取和转换
详情请见test.py

res = tn.parse(target=u'过十分钟') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)
res = tn.parse(target=u'2013年二月二十八日下午四点三十分二十九秒', timeBase='2013-02-28 16:30:29') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)
res = tn.parse(target=u'我需要大概33天2分钟四秒', timeBase='2013-02-28 16:30:29') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)
res = tn.parse(target=u'今年儿童节晚上九点一刻') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)
res = tn.parse(target=u'2个小时以前') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)
res = tn.parse(target=u'晚上8点到上午10点之间') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

from TimeNormalizer import TimeNormalizer # 引入包

tn = TimeNormalizer()

res = tn.parse(target=u'晚上8点到上午10点之间') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

res = tn.parse(target=u'2013年二月二十八日下午四点三十分二十九秒', timeBase='2013-02-28 16:30:29') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

res = tn.parse(target=u'我需要大概33天2分钟四秒', timeBase='2013-02-28 16:30:29') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

res = tn.parse(target=u'今年儿童节晚上九点一刻') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

res = tn.parse(target=u'三日') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

res = tn.parse(target=u'7点4') # target为待分析语句，timeBase为基准时间默认是当前时间
print(res)

res = tn.parse(target=u'今年春分')
print(res)

res = tn.parse(target=u'7000万')
print(res)

res = tn.parse(target=u'7百')
print(res)

res = tn.parse(target=u'7千')
print(res)

## （3）反义词搜索

github url：https://github.com/liuhuanyong/ChineseAntiword

word = '天才'
antiwords:['庸才', '庸人', '蠢材']
word = '快乐'
antiwords:['悲伤', '伤心', '难过', '痛苦', '烦恼', '苦恼']
word = '和蔼'
antiwords:['凶狠', '凶残', '粗暴', '凶横', '凶恶', '严厉', '蛮横']
word = '批判'
antiwords:['表扬', '表彰', '赞颂']

## （4）地址名纠错
github_url:http://github.com/PyUnit/pyunit-address
