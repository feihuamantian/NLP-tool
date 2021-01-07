# NLP-tool
github url: https://github.com/yongzhuo/Macropodus
About 自然语言处理工具Macropodus，基于Albert+BiLSTM+CRF深度学习网络架构，中文分词，词性标注，命名实体识别，新词发现，关键词，文本摘要，文本相似度，科学计算器，中文数字阿拉伯数字(罗马数字)转换，中文繁简转换，拼音转换。

时间转换工具：
github url : https://github.com/zhanzecheng/Time_NLP

pip install arrow==0.14.0
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

#
#
#
# def boson_analy(pattern, basetime):
#     nlp = BosonNLP('MWSY30Ja.14341.z39Al-kSksZt')
#     result = nlp.convert_time(
#         pattern,
#         datetime.datetime.today())
#     print (json.dumps(result))
#     return json.dumps(result)
#
# with open('C:/Users/zhm/Desktop/test.txt') as testfile:
#     data = []
#     for each in testfile:
#         res = tn.parse(each, arrow.now())
#         res_b = boson_analy(each, datetime.datetime.now())
#         data.append(each+'Boson:'+res_b+'\n'+'Time-NLP:'+res+'\n'+'\n')
# with open('C:/Users/zhm/Desktop/对比.txt', 'wb') as resfile:
#     resfile.writelines(data)
#
# ### 測試輸出文件


# with open('resource/holi_lunar.json') as file_1:
#     out = json.load(file_1)
#     print type(out)
# with open('resource/holi_lunar.json', 'w') as file_out:
#     print json.dumps(out, indent=2, ensure_ascii=False)
#     print >> file_out, json.dumps(out, indent=2, ensure_ascii=False).encode('utf-8')
#
# with open('resource/holi_lunar.json') as file_out:
#     print json.load(file_out)


# dset = []
# with open('C:/Users/zhm/Desktop/test.txt') as testfile:
#     for each in testfile:
#         dset.append(each)
#
# def run(query):
#     tn = TimeNormalizer()
#     res = tn.parse(target=query, timeBase='2013-02-28 16:30:29')
#     print res
# if __name__ == '__main__':
#     while True:
#        query = random.choice(dset)
#        lp = LineProfiler()
#        lp_wrapper = lp(run)
#        lp_wrapper(query)
#        lp.print_stats()
#        cProfile.run("run(query)")

# with open(os.path.dirname(__file__) + '/resource/regex.txt', 'wb') as f:
#     f.write(u'((前|昨|今|明|后)(天|日)?(早|晚)(晨|上|间)?)|(\\d+个?[年月日天][以之]?[前后])|(\\d+个?半?(小时|钟头|h|H))|(半个?(小时|钟头))|(\\d+(分钟|min))|([13]刻钟)|(


