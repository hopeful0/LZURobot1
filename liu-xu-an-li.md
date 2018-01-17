案例说明：

整数分解，又称质因子分解。在数学中，整数分解问题是指:给出一个正整数，将其写成几个素数的乘积。例如，给出45这个数，它可以分解成3^2×5。根据算术基本定理，这样的分解结果应该是独一无二的。这个问题在代数学、密码学、计算复杂性理论和量子计算机等领域中有重要意义。

利用blockly实现整数分解

思路：先对输入的正整数n进行是否质数的判断，若是质数，直接输出n=n×1。若是合数，就用它去除从2开始的自然数，找出第一个因数j，再使n=n÷j，重复刚才的步骤，直到n成为质数，即最大的因数，再输出所有因数。

模块展示：

![](/assets/刘旭案例模块1.png)

运行示例：

![](/assets/刘旭案例运行图1.png)

![](/assets/刘旭案例运行图2.png)

![](/assets/刘旭案例运行图3.png)

XML代码：

&lt;xml xmlns="http://www.w3.org/1999/xhtml"&gt;

  &lt;variables&gt;

    &lt;variable type="" id=".d?sxIUePWsm\[+F\[!l?\("&gt;a&lt;/variable&gt;

    &lt;variable type="" id="\*7JCe;3\*\#}p/\(=t.Pbt!"&gt;b&lt;/variable&gt;

    &lt;variable type="" id="\)\*My0O}?z$q\[J,IsqE9\|"&gt;c&lt;/variable&gt;

    &lt;variable type="" id="NrwG\|CuKSl-ke1?O@4\#\)"&gt;d&lt;/variable&gt;

    &lt;variable type="" id="e~TCdGNCokg;1WYc\)UrI"&gt;m&lt;/variable&gt;

    &lt;variable type="" id="!AIKEs?\`pMRtJgNKJYR?"&gt;数字&lt;/variable&gt;

    &lt;variable type="" id="ACl}?3;=eLOuNhd3X,F\)"&gt;n&lt;/variable&gt;

    &lt;variable type="" id="UJNd=m\[tJ77\[ra~T\#Xmp"&gt;i&lt;/variable&gt;

    &lt;variable type="" id="O1\]naO\[bD\[Y/4zW/pL\(\("&gt;项目&lt;/variable&gt;

    &lt;variable type="" id="d/oQ%C6gIk?t\]@nYcxdw"&gt;j&lt;/variable&gt;

  &lt;/variables&gt;

  &lt;block type="variables\_set" id="\`AR\|R=CoMg\[nY+eXA=4a" x="-87" y="-187"&gt;

    &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

    &lt;value name="VALUE"&gt;

      &lt;block type="text\_prompt\_ext" id="b\)q3IlT%U-2EHskQ8cvZ"&gt;

        &lt;mutation type="TEXT"&gt;&lt;/mutation&gt;

        &lt;field name="TYPE"&gt;TEXT&lt;/field&gt;

        &lt;value name="TEXT"&gt;

          &lt;shadow type="text" id="~~EMQ8n4-X8ZG\#gSHqo{"&gt;

            &lt;field name="TEXT"&gt;abc&lt;/field&gt;

          &lt;/shadow&gt;

        &lt;/value&gt;

      &lt;/block&gt;

    &lt;/value&gt;

    &lt;next&gt;

      &lt;block type="variables\_set" id="I+\[nT\[G}!Po?qt~Ui\[,e"&gt;

        &lt;field name="VAR" id=".d?sxIUePWsm\[+F\[!l?\(" variabletype=""&gt;a&lt;/field&gt;

        &lt;value name="VALUE"&gt;

          &lt;block type="variables\_get" id="\)MZY}g\[Q\[wSGV:Q0:N\#n"&gt;

            &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

          &lt;/block&gt;

        &lt;/value&gt;

        &lt;next&gt;

          &lt;block type="controls\_if" id="mp%05m0Ysxv9s5H.%fJ\["&gt;

            &lt;mutation else="1"&gt;&lt;/mutation&gt;

            &lt;value name="IF0"&gt;

              &lt;block type="math\_number\_property" id="1Y\`%lX9s\|GYn@vDby}sW"&gt;

                &lt;mutation divisor\_input="false"&gt;&lt;/mutation&gt;

                &lt;field name="PROPERTY"&gt;PRIME&lt;/field&gt;

                &lt;value name="NUMBER\_TO\_CHECK"&gt;

                  &lt;shadow type="math\_number" id=":U,8vx\*j.q\(\`LflW1yq3"&gt;

                    &lt;field name="NUM"&gt;0&lt;/field&gt;

                  &lt;/shadow&gt;

                  &lt;block type="variables\_get" id="I}0!Jol{o:ju+q-r\*yjW"&gt;

                    &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

              &lt;/block&gt;

            &lt;/value&gt;

            &lt;statement name="DO0"&gt;

              &lt;block type="text\_append" id="d:;aY1/ycu5{Ag\#w?@:1"&gt;

                &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                &lt;value name="TEXT"&gt;

                  &lt;shadow type="text" id="x?vnq9!mh2gHakELS1HO"&gt;

                    &lt;field name="TEXT"&gt;&lt;/field&gt;

                  &lt;/shadow&gt;

                  &lt;block type="text" id="sAu$A!aP?Cwq,bF99MZC"&gt;

                    &lt;field name="TEXT"&gt;=1\*&lt;/field&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

                &lt;next&gt;

                  &lt;block type="text\_append" id="\#GWF{{4}8EV\[p1\(i\[\#G\`"&gt;

                    &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                    &lt;value name="TEXT"&gt;

                      &lt;shadow type="text" id="wfJgnD,eNjeM@i;xa3\)d"&gt;

                        &lt;field name="TEXT"&gt;&lt;/field&gt;

                      &lt;/shadow&gt;

                      &lt;block type="variables\_get" id="E8euyEMw20WRkc\_lo\|p."&gt;

                        &lt;field name="VAR" id=".d?sxIUePWsm\[+F\[!l?\(" variabletype=""&gt;a&lt;/field&gt;

                      &lt;/block&gt;

                    &lt;/value&gt;

                    &lt;next&gt;

                      &lt;block type="text\_print" id="/OYw/uz-fdyKj8!.o=}/"&gt;

                        &lt;value name="TEXT"&gt;

                          &lt;shadow type="text" id=",,V~CHq\]!Z~\*OUKdYWS/"&gt;

                            &lt;field name="TEXT"&gt;abc&lt;/field&gt;

                          &lt;/shadow&gt;

                          &lt;block type="variables\_get" id="5L,ft$Z32S:?.\[qm{{\`j"&gt;

                            &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                      &lt;/block&gt;

                    &lt;/next&gt;

                  &lt;/block&gt;

                &lt;/next&gt;

              &lt;/block&gt;

            &lt;/statement&gt;

            &lt;statement name="ELSE"&gt;

              &lt;block type="variables\_set" id="\(\`G@WE9/G.o\_PIZi~T\*t"&gt;

                &lt;field name="VAR" id="\)\*My0O}?z$q\[J,IsqE9\|" variabletype=""&gt;c&lt;/field&gt;

                &lt;value name="VALUE"&gt;

                  &lt;block type="variables\_get" id="rb1$.iC:StYfEUdpfFx4"&gt;

                    &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                  &lt;/block&gt;

                &lt;/value&gt;

                &lt;next&gt;

                  &lt;block type="text\_append" id="-%u,\_JVP3SZaql0SZT\_O"&gt;

                    &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                    &lt;value name="TEXT"&gt;

                      &lt;shadow type="text" id="Q\*m{\)d4Xh95\_^$6fVrXd"&gt;

                        &lt;field name="TEXT"&gt;&lt;/field&gt;

                      &lt;/shadow&gt;

                      &lt;block type="text" id="G~\_ydwc0G;w4;U\_\*ClTP"&gt;

                        &lt;field name="TEXT"&gt;=&lt;/field&gt;

                      &lt;/block&gt;

                    &lt;/value&gt;

                    &lt;next&gt;

                      &lt;block type="variables\_set" id="fQDc=jsic\[0c2I\[o\*yRl"&gt;

                        &lt;field name="VAR" id="d/oQ%C6gIk?t\]@nYcxdw" variabletype=""&gt;j&lt;/field&gt;

                        &lt;value name="VALUE"&gt;

                          &lt;block type="math\_number" id="E:ZR\(ya$+dAA87V\#BNk\("&gt;

                            &lt;field name="NUM"&gt;2&lt;/field&gt;

                          &lt;/block&gt;

                        &lt;/value&gt;

                        &lt;next&gt;

                          &lt;block type="controls\_whileUntil" id="iYd4\]\_Q}Y-.LGyo\]\#jH\)"&gt;

                            &lt;field name="MODE"&gt;UNTIL&lt;/field&gt;

                            &lt;value name="BOOL"&gt;

                              &lt;block type="math\_number\_property" id="}9N1CP\_aqLh!y0\`BKtKx"&gt;

                                &lt;mutation divisor\_input="false"&gt;&lt;/mutation&gt;

                                &lt;field name="PROPERTY"&gt;PRIME&lt;/field&gt;

                                &lt;value name="NUMBER\_TO\_CHECK"&gt;

                                  &lt;shadow type="math\_number" id="jrZA0rah}+!h\(/RsRZO/"&gt;

                                    &lt;field name="NUM"&gt;0&lt;/field&gt;

                                  &lt;/shadow&gt;

                                  &lt;block type="variables\_get" id="\[yK\|zLa\(^4j3/9wvqU08"&gt;

                                    &lt;field name="VAR" id="\)\*My0O}?z$q\[J,IsqE9\|" variabletype=""&gt;c&lt;/field&gt;

                                  &lt;/block&gt;

                                &lt;/value&gt;

                              &lt;/block&gt;

                            &lt;/value&gt;

                            &lt;statement name="DO"&gt;

                              &lt;block type="controls\_if" id="\#\)2wP\_z:psCR:\*Z\(\[qfR"&gt;

                                &lt;mutation else="1"&gt;&lt;/mutation&gt;

                                &lt;value name="IF0"&gt;

                                  &lt;block type="math\_number\_property" id="K\(vl9\(W~YIj2T\|D\`%}9I"&gt;

                                    &lt;mutation divisor\_input="false"&gt;&lt;/mutation&gt;

                                    &lt;field name="PROPERTY"&gt;WHOLE&lt;/field&gt;

                                    &lt;value name="NUMBER\_TO\_CHECK"&gt;

                                      &lt;shadow type="math\_number" id="\|yVNeW-uj3u\*t}?Rb\_u$"&gt;

                                        &lt;field name="NUM"&gt;0&lt;/field&gt;

                                      &lt;/shadow&gt;

                                      &lt;block type="math\_arithmetic" id="K:E7T$n;DXMu:uv-/e:%"&gt;

                                        &lt;field name="OP"&gt;DIVIDE&lt;/field&gt;

                                        &lt;value name="A"&gt;

                                          &lt;shadow type="math\_number" id="\`-7Qh6t1A9{\_EhS;1ubj"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="variables\_get" id="-5yK4Scw.E\#mt2x;\)-Yn"&gt;

                                            &lt;field name="VAR" id="\)\*My0O}?z$q\[J,IsqE9\|" variabletype=""&gt;c&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                        &lt;value name="B"&gt;

                                          &lt;shadow type="math\_number" id="NTzEqk%+\)bioEUkbtlco"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="variables\_get" id="s\)0Fbqb$pTisR.\]/D@0U"&gt;

                                            &lt;field name="VAR" id="d/oQ%C6gIk?t\]@nYcxdw" variabletype=""&gt;j&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                      &lt;/block&gt;

                                    &lt;/value&gt;

                                  &lt;/block&gt;

                                &lt;/value&gt;

                                &lt;statement name="DO0"&gt;

                                  &lt;block type="variables\_set" id="\)0\*MK,RKo,8pE4HhK\`h9"&gt;

                                    &lt;field name="VAR" id="\)\*My0O}?z$q\[J,IsqE9\|" variabletype=""&gt;c&lt;/field&gt;

                                    &lt;value name="VALUE"&gt;

                                      &lt;block type="math\_arithmetic" id="{RGI1.$V6KqG{%{\)\|zqI"&gt;

                                        &lt;field name="OP"&gt;DIVIDE&lt;/field&gt;

                                        &lt;value name="A"&gt;

                                          &lt;shadow type="math\_number" id="\`-7Qh6t1A9{\_EhS;1ubj"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="variables\_get" id="yb?@BLw6\)EteE$1+^\_R~"&gt;

                                            &lt;field name="VAR" id="\)\*My0O}?z$q\[J,IsqE9\|" variabletype=""&gt;c&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                        &lt;value name="B"&gt;

                                          &lt;shadow type="math\_number" id="NTzEqk%+\)bioEUkbtlco"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="variables\_get" id="\]:.HKneFWt\({044~l!oi"&gt;

                                            &lt;field name="VAR" id="d/oQ%C6gIk?t\]@nYcxdw" variabletype=""&gt;j&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                      &lt;/block&gt;

                                    &lt;/value&gt;

                                    &lt;next&gt;

                                      &lt;block type="text\_append" id="\_m,}-bNzN$$xRL6SCi7@"&gt;

                                        &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                                        &lt;value name="TEXT"&gt;

                                          &lt;shadow type="text" id="fJn$Yvx2G\_r7\]OUwWd\(A"&gt;

                                            &lt;field name="TEXT"&gt;&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="variables\_get" id="CYbq%qyzcYn^y9\*e7JHB"&gt;

                                            &lt;field name="VAR" id="d/oQ%C6gIk?t\]@nYcxdw" variabletype=""&gt;j&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                        &lt;next&gt;

                                          &lt;block type="text\_append" id="rGI;L\]q6sJze/\*E45F$\["&gt;

                                            &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                                            &lt;value name="TEXT"&gt;

                                              &lt;shadow type="text" id="b+vEZS\];9%$w%?qVtejk"&gt;

                                                &lt;field name="TEXT"&gt;&lt;/field&gt;

                                              &lt;/shadow&gt;

                                              &lt;block type="text" id="ju-i~1tceG\(zLMNrwrur"&gt;

                                                &lt;field name="TEXT"&gt;\*&lt;/field&gt;

                                              &lt;/block&gt;

                                            &lt;/value&gt;

                                          &lt;/block&gt;

                                        &lt;/next&gt;

                                      &lt;/block&gt;

                                    &lt;/next&gt;

                                  &lt;/block&gt;

                                &lt;/statement&gt;

                                &lt;statement name="ELSE"&gt;

                                  &lt;block type="variables\_set" id="si\]Bq\(\#\*v}O9YXA=bCf\#"&gt;

                                    &lt;field name="VAR" id="d/oQ%C6gIk?t\]@nYcxdw" variabletype=""&gt;j&lt;/field&gt;

                                    &lt;value name="VALUE"&gt;

                                      &lt;block type="math\_arithmetic" id="\_48e\(X-BOdS{dpUf0c5\#"&gt;

                                        &lt;field name="OP"&gt;ADD&lt;/field&gt;

                                        &lt;value name="A"&gt;

                                          &lt;shadow type="math\_number" id="\`-7Qh6t1A9{\_EhS;1ubj"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="variables\_get" id="gX5^\_:l0}LfLDpdxh-}T"&gt;

                                            &lt;field name="VAR" id="d/oQ%C6gIk?t\]@nYcxdw" variabletype=""&gt;j&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                        &lt;value name="B"&gt;

                                          &lt;shadow type="math\_number" id="NTzEqk%+\)bioEUkbtlco"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/shadow&gt;

                                          &lt;block type="math\_number" id="3.ZC2mc7=}v:nsg/7^yG"&gt;

                                            &lt;field name="NUM"&gt;1&lt;/field&gt;

                                          &lt;/block&gt;

                                        &lt;/value&gt;

                                      &lt;/block&gt;

                                    &lt;/value&gt;

                                  &lt;/block&gt;

                                &lt;/statement&gt;

                              &lt;/block&gt;

                            &lt;/statement&gt;

                            &lt;next&gt;

                              &lt;block type="text\_append" id="^jT9\)g\|O,H3hrw~;2Qc\]"&gt;

                                &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

                                &lt;value name="TEXT"&gt;

                                  &lt;shadow type="text" id="fJn$Yvx2G\_r7\]OUwWd\(A"&gt;

                                    &lt;field name="TEXT"&gt;&lt;/field&gt;

                                  &lt;/shadow&gt;

                                  &lt;block type="variables\_get" id="~8KKVOy2p\]I4\[dk:,N\|x"&gt;

                                    &lt;field name="VAR" id="\)\*My0O}?z$q\[J,IsqE9\|" variabletype=""&gt;c&lt;/field&gt;

                                  &lt;/block&gt;

                                &lt;/value&gt;

                                &lt;next&gt;

                                  &lt;block type="text\_print" id="\_K\#sB+Yjp2\#9UT,PCh\|~"&gt;

                                    &lt;value name="TEXT"&gt;

                                      &lt;shadow type="text" id=",,V~CHq\]!Z~\*OUKdYWS/"&gt;

                                        &lt;field name="TEXT"&gt;abc&lt;/field&gt;

                                      &lt;/shadow&gt;

                                      &lt;block type="variables\_get" id="r8;YB5A6n$tR\`0cCUtgh"&gt;

                                        &lt;field name="VAR" id="!AIKEs?\`pMRtJgNKJYR?" variabletype=""&gt;数字&lt;/field&gt;

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

            &lt;/statement&gt;

          &lt;/block&gt;

        &lt;/next&gt;

      &lt;/block&gt;

    &lt;/next&gt;

  &lt;/block&gt;

&lt;/xml&gt;

