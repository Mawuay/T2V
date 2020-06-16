# T2V
This report details the Senior Design project proposal of Team 13, T2V, composed of Daniel Ackuaku, Hamilton Mutschler, Drew Smits, and Kevin Um. The proposed project is the design of a working prototype for a communication system between vehicle and traffic infrastructure for the improvement of traffic throughput and safety. The design consists of an interface for both vehicle and traffic infrastructure that would allow communication over Bluetooth. The location of each vehicle is determined by the traffic infrastructure via RFID readers and compatible RFID tags so that traffic flow can be controlled intelligently.
Due to the unprecedented circumstances regarding the COVID-19 pandemic, the second half of our spring semester was restricted in which our team could not meet in person and had no access to Calvin University’s Engineering Building.  Because of this, the scope of the project had to be reduced. However, our team successfully displayed a working prototype of a fully autonomous figure-8 intersection through numerous online meetings and remote work.


<!--
/* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{mso-style-unhide:no;
	mso-style-qformat:yes;
	mso-style-parent:"";
	margin:0in;
	margin-bottom:.0001pt;
	line-height:115%;
	mso-pagination:widow-orphan;
	font-size:12.0pt;
	font-family:"Times New Roman",serif;
	mso-fareast-font-family:"Times New Roman";
	mso-ansi-language:EN;}
h1
	{mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-qformat:yes;
	mso-style-link:"Heading 1 Char";
	mso-style-next:Normal;
	margin-top:20.0pt;
	margin-right:0in;
	margin-bottom:6.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	mso-outline-level:1;
	font-size:18.0pt;
	font-family:"Roboto Light";
	mso-fareast-font-family:"Roboto Light";
	mso-bidi-font-family:"Roboto Light";
	mso-font-kerning:0pt;
	mso-ansi-language:EN;
	font-weight:normal;}
h2
	{mso-style-priority:9;
	mso-style-qformat:yes;
	mso-style-link:"Heading 2 Char";
	mso-style-next:Normal;
	margin:0in;
	margin-bottom:.0001pt;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	mso-outline-level:2;
	font-size:14.0pt;
	font-family:"Times New Roman",serif;
	mso-ansi-language:EN;
	font-weight:normal;
	font-style:italic;
	mso-bidi-font-style:normal;}
h3
	{mso-style-priority:9;
	mso-style-qformat:yes;
	mso-style-link:"Heading 3 Char";
	mso-style-next:Normal;
	margin-top:16.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	mso-outline-level:3;
	font-size:12.0pt;
	font-family:"Times New Roman",serif;
	color:#434343;
	mso-ansi-language:EN;
	font-weight:normal;
	font-style:italic;
	mso-bidi-font-style:normal;}
h4
	{mso-style-priority:9;
	mso-style-qformat:yes;
	mso-style-link:"Heading 4 Char";
	mso-style-next:Normal;
	margin-top:14.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	mso-outline-level:4;
	font-size:12.0pt;
	font-family:"Times New Roman",serif;
	color:#666666;
	mso-ansi-language:EN;
	font-weight:normal;}
h5
	{mso-style-noshow:yes;
	mso-style-priority:9;
	mso-style-qformat:yes;
	mso-style-link:"Heading 5 Char";
	mso-style-next:Normal;
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	mso-outline-level:5;
	font-size:11.0pt;
	font-family:"Times New Roman",serif;
	color:#666666;
	mso-ansi-language:EN;
	font-weight:normal;}
h6
	{mso-style-noshow:yes;
	mso-style-priority:9;
	mso-style-qformat:yes;
	mso-style-link:"Heading 6 Char";
	mso-style-next:Normal;
	margin-top:12.0pt;
	margin-right:0in;
	margin-bottom:4.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	mso-outline-level:6;
	font-size:11.0pt;
	font-family:"Times New Roman",serif;
	color:#666666;
	mso-ansi-language:EN;
	font-weight:normal;
	font-style:italic;
	mso-bidi-font-style:normal;}
p.MsoTitle, li.MsoTitle, div.MsoTitle
	{mso-style-priority:10;
	mso-style-unhide:no;
	mso-style-qformat:yes;
	mso-style-link:"Title Char";
	mso-style-next:Normal;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:3.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	font-size:26.0pt;
	font-family:"Times New Roman",serif;
	mso-fareast-font-family:"Times New Roman";
	mso-ansi-language:EN;}
p.MsoSubtitle, li.MsoSubtitle, div.MsoSubtitle
	{mso-style-priority:11;
	mso-style-unhide:no;
	mso-style-qformat:yes;
	mso-style-link:"Subtitle Char";
	mso-style-next:Normal;
	margin-top:0in;
	margin-right:0in;
	margin-bottom:16.0pt;
	margin-left:0in;
	line-height:115%;
	mso-pagination:widow-orphan lines-together;
	page-break-after:avoid;
	font-size:15.0pt;
	font-family:"Arial",sans-serif;
	mso-fareast-font-family:Arial;
	color:#666666;
	mso-ansi-language:EN;}
span.Heading1Char
	{mso-style-name:"Heading 1 Char";
	mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:"Heading 1";
	mso-ansi-font-size:18.0pt;
	mso-bidi-font-size:18.0pt;
	font-family:"Roboto Light";
	mso-ascii-font-family:"Roboto Light";
	mso-fareast-font-family:"Roboto Light";
	mso-hansi-font-family:"Roboto Light";
	mso-bidi-font-family:"Roboto Light";}
span.Heading2Char
	{mso-style-name:"Heading 2 Char";
	mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:"Heading 2";
	mso-ansi-font-size:14.0pt;
	mso-bidi-font-size:14.0pt;
	font-style:italic;
	mso-bidi-font-style:normal;}
span.Heading3Char
	{mso-style-name:"Heading 3 Char";
	mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:"Heading 3";
	color:#434343;
	font-style:italic;
	mso-bidi-font-style:normal;}
span.Heading4Char
	{mso-style-name:"Heading 4 Char";
	mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:"Heading 4";
	color:#666666;}
span.Heading5Char
	{mso-style-name:"Heading 5 Char";
	mso-style-noshow:yes;
	mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:"Heading 5";
	mso-ansi-font-size:11.0pt;
	mso-bidi-font-size:11.0pt;
	color:#666666;}
span.Heading6Char
	{mso-style-name:"Heading 6 Char";
	mso-style-noshow:yes;
	mso-style-priority:9;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:"Heading 6";
	mso-ansi-font-size:11.0pt;
	mso-bidi-font-size:11.0pt;
	color:#666666;
	font-style:italic;
	mso-bidi-font-style:normal;}
span.TitleChar
	{mso-style-name:"Title Char";
	mso-style-priority:10;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:Title;
	mso-ansi-font-size:26.0pt;
	mso-bidi-font-size:26.0pt;}
span.SubtitleChar
	{mso-style-name:"Subtitle Char";
	mso-style-priority:11;
	mso-style-unhide:no;
	mso-style-locked:yes;
	mso-style-link:Subtitle;
	mso-ansi-font-size:15.0pt;
	mso-bidi-font-size:15.0pt;
	font-family:"Arial",sans-serif;
	mso-ascii-font-family:Arial;
	mso-fareast-font-family:Arial;
	mso-hansi-font-family:Arial;
	mso-bidi-font-family:Arial;
	color:#666666;}
.MsoChpDefault
	{mso-style-type:export-only;
	mso-default-props:yes;
	mso-ansi-language:EN;}
.MsoPapDefault
	{mso-style-type:export-only;
	line-height:115%;}
@page WordSection1
	{size:8.5in 11.0in;
	margin:1.0in 1.0in 1.0in 1.0in;
	mso-header-margin:.5in;
	mso-footer-margin:.5in;
	mso-paper-source:0;}
div.WordSection1
	{page:WordSection1;}
 /* List Definitions */
 @list l0
	{mso-list-id:1227642011;
	mso-list-template-ids:75105080;}
