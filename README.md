# ぷにぐらま～ずまにゅある

X680x0でプログラミング(主にアセンブリ言語)をする時に役立つと思われる資料をまとめたものです。

無保証につき、内容に関しては責任を負いません。各自の責任においてご利用ください。

半角文字と全角文字の幅の比が 1:2 の等幅フォントを前提にしています。

現在のところ転載は禁止します。AIを通した利用、またはAIによる加工は禁止します。


## 目次

* [assembler.txt](assembler.txt)
  * アセンブラマニュアル(HAS060 v3.09+91 対応)。
  * HAS.XやHAS060.Xの拡張部分の詳細についてはそれぞれのドキュメントを参照してください。
  * ColdFireに関しては省略しています。
* [bioswork.txt](bioswork.txt)
  * IOCSワークの一覧(ROM IOCS version 1.0～1.3 対応)。
  * システム代替ソフトウェアの作成用です。
* [code.txt](code.txt)
  * ANK文字コード表。
* [condition.txt](condition.txt)
  * 条件表(コンディションコード)。
* [doscall.txt](doscall.txt)
  * DOSコールレファレンス(Human68k version 3.02 対応)。
  * 返値の項にレジスタ名が表記されていないものは d0.l が使用されます。
* [fefunc.txt](fefunc.txt)
  * 浮動小数点演算ファンクションコールレファレンス(FLOAT V2 対応)。
  * ドライバの不具合動作については、その数が多いことや対象ファイルの種類が
    多いなどの理由で記述していません。
* [fpcall.txt](fpcall.txt)
  * かな漢字変換ファンクションコールレファレンス(ASK68K V2/V3 対応)。
* [fs_devdrv.txt](fs_devdrv.txt)
  * デバイスドライバ。
* [fs_ospatch.txt](fs_ospatch.txt)
  * ファイルシステムの処理ルーチンの解説(Human68k version 3.02 対応)。
  * 処理内容の解説は Human68k を解析した結果から推測しています。
    一部の用語は記述の都合上勝手に決めたものです。
* [iocscall.txt](iocscall.txt)
  * IOCSコールレファレンス(ROM IOCS version 1.0～1.3 対応)。
  * 返値の項にレジスタ名が表記されていないものは d0.l が使用されます。
    また、返値がないものでも d0.l は常に破壊されると考えて下さい。
* [kbdctrl.txt](kbdctrl.txt)
  * キーボード制御コマンドコード。
* [lang_c.txt](lang_c.txt)
  * C言語便利表。エスケープシーケンスと、演算子の優先順位と結合規則です。
* [mmio.txt](mmio.txt)
  * メモリマップドI/O一覧(X68000/X68030 対応)。
* [number.txt](number.txt)
  * 整数の表現範囲及び浮動小数点実数の形式。
* [oswork.txt](oswork.txt)
  * OSワークの一覧と各種の表の解説(Human68k version 3.02 対応)。
  * システム代替ソフトウェアの作成用です。
* [programmers.txt](programmers.txt)
  * メモリマップ等。一部内容は mmio.txt と重複します。
* [scsicall.txt](scsicall.txt)
  * SCSI IOCSコールレファレンス(ROM IOCS version 1.0～1.3 対応)。
  * 未公開コールはX68030のSCSI ROMを解析した結果を参考にしているので、
    誤りがあるかも知れません。
* [trap.txt](trap.txt)
  * trap例外処理マニュアル(ROM IOCS version 1.0～1.3、Human68k version 3.02 対応)。
* [vector.txt](vector.txt)
  * 割り込みベクタ一覧。
* [_fdformat.txt](_fdformat.txt)
  * フロッピーディスクのフォーマット表。
* [_mediabyte.txt](_mediabyte.txt)
  * メディアバイト表。filesystem.txt から抜き出しただけです。
* [appendix/devname.txt](appendix/devname.txt)
  * デバイス名の一覧。
* [appendix/io_board.txt](appendix/io_board.txt)
  * SHARP製I/Oボードの一覧。
* [appendix/memmap.txt](appendix/memmap.txt)
  * 拡張ボードのメモリマップ。


## 参考資料

* ROM
  * IOCS ROM version 1.0 (X68000 初代、1987-05-07版)
  * IOCS ROM version 1.0 (X68000 ACE)
  * IOCS ROM version 1.0 (X68000 SUPER)
  * IOCS ROM version 1.1 (X68000 XVI)
  * IOCS ROM version 1.2 (X68000 Compact XVI)
  * IOCS ROM version 1.3 (X68030)
  * IOCS ROM version 1.5 (060turbo、1997-05-29版)
