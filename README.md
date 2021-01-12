# MagiaRecord-MentalStrengthening-Calculator

you need sth to run .ipynb

need sth like 精神强化模拟器（中文） https://mrtop.top/mr/chara/#/t (精神强化 - 魔法纪录中文Wiki https://magireco.moe/wiki/%E7%B2%BE%E7%A5%9E%E5%BC%BA%E5%8C%96) to see the tree

need a file to record the tree and the weight you set. I use Microsoft Excel to produce csv file. Python Numpy will read the file and produce data

data=

[
['123',4],['5607',8]
]

it means 2 plots, in 1st branch\ 2nd branch\ 3rd branch there is a subplot you give weight of 4, in 5th branch\ 6th branch there is no more branch, only a subplot, so 0, after that there is a 7th branch you set weight of 8.

0 to 9 are just marks, just a letter in str, no math here. use anything for free

8 > 4, so if you SB(data,'',1,9999), it will point '5607', if you SB(data,'',2,9999), it will point both

9999 is a special weight it means skip this plot. if you SB(data,'',1,9999), it points '5607', then, you have ['5',9999],['56',9999],['560',9999] otherwise the code will not reach '5607'.

SB(data,'',???,9999) is to search whole tree, SB(data,'56',???,''the weight of 56'') is to search trees under '56' subplot

a PC needs 10 min to calculate 4 branches such as Sayaka https://mrtop.top/mr/chara/#/2004/e/, but be impossible to calculate 6 branches such as Iroha https://mrtop.top/mr/chara/#/1001/e/ since the code is not efficient in sth, that is, it is not very smart. Run a dlc in it to merge branch 1 and 4, 2 and 5, 3 and 6 to reduce the wordload.

2GB memory recommended 

it provides a feature to random try to find better. In old version, it can not solve any so has this feature, now no need. But you can try run it (change some number to fit certain tree) since it doesnt require much memory. The basic thinking is to calculate each branch, and random 60 points to each branch, then calculate then repeat. With this, you can fix the code although the code is not user friendly. 500000 tries can be near the best i guess.
