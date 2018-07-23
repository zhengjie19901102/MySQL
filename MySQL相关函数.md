## MySQL相关函数

### 单行函数
- 字符函数
	* lenght('xxxx') 获取字符**字节**数
	* concat([字段名],'xxx','xx') 拼接成字符串
	* upper('xxx')	字符串全部大写(对英文)
	* lower('xxx')	字符串全部小写(对英文)
	* substr(‘xxx’,[option])	从'xxx'字符串中从[option]开始截取字符，索引从**1**开始
	* 	substr(‘xxx’,[option],[length]) 从'xxx'字符串中从[option]开始截取字符，截取[length]长度，索引从**1**开始
	* substring()		截取**字符**长度
	* instr('xxxyyy','yyy')  用于返回'xxxyyy'中出现的'yyy'第一次出现的索引
	* trim(' xxxx  ')			用于去除的前后空格符
	* trim('x' from 'xccc xxxx  xxx') 	去掉前后的'x'字符
	* lpad('aaa',10,'[*]')	用'[*]'左填充指定长度(不足10，填充)
	* rpad('aaa',10,'[*]')	与lpad方向相反的填充
	* replace('xxxxyyy','xxx','aaa')  替换'xxxxyyy'中的xxx为aaa
- 数学函数
	* round(19.22) 四舍五入
	* round(19.232,22)	四舍五入保留两位小数
	* ceil(19.222) 	向上取整
	* floor(19.22)	向下取整
	* truncate(1.65,1)  小数点保留几位(这里为1为)
	* mod(10,3)	取模运算(10与3取模)
- 日期函数
	* now()	返回当前系统日期+时间
	* curdate()	返回当前系统日期，不包含时间
	* curtime()	返回当前时间，不包含日期
	* year([日期对象,例如传入now()])		返回年
	* month([日期对象,例如传入now()])	返回月
	* monthname([日期对象,例如传入now()])	返回月名
	* str_to_date('m-dd-yyyy','%Y-%c-%d') 将字符通过制定的格式转换成日期
	* date_format('2018-2-2','%Y/%c/%d') 	将日期转换成字符  ->  结果:`2018/2/2`
	<img src="img/pc.png"/>
- 其他函数
	* version()	查看数据库版本信息
	* database()	查看当前数据库
	* user()		查看当前用
- 流程控制函数
	* if(exp1,exp2,exp3)   如果exp1成立，则返回exp2,否则返回exp3
	* case 要判断的字段或表达式 when 常量1 then	结果1 when 常量2 then 结果2 ... else 结果N end 	类似java中的switch语句
	* 多重if:
		```
		case
			when 条件1 
			then 结果1
			when 条件2
			then 结果2
			else	
			结果n
		end
		```
		
### 分组函数