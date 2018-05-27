Apply powerful machine learning algorith to win the market

总结
- 在回测基准，采用的因子，对冲的benchmark，因子都是十档的情况下，lgb按年划分测试集的二分类效果在中性化之前和之后五年平均表现要优于其他模型。
- 其他的模型中，lgb回归超额收益的非中性化表现很好，但是中性化以后的年化收益比较低，由此可见回归任务模型受到涨跌度的影响比较大，粗颗粒的分类更好的避免了过拟合，初步认为分类模型在多因子选股上具有优势。
-  lgb滚动预测周期不同的情况下，72个月的数据预测后1个月的非行业中性表现好，但是行业中性之后没有按年滚动预测效果好。
- 本次研究的数据集仅仅是13-17年ZZ,HS 800只股票，可以说是绩优股，这种比较稳定的股票相对于其他支股票具有较稳定，低噪声，自相关性较大，更满足机器学习方法中i.i.d独立同分布的条件，一旦扩充到全A股，效果可能会变得不好。

Csv文件：

Dataset_1 （800支股票2007到2017的70个因子）

Dataset_factorRank10 （基于dataset_1的因子分档）

Dataset_2（800支股票2007到2018的70个因子）

Dataset2_factorRank10 （基于dataset_2的因子分档）

Lgb_roll_month （lgb月度二分类预测结果）

Lgb_year（lgb年度二分类预测结果）

Lgbr_abs（lgb回归绝对收益率结果）

Rfc10_2class（随机森林因子十档做二分类）

Rfr_active （随机森林回归超额收益率）

Stacking_xgb0524（xgb和lr做融合）

Xgb0524 （xgb单模型预测结果）

代码文件：

discreteFactor  （因子离散）

tune_para_lgb（贝叶斯调参）

lgb_roll_by_month （月度滚动预测）

lgb_roll_by_year （年度滚动预测）

MultiModel （多模型比较）

rfc10_2class （随机森林二分类）

plot_acc_auc_classifierModel （auc，acc曲线绘制）# factorsMerge


