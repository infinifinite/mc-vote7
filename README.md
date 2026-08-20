# mc-vote7

<img width="1836" height="609" alt="image" src="https://github.com/user-attachments/assets/ed59e196-5ebb-4b74-84c0-b3db50943d36" />

Minecraftのレッドストーンで投票を行う回路と、「みんなもっと回路に詳しくなろう!」ということでその解説を含むワールドを作りました。**回路説明がメインです**。

7入力のスペックですが、実際に使うならもう少し取り回しを良くするべきかと思います。

回路部分は説明を単純にするためリピーターとトーチ、ダストのみで構成しており、横にあるMinecraft論理回路の基礎説明と対応します。

論理回路そのもの(NOTやANDゲート等)やMinecraftの個々の要素についての詳細な説明はありません。トーチとリピーターの基礎性質(反転と遅延)であることは知っている前提で説明書きがされています。

含まれる説明は以下の通りです:

1. エッジ検出とパルス信号
2. クロック回路
3. リピーターのロック
4. トグルフリップフロップ
5. 2進カウンタ

細かい話:

この回路は配信でAIが最初の方に提案したと思われるレバー(ボタン?)1つに対してカウンタを1ずつ加算する方式のカウンタ部分を実装したものです。

<img width="557" height="544" alt="image" src="https://github.com/user-attachments/assets/d71ce778-7522-4564-b0d3-5f45a0e46978" />

加算器とこの回路の大きな違いは、加算器は入力に対して出力が一意に定まるのに対し、この回路は値を保持するため入力が同じでも保持している値が同じでなければ出力が異なります。(計算機的には前者は純粋な論理回路、後者は状態機械と言えるのかは専門でもなんでもないのでよくわかりません。)

また、投票レバーそれぞれに個別の配線は必要なく、人数が多くても単に数珠つなぎにできるのでかさばりづらいかと思います。(SCSI的)

WDL: https://drive.google.com/drive/folders/1W0WrjNyHgFeo-DBkGRACIH7jUp4pCT_u?usp=sharing \
バージョンはJE26.2です。

---

なお資源が十分なら上のワールドにある回路は下ぐらいコンパクトにできます(追記: ワールドに追加しました)

<img width="1395" height="592" alt="スクリーンショット 2026-08-20 152411" src="https://github.com/user-attachments/assets/d1a1a87c-93f8-4afc-ac62-269b9253ca17" />
<img width="1067" height="468" alt="スクリーンショット 2026-08-20 152419" src="https://github.com/user-attachments/assets/5665bdba-1f66-454f-b029-5cb373e34041" />

---

追記:

音がならないレバー\
音符ブロックは上に何らかのブロックがあると音がなりません。右クリックは音が鳴らなくともオブサーバーで検知可能です。

<img width="473" height="401" alt="スクリーンショット 2026-08-20 145307" src="https://github.com/user-attachments/assets/244cdd7b-6080-43ff-824e-85eb70711a23" />
<img width="441" height="504" alt="スクリーンショット 2026-08-20 145315" src="https://github.com/user-attachments/assets/4d0a6a25-3955-4cb7-8312-6bea9ec2e410" />

自動作業台の背中側はOn/Offを見た目で区別できます。光源ではないので覗かないとわかりません。

RSランプなら光が漏れないように遮光ガラスを使うか、上に松明を置くのでもいいかもしれません。

---

あと3入力の過半数2の回路はこんな感じで組めました。ランプ側のはぐれレバーは出力表示のオンオフです

<img width="946" height="562" alt="スクリーンショット 2026-08-20 130340" src="https://github.com/user-attachments/assets/2179ee33-f844-42b3-8896-4ac80e65a31f" />
<img width="874" height="441" alt="スクリーンショット 2026-08-20 130331" src="https://github.com/user-attachments/assets/fa62b5a1-595f-42b5-b77e-b8a9804404cd" />
