<template>
	<view>
		<view :style="{color:showColor}"><rich-text :nodes="text1"></rich-text></view>
		<view class="vv1">
			<view class="vvv1">
				<view>声优:{{text2[idList].cv}}</view>
				<view>形象颜色:{{text2[idList].colorFigures}}</view>
				<view>生日:{{text2[idList].birthday}}</view>
				<view>爱好:{{text2[idList].hobby}}</view>
				<view>性格:{{text2[idList].personality}}</view>
				<view>别称:{{text2[idList].nickname}}</view>
			</view>
			<view class="vvv2">
				<image :src="text2[idList].imgsrc" style="width: 100%;display: inline" mode="widthFix"></image>
			</view>
			<view class="divLine"></view>
		</view>
		<view class="vv2">
			<view>{{text2[idList].description1}}</view>
			<view>{{text2[idList].description2}}</view>
		</view>
		
	</view>
</template>

<script>
	export default{
		data(){
			return{
				introduction:{},
				text1:"",
				showColor:"",
				idList:1,
				text2:[{
					id:1,cv:'中村绘里子',colorFigures:'红色',showColor:"#e22b30",
					birthday:'4月3日',
					hobby:'做点心，卡拉OK，煲电话粥',
					personality:"充满活力朝气",
					nickname:"春阁下、はるるん、Geass能力者、时空战士",
					description1:"从小喜欢唱歌和制作点心，性格乐观、上进且待人友善，跟事务所众人都能合得来，但有时也会在情绪高涨时候不知所措，而且极度害怕孤独，感情观念相当保守。经常在平坦的地面摔倒，反而在陡峭的地方不会有事，略微有些天然呆。住在离市区较远的地方，每天从家里搭首班电车花两小时通勤，还会在电车上听音乐。曾经给过制作人超级甜的食物。和千早是好朋友。",
					description2:"成为偶像的原因：为了实现自己的儿时梦想。小时候在公园里唱歌里被一名老奶奶夸奖，至此爱上了唱歌；后来随母亲参加演唱会，看着台上的歌手，并立下了一定也要在舞台上唱歌的志向，最终如愿以偿。",
					imgsrc:"https://img.moegirl.org/common/9/92/%E3%82%88%E3%81%86%E3%81%93%E3%81%9D%E7%A7%81%E9%81%94%E3%81%AE%E5%8A%87%E5%A0%B4%E3%81%B8%EF%BC%81_%E5%A4%A9%E6%B5%B7%E6%98%A5%E9%A6%99%2B.png"
				},{
					id:2,cv:'长谷川明子',colorFigures:'草绿',showColor:"#b4e04b",
					birthday:'11月23日',
					hobby:'和朋友聊天，美甲',
					personality:"小恶魔？",
					nickname:"金色毛蟲、MIKI",
					description1:"宣传词是“未完成的年轻造型女王（未完の幼きビジュアルクイーン）”。不知世间辛苦，想要轻松地当偶像，但是很有天赋，只看一次的舞蹈也可以完美重现，在听了制作人的话后决定稍微努力一点。后来叫制作人“Honey“。口癖是“あふぅ”、“～なの”。工作状态与睡眠状态间的转换非常迅速。我行我素，有点小腹黑。很尊敬千早，因此除了对千早用敬语外，对其他人基本都是直呼其名，包括最年长的梓。屡次被律子说教后，总算记得对律子用敬语，但会慢半拍。（另外对真和伊织的称呼分别是“真君”和“额头酱”）",
					description2:"成为偶像的原因：能够很容易的当上偶像就好，因为美希不愿刻苦。但是之后，美希会为偶像这条路刻苦一辈子的。",
					imgsrc:"https://img.moegirl.org/common/thumb/d/d6/%E6%81%8B%E3%81%99%E3%82%8B%E8%A6%96%E7%B7%9A_%E6%98%9F%E4%BA%95%E7%BE%8E%E5%B8%8C%2B.png/255px-%E6%81%8B%E3%81%99%E3%82%8B%E8%A6%96%E7%B7%9A_%E6%98%9F%E4%BA%95%E7%BE%8E%E5%B8%8C%2B.png"
				},
				{
					id:3,cv:'今井麻美',colorFigures:'蓝',showColor:"#2743d2",
					birthday:'2月25日',
					hobby:'音乐鉴赏，练习？',
					personality:"冷娇、淑女",
					nickname:"蒼い歌姫、歌神、72、搓衣板、贫野郎",
					description1:"做事一本正经，对于歌唱有比普通人多一倍的热情和才能，觉得不能唱歌就活不下去，其实是为了已去世的弟弟如月优而唱歌。对唱歌以外的东西没有兴趣，所以一开始时很排斥“呱呱厨房”，但是在贵音和制作人的帮助下放下偏见。在意自己的小胸部，有着奇怪的笑点，不擅长使用电子设备。弟弟因意外去世后，家中永无宁日，目前一个人独居中。和春香是好朋友。",
					description2:"成为偶像的原因：以歌手的身份活下去。弟弟死后，父母离异，原本开朗的她完全封闭了内心。弟弟生前极爱听她唱歌，于是音乐成为了她活下去的唯一动力。",
					imgsrc:"https://img.moegirl.org/common/thumb/f/f2/%E6%96%B0%E6%98%A5%E3%81%AE%E5%85%89%E3%81%AB%E9%A1%98%E3%81%84%E3%82%92%E8%BE%BC%E3%82%81%E3%81%A6_%E5%A6%82%E6%9C%88%E5%8D%83%E6%97%A9%2B.png/255px-%E6%96%B0%E6%98%A5%E3%81%AE%E5%85%89%E3%81%AB%E9%A1%98%E3%81%84%E3%82%92%E8%BE%BC%E3%82%81%E3%81%A6_%E5%A6%82%E6%9C%88%E5%8D%83%E6%97%A9%2B.png"
				},
				{
					id:4,cv:'仁后真耶子',colorFigures:'橙',showColor:"#f39939",
					birthday:'3月25日',
					hobby:'黑白棋，棒球',
					personality:"活力元气系",
					nickname:"小弥、穷妹子",
					description1:"个性活泼开朗，爱护家庭的好孩子。由于自身营养很差，身高近乎停止增长。家中经济似乎不太好。在6人（原作中为5人）姊弟中排行老大，在事务所里常常帮忙打扫与倒垃圾。天然呆，还有点恐高症的元气娘。",
					description2:"成为偶像的原因：全家人的生计。父亲工作不稳定，为了早些帮助家里减轻负担而成为了偶像。",
					imgsrc:"https://img.moegirl.org/common/thumb/9/9b/%E3%82%AB%E3%83%A9%E3%83%95%E3%83%AB%E3%83%95%E3%82%A1%E3%82%AF%E3%83%88%E3%83%AA%E3%83%BC_%E9%AB%98%E6%A7%BB%E3%82%84%E3%82%88%E3%81%84%2B.png/255px-%E3%82%AB%E3%83%A9%E3%83%95%E3%83%AB%E3%83%95%E3%82%A1%E3%82%AF%E3%83%88%E3%83%AA%E3%83%BC_%E9%AB%98%E6%A7%BB%E3%82%84%E3%82%88%E3%81%84%2B.png"
				},
				{
					id:5,cv:'仁后真耶子',colorFigures:'白',showColor:"#d3dde9",
					birthday:'12月24日',
					hobby:'写诗，喝茶，写博客',
					personality:"胆小、異性恐懼症",
					nickname:"ゆきぴょん、小雪、鏟子妹",
					description1:"生性爱哭，有男性恐惧症且怕狗，为了改变自己而选择成为偶像。喜欢喝茶（尤其是绿茶）。似乎对身材没有自信，本人也说自己是“没肉、贫乳、小不点（ひんそーでひんにゅーでちんちくりんで）”，不过数字上并没有很差。极度消沉时会习惯在地上挖个洞把自己埋起来（所以铲子成为了雪歩的代表物）",
					description2:"成为偶像的目的：改变自己现在的性格。严厉的父亲让她完全成为了一个毫无勇气的胆小鬼，十五岁之前从来没有见过除了家人以外的男人。为了让自己变得勇敢，瞒着父亲当上了偶像。",
					imgsrc:"https://img.moegirl.org/common/thumb/4/43/%E6%98%9F%E9%99%8D%E3%82%8B%E8%81%96%E5%A4%9C_%E8%90%A9%E5%8E%9F%E9%9B%AA%E6%AD%A9%2B.png/255px-%E6%98%9F%E9%99%8D%E3%82%8B%E8%81%96%E5%A4%9C_%E8%90%A9%E5%8E%9F%E9%9B%AA%E6%AD%A9%2B.png"
				},
				{
					id:6,cv:'菊地真',colorFigures:'黄',showColor:"#515558",
					birthday:'8月29日',
					hobby:'运动，收集毛绒玩偶',
					personality:"有胆识、假小子、帅哥宝冢系、运动少女",
					nickname:"真哥、真王子",
					description1:"从小被父亲当男孩养大，自称也是“仆（ぼく）”，因此乍看之下会被认为是美少年，导致女性饭的数量远多于男性，但本人希望有女人味，为了外表与内在的差距而烦恼著。运动神经超群，喜欢跳舞。空手道黑带初段，有着很强的战斗力，意外的怕鬼故事也怕蟑螂。和雪步的关系非常好。",
					description2:"成为偶像的原因：想重新做回女孩子。父亲是一位儿子控，一直以要求儿子的条件要求她，包括服装及生活，为了更有女生气概而瞒着父亲加入了765事务所。",
					imgsrc:"https://img.moegirl.org/common/thumb/d/d6/%E6%A1%83%E8%89%B2%E3%82%B9%E3%83%9E%E3%82%A4%E3%83%AB%E2%99%AA_%E8%8F%8A%E5%9C%B0%E7%9C%9F%2B.png/255px-%E6%A1%83%E8%89%B2%E3%82%B9%E3%83%9E%E3%82%A4%E3%83%AB%E2%99%AA_%E8%8F%8A%E5%9C%B0%E7%9C%9F%2B.png"
				},
				{
					id:7,cv:'下田麻美',colorFigures:'黄',showColor:"#ffe43f",
					birthday:'5月22日',
					hobby:'发手机邮件、环保',
					personality:"小恶魔系",
					nickname:"小双",
					description1:"双胞胎中的妹妹，姐姐是双海真美。初代游戏中被设定为双子中的姐姐，X-BOX360版、PSP版及之后的作品中设定为妹妹。为了和真美分清身份，在头发右侧梳了个短辫子。二代并未留长，不过身材却发生了很大的变化。父亲是医师，因为行医而和母亲相遇，生活条件为中产阶级水平。姐妹二人性格大体相近，酷爱玩耍和恶作剧，还很喜欢打游戏。除了符合年龄的天真烂漫之外，也有人小鬼大的一面，经常说些调戏大人的言论。两人都称呼制作人为“兄ちゃん（哥哥）”，且非常喜欢欺负这个大哥哥。",
					description2:"成为偶像的原因：为了在电视台上出名，兼骗取更多的零花钱。PS4游戏《偶像大师：白金星光》中，成为偶像的目的是想学习更高深的恶作剧技巧。（这跟当偶像有什么关系！）",
					imgsrc:"https://img.moegirl.org/common/thumb/1/13/%E7%A7%8B%E3%82%92%E5%BD%A9%E3%82%8B%E3%82%A8%E3%83%B3%E3%82%BF%E3%83%BC%E3%83%86%E3%82%A4%E3%83%8A%E3%83%BC_%E5%8F%8C%E6%B5%B7%E4%BA%9C%E7%BE%8E%2B.png/255px-%E7%A7%8B%E3%82%92%E5%BD%A9%E3%82%8B%E3%82%A8%E3%83%B3%E3%82%BF%E3%83%BC%E3%83%86%E3%82%A4%E3%83%8A%E3%83%BC_%E5%8F%8C%E6%B5%B7%E4%BA%9C%E7%BE%8E%2B.png"
				},
				{
					id:8,cv:'下田麻美',colorFigures:'黄',showColor:"#ffe43f",
					birthday:'5月22日',
					hobby:'发手机邮件、盆栽',
					personality:"小恶魔系",
					nickname:"大双",
					description1:"双胞胎中的姐姐，妹妹是双海亚美。初代游戏中被设定为双子中的妹妹，X-BOX360版、PSP版及之后的作品中设定为姐姐。为了和亚美分清身份，在头发左边梳了个短辫子。二代变长为短马尾，身材也发生了很大的变化。父亲是医师，因为行医而和母亲相遇，生活条件为中产阶级水平。姐妹二人性格大体相近，酷爱玩耍和恶作剧，还很喜欢打游戏。除了符合年龄的天真烂漫之外，也有人小鬼大的一面，经常说些调戏大人的言论。两人都称呼制作人为“兄ちゃん（哥哥）”，且非常喜欢欺负这个大哥哥。因为二代中双子分别成为独立角色，两人之间的区别逐渐变得更加明显。真美的声音略偏向低音调，性格也比亚美更为稳重有责任感，先妹妹一步进入少女的思春期，对制作人表示好感的台词增多。",
					description2:"成为偶像的原因：为了在电视台上出名，兼骗取更多的零花钱。PS4游戏《偶像大师：白金星光》中成为偶像的目的是想变得性感成熟。",
					imgsrc:"https://img.moegirl.org/common/thumb/6/6b/%E3%81%86%E3%81%8D%E3%81%86%E3%81%8D%E3%82%B9%E3%82%A4%E3%83%BC%E3%83%88%E3%82%BF%E3%82%A4%E3%83%A0_%E5%8F%8C%E6%B5%B7%E7%9C%9F%E7%BE%8E%2B.png/255px-%E3%81%86%E3%81%8D%E3%81%86%E3%81%8D%E3%82%B9%E3%82%A4%E3%83%BC%E3%83%88%E3%82%BF%E3%82%A4%E3%83%A0_%E5%8F%8C%E6%B5%B7%E7%9C%9F%E7%BE%8E%2B.png"
				},
				{
					id:9,cv:'钉宫理惠',colorFigures:'粉红',showColor:"#fd99e1",
					birthday:'5月5日',
					hobby:'海外旅行、探访美食',
					personality:"傲娇",
					nickname:"额头酱、大小姐",
					description1:"水濑财团的大小姐。和有气质的外表正好相反，相当任性，傲娇的负责人。非常讨厌输给别人。因父亲和765 Production的社长是朋友而透过关系进入演艺界。对2位哥哥怀有强烈的自卑感与竞争心理。口癖是“にひひ!”。经常随身带着一只叫“夏露露18世”的兔子玩偶，很会讲鬼故事。虽然外表看上去是名小淑女，其实却正好相反，刁蛮任性又傲娇。性格要强，非常讨厌输给别人。也很在意个人形象，对外人拼命展示自己淑女的一面，只有对熟悉的人才会表现刁蛮的一面。但没有大小姐的架子，颇有常识，是事务所第二吐槽役，还很会讲鬼故事。与事务所最穷的弥生关系相当不错，在弥生面前只会娇不会傲。（没错！这就是传说中的贫富真爱组のヮの）",
					description2:"成为偶像的原因：为了证明自己。父亲和哥哥的成功显得她并不是很出色，为了在世人面前证明自己不是靠父兄的花瓶大小姐而成为偶像。",
					imgsrc:"https://img.moegirl.org/common/thumb/7/7b/%E3%82%AD%E3%83%A5%E3%83%BC%E3%83%86%E3%82%A3%E3%83%BC%E3%83%88%E3%83%AA%E3%83%83%E3%82%AF%E2%99%AA_%E6%B0%B4%E7%80%AC%E4%BC%8A%E7%B9%94%2B.png/255px-%E3%82%AD%E3%83%A5%E3%83%BC%E3%83%86%E3%82%A3%E3%83%BC%E3%83%88%E3%83%AA%E3%83%83%E3%82%AF%E2%99%AA_%E6%B0%B4%E7%80%AC%E4%BC%8A%E7%B9%94%2B.png"
				},
				{
					id:10,cv:'高桥智秋',colorFigures:'紫',showColor:"#9238be",
					birthday:'7月19日',
					hobby:'带狗散步，逛咖啡馆',
					personality:"沉着、天然呆、路痴",
					nickname:"梓姐、姐姐、乙女姐、F91",
					description1:"765所属偶像中最为年长，且胸部丰满。天然而沉着的治愈系大姐姐，不过是个严重的路痴。在设定上比制作人年长，制作人与爱好者都称她为“あずささん”。加入龙宫小町后，把头发理短了。是个严重的路痴，在哪里都能迷路比如自家事务所开的剧场。而且为人迷糊，什么都能带到事务所。莫名其妙地非常有男人缘。",
					description2:"成为偶像的原因：为了与梦中人相遇。据说曾经有恋爱失败的经历，为了“找到心中的白马王子”而成为了765事务所的偶像。但对感情比较保守，还跟好友约定谁都不能过线。",
					imgsrc:"https://img.moegirl.org/common/thumb/6/60/%E3%82%A6%E3%82%A9%E3%83%BC%E3%82%BF%E3%83%BC%E3%83%89%E3%83%AA%E3%83%BC%E3%83%A0_%E4%B8%89%E6%B5%A6%E3%81%82%E3%81%9A%E3%81%95%2B.png/255px-%E3%82%A6%E3%82%A9%E3%83%BC%E3%82%BF%E3%83%BC%E3%83%89%E3%83%AA%E3%83%BC%E3%83%A0_%E4%B8%89%E6%B5%A6%E3%81%82%E3%81%9A%E3%81%95%2B.png"
				},
				{
					id:11,cv:'原由实',colorFigures:'紫红',showColor:"#a6126a",
					birthday:'1月21日',
					hobby:'天文观测、看舞台剧→天文观测、历史',
					personality:"、大小姐、女王、电波、吃货",
					nickname:"	贵音殿、小公主、拉面姬、面妖",
					description1:"气质高贵，性格温和，坦诚，温柔有礼，思考回路却有些古怪，有电波属性，语速很慢。有着『银色王女』的称号，除了公开的资料，其他全是......765公认大胃王，非常喜欢拉面，休息日会去探访各种美食。直觉敏锐，导致恶德记者数次偷拍未遂。弱点是蛇，在响家留宿时被吓晕过。平时沉默寡言，有种冰山美人的气质。但思考回路略微与正常人不一致，有电波属性，对于不想回答的问题会直接以“这是最高秘密”来拒绝。出身似乎很高贵，是765事务所三大富户之一。有勇有谋，文武双全，通晓和文化，也十分擅长空手道和弓道，但很奇怪地不认识片假名。",
					description2:"成为偶像的原因：这是最高秘密。",
					imgsrc:"https://img.moegirl.org/common/thumb/e/e9/%E5%84%AA%E9%9B%85%E3%81%AA%E3%81%B2%E3%81%A8%E3%81%A8%E3%81%8D_%E5%9B%9B%E6%9D%A1%E8%B2%B4%E9%9F%B3%2B.png/255px-%E5%84%AA%E9%9B%85%E3%81%AA%E3%81%B2%E3%81%A8%E3%81%A8%E3%81%8D_%E5%9B%9B%E6%9D%A1%E8%B2%B4%E9%9F%B3%2B.png"
				},
				{
					id:12,cv:'沼仓爱美',colorFigures:'天蓝',showColor:"#01adb9",
					birthday:'10月10日',
					hobby:'编织，乒乓球，散步',
					personality:"活力元气系",
					nickname:"兽王、响爷、德鲁伊",
					description1:"性格爽朗，一根筋，非常要强。能够听懂动物的话，和刚认识的牛在分别时都能哭得泪流满面（真正的泪牛）。跳舞能力是765中最好的（动画中未有特别表现），拥有不比菊地真差的运动能力。老家在冲绳，有兄长一人，跟老哥赌气而独自离家到765当偶像。喜欢吃苦瓜。害怕寂寞，因此在家中养有狗﹑鸟﹑仓鼠等极多宠物（包括蛇和鳄鱼），并视之为家人。会为宠物煮食却总忍不住偷吃而致宠物逃跑。虽然元气满满且外表帅气，实际上却是可爱系的女孩子。有口癖，自称时会用“自分”。",
					description2:"成为偶像的原因：为了宠物们的饲料钱。",
					imgsrc:"https://img.moegirl.org/common/thumb/1/18/%E4%BC%9D%E3%82%8F%E3%82%8B%E6%80%9D%E3%81%84_%E6%88%91%E9%82%A3%E8%A6%87%E9%9F%BF%2B.png/255px-%E4%BC%9D%E3%82%8F%E3%82%8B%E6%80%9D%E3%81%84_%E6%88%91%E9%82%A3%E8%A6%87%E9%9F%BF%2B.png"
				},
				{
					id:13,cv:'若林直美',colorFigures:'绿',showColor:"#01a860",
					birthday:'6月23日',
					hobby:'考资格证，分析&实践',
					personality:"沉着冷静、有胆识",
					nickname:"眼镜娘、炸虾、律姐",
					description1:"冷静沈著思考清晰的眼镜娘。凡事会清楚表达自己的意见。765事务所的制作人，根据社长所说曾经是偶像，但是社长因此被说多嘴。有着“鬼军曹”的称号，负责说教。龙宫小町是律子成为制作人后带出来的第一个组合。电脑水平很高，擅长收集、处理情报，音无小鸟也会向她求助电脑方面的事宜。有喜好游戏的宅属性，因此很受亚美真美的喜爱。商人世家出身，父亲是大商店的店长。堂弟是876事务所的伪娘偶像秋月凉，姐弟妹关系很好。765事务所首屈一指的头脑派，冷静沉着，思考清晰，凡事会清楚表达自己的意见。标准的守序善良阵营，认真踏实，注重规矩。不过有时会因为一些小事而炸毛，是事务所第一吐槽役。",
					description2:"成为偶像的原因：为了成为制作人。最初为了积攒商业活动的经验，在765事务所打工做事务员，后来因为人手不足才临时成为偶像。作为偶像的同时也兼任事务员的工作。",
					imgsrc:"https://img.moegirl.org/common/thumb/1/12/%E3%81%8D%E3%82%89%E3%82%81%E3%81%8D%E3%83%9F%E3%83%A5%E3%83%BC%E3%82%B8%E3%82%A2%E3%83%A0_%E7%A7%8B%E6%9C%88%E5%BE%8B%E5%AD%90%2B.png/255px-%E3%81%8D%E3%82%89%E3%82%81%E3%81%8D%E3%83%9F%E3%83%A5%E3%83%BC%E3%82%B8%E3%82%A2%E3%83%A0_%E7%A7%8B%E6%9C%88%E5%BE%8B%E5%AD%90%2B.png"
				},
				{
					id:14,cv:'泷田树里',colorFigures:'浅黄',showColor:"#fff79f",
					birthday:'9月9日',
					hobby:'妄想、看电视',
					personality:"冒失、妄想、腐女",
					nickname:"鸟姐、最强事务员",
					description1:"爱好妄想（设定来自中之人的妄想癖），经常妄想自己结婚、其他偶像之间的百合等稀奇古怪的事情。尤其喜欢帅气的真，妄想过真×自己的CP，动画版中则妄想过真×雪步的CP。妄想时的画风极度猎奇，一旦被从妄想状态叫醒就会泪奔，有时还会伴有「ダメよ小鳥」的发言。因为百合类的妄想而被爱好者怀疑是腐女，后来判明确实如此。拥有腐女向的同人本，曾试图向雪步传教，还会爆买同人本。做事勤勉，待人温和，如同大家的姐姐一般包容着制作人和众位偶像。只不过性格相当迷糊，经常掉链子，偷懒被律子抓到的话还会被折扇敲脑袋。迷你偶像里小小鸟比本人更勤快、工作能力更强……此外很容易恐慌，广播剧中常见演唱会MC时紧张过度的小鸟导致偶像们也陷入恐慌的场景。受惊时会发出「ピヨッ！」（啾！）的叫声。",
					description2:"小鸟偶尔会在高木顺二朗社长经常光顾的钢琴酒吧「Unamela」（据伊织说「客人中有很多政经界的大人物」）里作为歌手唱歌。最后赤羽根P问她「当偶像不也不是梦吗」，小鸟的回答是：「女人都是有各种过去的哟。但是现在的我像这样偶尔唱唱歌的话就很开心了。」",
					imgsrc:"https://img.moegirl.org/common/thumb/4/4c/%E3%83%AC%E3%83%99%E3%83%AB%E3%82%A2%E3%83%83%E3%83%97_%E9%9F%B3%E7%84%A1%E5%B0%8F%E9%B3%A5.jpg/255px-%E3%83%AC%E3%83%99%E3%83%AB%E3%82%A2%E3%83%83%E3%83%97_%E9%9F%B3%E7%84%A1%E5%B0%8F%E9%B3%A5.jpg"
				},
				],
			}	
		},
		onLoad(res){
			let i =JSON.parse(decodeURIComponent(res.index))
			this.introduction=i
			console.log(this.introduction)
			this.text1='<h1 class="h1-1">'+this.introduction.name+'</h1>'
			this.idList=this.introduction.id-1
			this.showColor=this.text2[this.idList].showColor
			console.log(this.showColor)
		},
		
		methods:{
			
		}
	}
</script>

<style lang="less">
	body{
		background-color: #FFFAE8;
	}
	.divLine{
		width: 750rpx;
		height: 15rpx;
		border-bottom: 5rpx solid #999;
	}
	.h1-1{
		
		font-family: 华文新魏;
		margin-top: 20rpx;
		text-align: center;
	}
	.vv1{
		margin: 20rpx;
		min-height: 300rpx;
		.vvv1{
			min-height: 300rpx;
			display: inline-block;
			width: 500rpx;
			
			view{
				margin: 5rpx;
				padding-bottom: 10rpx;
				font-family: 楷体;
			}
		}
		.vvv2{
			display: inline-block;
			height: 300rpx;
			width: 200rpx;
			float: right;
		}
	}
	.vv2{
		text-indent: 2em;
	}
</style>