* 書籍、雑誌
  * 68000プログラマーズ・ハンドブック (宍倉幸則、技術評論社)
  * プログラマーのためのX68000環境ハンドブック (吉沢正敏、市原昌文、工学社)
  * Inside X68000 (桑野雅彦、SOFT BANK)
  * Outside X68000 (桑野雅彦、SOFT BANK)
  * X68030 Inside/Out (桑野雅彦、SOFT BANK)
  * X68k Programming Series #0 X680x0 Develop. &amp; libc II
  * X68k Programming Series #1 X68000 Develop.
    Vol.1 Programmer's Guide (中村祐一(他)、SOFT BANK)
  * X68000マシン語プログラミング 入門編 (村田敏幸、SOFT BANK)
  * C COMPILER PRO-68K ver2.0 付属マニュアル (SHARP)
  * C COMPILER PRO-68K ver2.1 NEW KIT 付属マニュアル (SHARP)
  * X68000 XVI・XVI\[HD\] 取扱説明書 (SHARP)
  * プログラミング言語C 第二版 (B.W.カーニハン、D.M.リッチー、石田晴久訳、共立出版)
  * Oh!X(各種記事) (村田敏幸(他)、SOFT BANK)
* Human68kファイル
  * HUMAN.SYS (Human68k version 3.02) (SHARP/Hudson)
  * PRNDRV*.SYS (version 1.00～1.03) (SHARP/Hudson)
  * FDDEVICE.X (version 1.00) (SHARP/Hudson)
  * IOCS.X (version 1.50) (SHARP)
  * FLOAT2.X (version 2.03) (SHARP)
  * FLOAT3.X (version 2.03) (SHARP)
  * FLOAT4.X (version 1.02) (SHARP)
  * OPMDRV3.X (version 1.11) (SHARP/Luvex)
  * GPIBDRV.SYS version 1.00 (SHARP)
* SCSI資料
  * Mach-2 取扱説明書 (満開製作所)
  * SX-68SC 取扱説明書 (SYSTEM SACOM)
  * sse_121a.lzh (SUSIE.X V1.21A) (GORRY)
  * 1989_SCSI_Product_Guide.pdf (Fujitsu Microelectronics, Inc.)
  * MB89352.pdf
* その他のハードウェア
  * Nereid for X680x0 取扱説明書 (X-PowerStation)
  * PSX16750 関係のドキュメント (東野伸之)
* フリーソフトウェア等
  * アセンブラ
    * has309.lzh (HAS.X versin 3.09) (中村祐一)
    * has06091.lzh hassrc91.lzh (HAS060.X version 3.09+91) (M.Kamada)
  * 9scset.lzh (9SCDRV.X v3.14+2) (6no8rou)
  * tw136c14.lzh (TwentyOne Ver 1.36c+14) (T.Kawamoto、GORRY)
  * hiocssrc.lzh (HIOCS.X version 1.10+16) (中村祐一)
  * disktut2.lzh (清十郎)
  * knjtut02.lzh (清十郎、シロ)
  * 060turbo.sys (version 0.54～0.60) (鎌田誠)
  * cutils14.tgz (cutils 1.4 - cinfo) (Sandro Sigala)
  * eb007.lzh (EB.X version 0.07) (Shi-MAD.)
  * zm302a_s.lzh (Z-MUSIC version 3.02A) (ZENJI SOFT)
  * mndrv100.zip (mndrv version 1.00) (S.Tsuyuzaki)
  * merv4set.lzh (山内千里)
  * gmoji14.lzh (GMoji V1.4) (AIG-Soft)
* ドキュメント類
  * ASMDAT03.DOC (鎌田誠)
  * callhelp.lzh (Epsilon他)
  * iocscall.lzh (著者不明)
  * HUMAN.DOC、FCB.DOC (著者不明)
  * X30_SYSPORT.DOC、X68_SRAM.DOC、X68_VECTOR.DOC (著者失念)

(順不同、敬称略)


## その他

現在はGitHubでホスティングして細かく改訂しているためバージョン番号での区分を
していませんが、あえてバージョニングするなら「第八版 第Ｘ刷」となります。

古いバージョンについては再配布を控えていただけると幸いです。

TcbnErikが死亡した場合、有志によりメンテナンスを引き継いでもかまいません。


## Author

TcbnErik  /  https://github.com/kg68k/puni
