**柏江山blockly程序**

---

这次我写的程序是求两个数的最大公约数与最小公倍数。因为小学时总用辗转相除法或短除法求两个数的最大公约数与最小公倍数，觉得非常麻烦，因此我想写个程序，直接把两个数字输入之后，立刻得到它们的最大公约数与最小公倍数，具体程序设计如下：

![](/assets/2.JPG)

然后执行程序，分别按照我编辑好的说明，输入第一个、第二个数字，就会显示出这两个数的最大公约数与最小公倍数

![](/assets/3.JPG)

![](/assets/4.JPG)

![](/assets/5.JPG)

![](/assets/6.JPG)![](/assets/10.JPG)![](/assets/245.JPG)

**可再取两个数字进行验证，这次取11与3**

![](/assets/5.JPG)![](/assets/344.JPG)

![](/assets/7.JPG)

![](/assets/33.JPG)

由此可证明这个程序是完全无错的。

XML代码：

&lt;xml xmlns="[http://www.w3.org/1999/xhtml"&gt](http://www.w3.org/1999/xhtml"&gt);

&lt;variables&gt;

```
&lt;variable type="" id=",\[QWdnt0HD+;EE\|\_t?Zm"&gt;x&lt;/variable&gt;

&lt;variable type="" id="\(,LYi:yr\*$QobOq%!HT}"&gt;{textVariable}&lt;/variable&gt;

&lt;variable type="" id="\)\#@v.tv,\|n5{;L\)M{.p:"&gt;m&lt;/variable&gt;

&lt;variable type="" id="K\*7d\#n8D\(CU/NHbSJ\#b,"&gt;n&lt;/variable&gt;

&lt;variable type="" id="-T/z.VZy3fY@w{zUH=81"&gt;c&lt;/variable&gt;

&lt;variable type="" id=".\(6\[E$HkU\)\#\[X\|!2@@cC"&gt;q&lt;/variable&gt;

&lt;variable type="" id="@2hTW%\_l\#R+/Af$M=^6%"&gt;temp&lt;/variable&gt;

&lt;variable type="" id="Oaza.YT=q\_iO\]e:Qb/;1"&gt;r&lt;/variable&gt;

&lt;variable type="" id="wrnDoEoDPvE=\_u3cQq\)l"&gt;p&lt;/variable&gt;
```

&lt;/variables&gt;

&lt;block type="variables\_set" id="~fQ@yINikVBCm95d\)tT@" x="-488" y="-412"&gt;

    &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

    &lt;value name="VALUE"&gt;

      &lt;block type="text\_prompt\_ext" id="W4th4RxJNco0Mvty\|88\`"&gt;

        &lt;mutation type="NUMBER"&gt;&lt;/mutation&gt;

        &lt;field name="TYPE"&gt;NUMBER&lt;/field&gt;

        &lt;value name="TEXT"&gt;

          &lt;shadow type="text" id="ZSWI\|S~+o2\#1@R\`xJUOw"&gt;

            &lt;field name="TEXT"&gt;1&lt;/field&gt;

          &lt;/shadow&gt;

          &lt;block type="text" id="8tVnRf{D@j4!%\[Wg-0e\`"&gt;

            &lt;field name="TEXT"&gt;请输入第一个数字&lt;/field&gt;

          &lt;/block&gt;

        &lt;/value&gt;

      &lt;/block&gt;

    &lt;/value&gt;

    &lt;next&gt;

      &lt;block type="variables\_set" id="CA/.C3i^opgM\)B+E@t%O"&gt;

        &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

        &lt;value name="VALUE"&gt;

          &lt;block type="text\_prompt\_ext" id="}}~ovUFrBrId.4\`jV8Oz"&gt;

            &lt;mutation type="NUMBER"&gt;&lt;/mutation&gt;

            &lt;field name="TYPE"&gt;NUMBER&lt;/field&gt;

            &lt;value name="TEXT"&gt;

              &lt;shadow type="text" id="m\*^$G$Rk!\`m\[!bjOK\(-l"&gt;

                &lt;field name="TEXT"&gt;2&lt;/field&gt;

              &lt;/shadow&gt;

              &lt;block type="text" id="WG^,/lnQ:fgkpKFz+{R\["&gt;

                &lt;field name="TEXT"&gt;请输入第二个数字&lt;/field&gt;

              &lt;/block&gt;

            &lt;/value&gt;

          &lt;/block&gt;

        &lt;/value&gt;

        &lt;next&gt;

          &lt;block type="controls\_if" id="yGH+;d$QuqP11a2c~U9~"&gt;

            &lt;value name="IF0"&gt;

              &lt;block type="logic\_compare" id=":^.\#R3p\[-P\]^\#KFCv7}\["&gt;

                &lt;field name="OP"&gt;LT&lt;/field&gt;

                &lt;value name="A"&gt;

                  &lt;block type="variables\_get" id="\_vfkAt?Hwh=\#SeGfGmrJ"&gt;

                    &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

                &lt;value name="B"&gt;

                  &lt;block type="variables\_get" id="qpk%4Nt1HUpsfo\#}XKXO"&gt;

                    &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

              &lt;/block&gt;

            &lt;/value&gt;

            &lt;statement name="DO0"&gt;

              &lt;block type="variables\_set" id="DOPSTs0%UdXhrm{jCp+J"&gt;

                &lt;field name="VAR" id="@2hTW%\_l\#R+/Af$M=^6%" variabletype=""&gt;temp&lt;/field&gt;

                &lt;value name="VALUE"&gt;

                  &lt;block type="variables\_get" id="0\#-a:-I\_k8mV\|rKk+}th"&gt;

                    &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

                &lt;next&gt;

                  &lt;block type="variables\_set" id="ox\_1B1A@P}J29\`\*RgfZj"&gt;

                    &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                    &lt;value name="VALUE"&gt;

                      &lt;block type="variables\_get" id="@\(3@KF$P248\*l/elh\`cx"&gt;

                        &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                      &lt;/block&gt;

                    &lt;/value&gt;

                    &lt;next&gt;

                      &lt;block type="variables\_set" id="+:XJviD5hlnV3vDN.=jd"&gt;

                        &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                        &lt;value name="VALUE"&gt;

                          &lt;block type="variables\_get" id="8igtNGuqBmyhh3,m5N!n"&gt;

                            &lt;field name="VAR" id="@2hTW%\_l\#R+/Af$M=^6%" variabletype=""&gt;temp&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                        &lt;next&gt;

                          &lt;block type="variables\_set" id="-DYQ\*a\`7Zvbn\[02i=\]T+"&gt;

                            &lt;field name="VAR" id="wrnDoEoDPvE=\_u3cQq\)l" variabletype=""&gt;p&lt;/field&gt;

                            &lt;value name="VALUE"&gt;

                              &lt;block type="math\_arithmetic" id="CdF!DxN\`U\#4=lIh^WI:G"&gt;

                                &lt;field name="OP"&gt;MULTIPLY&lt;/field&gt;

                                &lt;value name="A"&gt;

                                  &lt;shadow type="math\_number" id="HayXxp=I5MW~3h\(8FAW;"&gt;

                                    &lt;field name="NUM"&gt;1&lt;/field&gt;

                                  &lt;/shadow&gt;

                                  &lt;block type="variables\_get" id="M\`v=RN4-s-tRx$O\[9T\*a"&gt;

                                    &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                                  &lt;/block&gt;

                                &lt;/value&gt;

                                &lt;value name="B"&gt;

                                  &lt;shadow type="math\_number" id="\|mABypa~KQ9IP+?\)p\*,J"&gt;

                                    &lt;field name="NUM"&gt;1&lt;/field&gt;

                                  &lt;/shadow&gt;

                                  &lt;block type="variables\_get" id="uJvsu2?TAX6db5e\|lPYm"&gt;

                                    &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                                  &lt;/block&gt;

                                &lt;/value&gt;

                              &lt;/block&gt;

                            &lt;/value&gt;

                          &lt;/block&gt;

                        &lt;/next&gt;

                      &lt;/block&gt;

                    &lt;/next&gt;

                  &lt;/block&gt;

                &lt;/next&gt;

              &lt;/block&gt;

            &lt;/statement&gt;

            &lt;next&gt;

              &lt;block type="controls\_whileUntil" id="GuI3q@\(ge@h^\(\|8/q\`%\)"&gt;

                &lt;field name="MODE"&gt;WHILE&lt;/field&gt;

                &lt;value name="BOOL"&gt;

                  &lt;block type="logic\_compare" id="6cqxG\`3$Fr$EDYlS%F,\`"&gt;

                    &lt;field name="OP"&gt;NEQ&lt;/field&gt;

                    &lt;value name="A"&gt;

                      &lt;block type="variables\_get" id="1A!;Xd\*xSn^Z%%9od\[y\]"&gt;

                        &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                      &lt;/block&gt;

                    &lt;/value&gt;

                    &lt;value name="B"&gt;

                      &lt;block type="math\_number" id="j+\_OBuih7-juXI=-NDoV"&gt;

                        &lt;field name="NUM"&gt;0&lt;/field&gt;

                      &lt;/block&gt;

                    &lt;/value&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

                &lt;statement name="DO"&gt;

                  &lt;block type="variables\_set" id="?LlTyuZe7HKw~BgbvTOU"&gt;

                    &lt;field name="VAR" id="Oaza.YT=q\_iO\]e:Qb/;1" variabletype=""&gt;r&lt;/field&gt;

                    &lt;value name="VALUE"&gt;

                      &lt;block type="math\_modulo" id="\(P4RR}AQw\(GAx{zXXw\|K"&gt;

                        &lt;value name="DIVIDEND"&gt;

                          &lt;shadow type="math\_number" id="CLa\_$-g4.\(!02Hg$s0Tm"&gt;

                            &lt;field name="NUM"&gt;64&lt;/field&gt;

                          &lt;/shadow&gt;

                          &lt;block type="variables\_get" id="6GE4Doo0k\*-OQ\*iPtCe{"&gt;

                            &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                        &lt;value name="DIVISOR"&gt;

                          &lt;shadow type="math\_number" id="c2\#2Lm\]Eg2kH\]:bjx-Vl"&gt;

                            &lt;field name="NUM"&gt;10&lt;/field&gt;

                          &lt;/shadow&gt;

                          &lt;block type="variables\_get" id="\]\*%ec+N@oxck!X3eo\]w$"&gt;

                            &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                      &lt;/block&gt;

                    &lt;/value&gt;

                    &lt;next&gt;

                      &lt;block type="variables\_set" id="7gC~9Zwfn\)fdV\(5SUb93"&gt;

                        &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                        &lt;value name="VALUE"&gt;

                          &lt;block type="variables\_get" id="QR}DQiNG\`b/%lXuW6H/v"&gt;

                            &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                        &lt;next&gt;

                          &lt;block type="variables\_set" id="eg0\|QWA\#N}%.a\#m\#pB+F"&gt;

                            &lt;field name="VAR" id="\)\#@v.tv,\|n5{;L\)M{.p:" variabletype=""&gt;m&lt;/field&gt;

                            &lt;value name="VALUE"&gt;

                              &lt;block type="variables\_get" id="ad-c%d,\[\_\(I%Z}J::\)B6"&gt;

                                &lt;field name="VAR" id="Oaza.YT=q\_iO\]e:Qb/;1" variabletype=""&gt;r&lt;/field&gt;

                              &lt;/block&gt;

                            &lt;/value&gt;

                          &lt;/block&gt;

                        &lt;/next&gt;

                      &lt;/block&gt;

                    &lt;/next&gt;

                  &lt;/block&gt;

                &lt;/statement&gt;

                &lt;next&gt;

                  &lt;block type="text\_print" id="o\]x~~seN\#O~Om+\`qciIm"&gt;

                    &lt;value name="TEXT"&gt;

                      &lt;shadow type="text" id="q.x}INtM@%p.SPP7!o\[I"&gt;

                        &lt;field name="TEXT"&gt;它们的最大公约数是&lt;/field&gt;

                      &lt;/shadow&gt;

                    &lt;/value&gt;

                    &lt;next&gt;

                      &lt;block type="text\_print" id="s^\*\)@i\*:Vzpb;/TXt4HR"&gt;

                        &lt;value name="TEXT"&gt;

                          &lt;shadow type="text" id="!h\[^5\#,\)jyF\#e?m/LhE@"&gt;

                            &lt;field name="TEXT"&gt;abc&lt;/field&gt;

                          &lt;/shadow&gt;

                          &lt;block type="variables\_get" id="\(UbjO%Hg\[-AF,!\#c%iy\#"&gt;

                            &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                        &lt;next&gt;

                          &lt;block type="text\_print" id=".;l+pQ!\*\(ho^hoUAdU41"&gt;

                            &lt;value name="TEXT"&gt;

                              &lt;shadow type="text" id="w9A:FTy\#jk?P8bEpw\]+s"&gt;

                                &lt;field name="TEXT"&gt;它们的最小公倍数是&lt;/field&gt;

                              &lt;/shadow&gt;

                            &lt;/value&gt;

                            &lt;next&gt;

                              &lt;block type="variables\_set" id="\[N;Hiuh{;KBH^/pdMfNG"&gt;

                                &lt;field name="VAR" id=".\(6\[E$HkU\)\#\[X\|!2@@cC" variabletype=""&gt;q&lt;/field&gt;

                                &lt;value name="VALUE"&gt;

                                  &lt;block type="math\_arithmetic" id="bqZVVzF^j7iYV%umdcOL"&gt;

                                    &lt;field name="OP"&gt;DIVIDE&lt;/field&gt;

                                    &lt;value name="A"&gt;

                                      &lt;shadow type="math\_number" id="gwWs;\[ld;ChG\[\_~,ipF}"&gt;

                                        &lt;field name="NUM"&gt;1&lt;/field&gt;

                                      &lt;/shadow&gt;

                                      &lt;block type="variables\_get" id="E\)tA\_6eafOi\#d:Zri\`vy"&gt;

                                        &lt;field name="VAR" id="wrnDoEoDPvE=\_u3cQq\)l" variabletype=""&gt;p&lt;/field&gt;

                                      &lt;/block&gt;

                                    &lt;/value&gt;

                                    &lt;value name="B"&gt;

                                      &lt;shadow type="math\_number" id="fwA.bc$dc\)8ea%m@XUP\*"&gt;

                                        &lt;field name="NUM"&gt;1&lt;/field&gt;

                                      &lt;/shadow&gt;

                                      &lt;block type="variables\_get" id="\#K~Kc.0B\({Q\_k\_Cfc;Ww"&gt;

                                        &lt;field name="VAR" id="K\*7d\#n8D\(CU/NHbSJ\#b," variabletype=""&gt;n&lt;/field&gt;

                                      &lt;/block&gt;

                                    &lt;/value&gt;

                                  &lt;/block&gt;

                                &lt;/value&gt;

                                &lt;next&gt;

                                  &lt;block type="text\_print" id="L\_cxZz4-^uo\#eLe=e%G!"&gt;

                                    &lt;value name="TEXT"&gt;

                                      &lt;shadow type="text" id="K!v^\)\_1S\|\|8\]9tX0xf1u"&gt;

                                        &lt;field name="TEXT"&gt;abc&lt;/field&gt;

                                      &lt;/shadow&gt;

                                      &lt;block type="variables\_get" id="JE\#=Nw2\#Y9.Fxgc;yNKb"&gt;

                                        &lt;field name="VAR" id=".\(6\[E$HkU\)\#\[X\|!2@@cC" variabletype=""&gt;q&lt;/field&gt;

                                      &lt;/block&gt;

                                    &lt;/value&gt;

                                  &lt;/block&gt;

                                &lt;/next&gt;

                              &lt;/block&gt;

                            &lt;/next&gt;

                          &lt;/block&gt;

                        &lt;/next&gt;

                      &lt;/block&gt;

                    &lt;/next&gt;

                  &lt;/block&gt;

                &lt;/next&gt;

              &lt;/block&gt;

            &lt;/next&gt;

          &lt;/block&gt;

        &lt;/next&gt;

      &lt;/block&gt;

    &lt;/next&gt;

&lt;/block&gt;

&lt;/xml&gt;