@list l0:level1
	{mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level2
	{mso-level-number-format:alpha-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level3
	{mso-level-number-format:roman-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:right;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level4
	{mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level5
	{mso-level-number-format:alpha-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level6
	{mso-level-number-format:roman-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:right;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level7
	{mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level8
	{mso-level-number-format:alpha-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l0:level9
	{mso-level-number-format:roman-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:right;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1
	{mso-list-id:1613322749;
	mso-list-template-ids:70170260;}
@list l1:level1
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level2
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level3
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level4
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level5
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level6
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level7
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level8
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l1:level9
	{mso-level-number-format:bullet;
	mso-level-text:-;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2
	{mso-list-id:2098668804;
	mso-list-template-ids:-1713711306;}
@list l2:level1
	{mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level2
	{mso-level-number-format:alpha-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level3
	{mso-level-number-format:roman-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:right;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level4
	{mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level5
	{mso-level-number-format:alpha-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level6
	{mso-level-number-format:roman-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:right;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level7
	{mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level8
	{mso-level-number-format:alpha-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:left;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}
@list l2:level9
	{mso-level-number-format:roman-lower;
	mso-level-tab-stop:none;
	mso-level-number-position:right;
	text-indent:-.25in;
	text-decoration:none;
	text-underline:none;}

-->
