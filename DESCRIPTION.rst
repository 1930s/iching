          <div class="show-content">
<p></p><div class="image-package">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/I_Ching_Song_Dynasty_print.jpg/440px-I_Ching_Song_Dynasty_print.jpg"><br><div class="image-caption"></div>
</div>
<p>iching is a packge developed by Cheng-Jun Wang. It employs the method of Shicao prediction to reproduce the prediction of I Ching--the Book of Exchanges. The I Ching ([î tɕíŋ]; Chinese: 易經; pinyin: Yìjīng), also known as the Classic of Changes or Book of Changes in English, is an ancient divination text and the oldest of the Chinese classics.</p>
<p></p><div class="image-package">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a1/Yarrow_stalks_for_I_Ching.JPG/440px-Yarrow_stalks_for_I_Ching.JPG"><br><div class="image-caption"></div>
</div>
<p>The Zhou yi provided a guide to cleromancy that used the stalks of the yarrow plant, but it is not known how the yarrow stalks became numbers, or how specific lines were chosen from the line readings. In the hexagrams, broken lines were used as shorthand for the numbers 6 (六) and 8 (八), and solid lines were shorthand for values of 7 (七) and 9 (九). The Great Commentary contains a late classic description of a process where various numerological operations are performed on a bundle of 50 stalks, leaving remainders of 6 to 9.</p>
<p>大衍之数五十，其用四十有九。分而为二以象两，挂一以象三，揲之以四以象四时，归奇于扐以象闰。五岁再闰，故再扐而后挂。天一，地二；天三，地四；天五，地六；天七，地八；天九，地十。天数五，地数五。五位相得而各有合，天数二十有五，地数三十，凡天地之数五十有五，此所以成变化而行鬼神也。乾之策二百一十有六，坤之策百四十有四，凡三百六十，当期之日。二篇之策，万有一千五百二十，当万物之数也。是故四营而成《易》，十有八变而成卦，八卦而小成。引而伸之，触类而长之，天下之能事毕矣。显道神德行，是故可与酬酢，可与祐神矣。子曰：“知变化之道者，其知神之所为乎。”</p>
<h1>Install</h1>
<pre><code class="python">pip install iching</code></pre>
<h1>Use</h1>
<pre><code class="python">from iching import iching</code></pre>
<h5>0. Set iching time</h5>
<pre><code class="python">iching.ichingDate(1985052620150704) 
# e.g., 19850526 is your birthday and 20150704 is the prediction time.
# of course, your can also input more precise time.</code></pre>
<h5>1. Start to predict</h5>
<pre><code class="python">iching.getPredict()</code></pre>
<h5>2. Get the iching name</h5>
<pre><code class="python">fixPred, changePred   = iching.getPredict()
iching.ichingName(fixPred, changePred  )</code></pre>
<h5>3. Geth the iching text</h5>
<pre><code class="python">iching.ichingText(fixPred, iching)</code></pre>

<pre><code>坎卦原文坎。习坎，有孚，维心亨，行有尚。象曰：水洊至，习坎。君子以常德行，习教事。白话文解释习坎卦：
抓获俘虏，劝慰安抚他们，通泰。途中将得到帮助。《象辞》说：坎为永，水长流不滞，是坎卦的卦象。君子观此卦象，
从而尊尚德行，取法于细水长流之象，学习教化人民的方法。

《断易天机》解坎卦坎上坎下，为坎宫本位卦。坎为陷入、陷阱，为险难之境。此时应坚持信心，才能豁然贯通。

北宋易学家邵雍解艰难危险，重险重陷；事多困阻，谨慎行事。得此卦者，运气不佳，多难危险，事多困阻，宜谨言慎行，退守保安。</code></pre>
<h5>4. Understand Three Changes</h5>
<pre><code class="python">data = 50 - 1
sky, earth, firstChange, data = iching.getChange(data)
print sky, '\n', earth, '\n',firstChange, '\n', data

sky, earth, secondChange, data = iching.getChange(data)
print sky, '\n', earth, '\n',secondChange, '\n', data

sky, earth, thirdChange, data = iching.getChange(data)
print sky, '\n', earth, '\n',thirdChange, '\n', data</code></pre>
<h5>4. Plot transitions</h5>
<pre><code class="python">import matplotlib.pyplot as plt
fig = plt.figure(figsize=(15, 10),facecolor='white')
plt.subplot(2, 2, 1)
iching.plotTransition(10000, w = 50)
plt.subplot(2, 2, 2)
iching.plotTransition(10000, w = 50)
plt.subplot(2, 2, 3)
iching.plotTransition(10000, w = 50)
plt.subplot(2, 2, 4)
iching.plotTransition(10000, w = 50)</code></pre>
<p></p><div class="image-package">
<img src="http://7lrzgn.com1.z0.glb.clouddn.com/download.png"><br><div class="image-caption"></div>
</div>
</div>
        </div>
      </div>