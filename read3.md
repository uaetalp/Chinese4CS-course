<style>
/* 强制调大拼音样式，适配打印阅读 */
ruby {
    ruby-align: center;
    margin: 0 0.12em; 
}rt {
    font-size: 1.1em !important;  /* 显著调大拼音字号 */
    font-weight: bold !important; 
    color: #2c3e50 !important;   
    padding-bottom: 0.4em !important; 
}/* 打印优化 */
@media print {
    body { font-size: 14pt; line-height: 2.2; }
    h2 { border-bottom: 2px solid #333; padding-bottom: 8px; margin-top: 40px; }
}
</style>

# Week 3：<ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby><ruby>基<rt>jī</rt></ruby><ruby>础<rt>chǔ</rt></ruby>

## 1. <ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby><ruby>与<rt>yǔ</rt></ruby><ruby>管<rt>guǎn</rt></ruby><ruby>理<rt>lǐ</rt></ruby><ruby>系统<rt>xì tǒng</rt></ruby> (Database & DBMS)

<ruby>什么是<rt>shén me shì</rt></ruby><ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby>？ <ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby>（Database）<ruby>是<rt>shì</rt></ruby><ruby>按照<rt>àn zhào</rt></ruby><ruby>数据结构<rt>shù jù jié gòu</rt></ruby><ruby>来<rt>lái</rt></ruby><ruby>管理<rt>guǎn lǐ</rt></ruby><ruby>数据<rt>shù jù</rt></ruby><ruby>的<rt>de</rt></ruby><ruby>仓库<rt>cāng kù</rt></ruby> 。<ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby><ruby>管<rt>guǎn</rt></ruby><ruby>理<rt>lǐ</rt></ruby><ruby>系统<rt>xì tǒng</rt></ruby>（DBMS）<ruby>是<rt>shì</rt></ruby><ruby>操纵<rt>cāo zòng</rt></ruby><ruby>和<rt>hé</rt></ruby><ruby>管理<rt>guǎn lǐ</rt></ruby><ruby>数据库<rt>shù jù kù</rt></ruby><ruby>的<rt>de</rt></ruby><ruby>大型<rt>dà xíng</rt></ruby><ruby>软件<rt>ruǎn jiàn</rt></ruby> 。<ruby>常见<rt>cháng jiàn</rt></ruby><ruby>的<rt>de</rt></ruby> <ruby>DBMS<rt></rt></ruby> <ruby>有<rt>yǒu</rt></ruby> MySQL、Oracle <ruby>和<rt>hé</rt></ruby> SQL Server 。

------

## 2. <ruby>关<rt>guān</rt></ruby><ruby>系<rt>xì</rt></ruby><ruby>型<rt>xíng</rt></ruby><ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby><ruby>结<rt>jié</rt></ruby><ruby>构<rt>gòu</rt></ruby> (Relational Database Structure)

<ruby>表<rt>biǎo</rt></ruby><ruby>的<rt>de</rt></ruby><ruby>组<rt>zǔ</rt></ruby><ruby>成<rt>chéng</rt></ruby>： <ruby>关<rt>guān</rt></ruby><ruby>系<rt>xì</rt></ruby><ruby>型<rt>xíng</rt></ruby><ruby>数<rt>shù</rt></ruby><ruby>据<rt>jù</rt></ruby><ruby>库<rt>kù</rt></ruby><ruby>由<rt>yóu</rt></ruby><ruby>表<rt>biǎo</rt></ruby>（Table）<ruby>组成<rt>zǔ chéng</rt></ruby> 。<ruby>表<rt>biǎo</rt></ruby><ruby>由<rt>yóu</rt></ruby><ruby>行<rt>háng</rt></ruby>（Row / <ruby>记录<rt>jì lù</rt></ruby>）<ruby>和<rt>hé</rt></ruby><ruby>列<rt>liè</rt></ruby>（Column / <ruby>字段<rt>zì duàn</rt></ruby>）<ruby>组成<rt>zǔ chéng</rt></ruby> 。

**<ruby>主<rt>zhǔ</rt></ruby><ruby>键<rt>jiàn</rt></ruby>（Primary Key）**：<ruby>能<rt>néng</rt></ruby><ruby>唯一<rt>wéi yī</rt></ruby><ruby>标识<rt>biāo shí</rt></ruby><ruby>表中<rt>biǎo zhōng</rt></ruby><ruby>每<rt>měi</rt></ruby><ruby>条<rt>tiáo</rt></ruby><ruby>记录<rt>jì lù</rt></ruby><ruby>的<rt>de</rt></ruby><ruby>字段<rt>zì duàn</rt></ruby>，<ruby>比如<rt>bǐ rú</rt></ruby><ruby>学号<rt>xué hào</rt></ruby> 。

**<ruby>索<rt>suǒ</rt></ruby><ruby>引<rt>yǐn</rt></ruby>（Index）**：<ruby>用于<rt>yòng yú</rt></ruby><ruby>提高<rt>tí gāo</rt></ruby><ruby>查询<rt>chá xún</rt></ruby><ruby>效率<rt>xiào lǜ</rt></ruby> 。

------

## 3. <ruby>S<rt></rt></ruby><ruby>Q<rt></rt></ruby><ruby>L<rt></rt></ruby> <ruby>常<rt>cháng</rt></ruby><ruby>用<rt>yòng</rt></ruby><ruby>操<rt>cāo</rt></ruby><rt>zuò</rt></ruby><ruby>范<rt>fàn</rt></ruby><ruby>例<rt>lì</rt></ruby> (SQL Operation Examples)

<ruby>我<rt>wǒ</rt></ruby><ruby>们<rt>men</rt></ruby><ruby>使<rt>shǐ</rt></ruby><ruby>用<rt>yòng</rt></ruby> SQL（<ruby>结构化<rt>jié gòu huà</rt></ruby><ruby>查询<rt>chá xún</rt></ruby><ruby>语言<rt>yǔ yán</rt></ruby>）<ruby>来<rt>lái</rt></ruby><ruby>管理<rt>guǎn lǐ</rt></ruby><ruby>数据<rt>shù jù</rt></ruby> 。

**<ruby>创<rt>chuàng</rt></ruby><ruby>建<rt>jiàn</rt></ruby><ruby>表<rt>biǎo</rt></ruby>：** “<ruby>创<rt>chuàng</rt></ruby><ruby>建<rt>jiàn</rt></ruby><ruby>一个<rt>yī gè</rt></ruby><ruby>名为<rt>míng wéi</rt></ruby>‘<ruby>学<rt>xué</rt></ruby><ruby>生<rt>shēng</rt></ruby>’<ruby>的<rt>de</rt></ruby><ruby>表<rt>biǎo</rt></ruby>” 。

**<ruby>插<rt>chā</rt></ruby><ruby>入<rt>rù</rt></ruby><ruby>数据<rt>shù jù</rt></ruby>：** “<ruby>向<rt>xiàng</rt></ruby><ruby>学<rt>xué</rt></ruby><ruby>生<rt>shēng</rt></ruby><ruby>表<rt>biǎo</rt></ruby><ruby>插入<rt>chā rù</rt></ruby><ruby>一条<rt>yī tiáo</rt></ruby><ruby>记录<rt>jì lù</rt></ruby>” 。

**<ruby>查<rt>chá</rt></ruby><ruby>询<rt>xún</rt></ruby><ruby>数据<rt>shù jù</rt></ruby>：** “<ruby>查<rt>chá</rt></ruby><ruby>询<rt>xún</rt></ruby><ruby>学<rt>xué</rt></ruby><ruby>生<rt>shēng</rt></ruby><ruby>表<rt>biǎo</rt></ruby><ruby>中的<rt>zhōng de</rt></ruby><ruby>所有<rt>suǒ yǒu</rt></ruby><ruby>数据<rt>shù jù</rt></ruby>” 。

------

## 4. <ruby>表<rt>biǎo</rt></ruby><ruby>之<rt>zhī</rt></ruby><ruby>间<rt>jiān</rt></ruby><ruby>的<rt>de</rt></ruby><ruby>关<rt>guān</rt></ruby><ruby>系<rt>xì</rt></ruby> (Table Relationships)

<ruby>在<rt>zài</rt></ruby><ruby>数据库<rt>shù jù kù</rt></ruby><ruby>设计<rt>shè jì</rt></ruby><ruby>中<rt>zhōng</rt></ruby>，<ruby>表<rt>biǎo</rt></ruby><ruby>和<rt>hé</rt></ruby><ruby>表<rt>biǎo</rt></ruby><ruby>之间<rt>zhī jiān</rt></ruby><ruby>有<rt>yǒu</rt></ruby><ruby>联系<rt>lián xì</rt></ruby> 。

**<ruby>一<rt>yī</rt></ruby><ruby>对<rt>duì</rt></ruby><ruby>多<rt>duō</rt></ruby><ruby>关<rt>guān</rt></ruby><ruby>系<rt>xì</rt></ruby>（One-to-Many）：** <ruby>比如<rt>bǐ rú</rt></ruby>“<ruby>一个<rt>yī gè</rt></ruby><ruby>学<rt>xué</rt></ruby><ruby>生<rt>shēng</rt></ruby><ruby>可以<rt>kě yǐ</rt></ruby><ruby>有<rt>yǒu</rt></ruby><ruby>多<rt>duō</rt></ruby><ruby>个<rt>gè</rt></ruby><ruby>成<rt>chéng</rt></ruby><ruby>绩<rt>jì</rt></ruby>” 。

**<ruby>多<rt>duō</rt></ruby><ruby>对<rt>duō</rt></ruby><ruby>多<rt>duō</rt></ruby><ruby>关<rt>guān</rt></ruby><ruby>系<rt>xì</rt></ruby>（Many-to-Many）：** <ruby>比如<rt>bǐ rú</rt></ruby>“<ruby>一个<rt>yī gè</rt></ruby><ruby>学<rt>xué</rt></ruby><ruby>生<rt>shēng</rt></ruby><ruby>可以<rt>kě yǐ</rt></ruby><ruby>选修<rt>xuǎn xiū</rt></ruby><ruby>多<rt>duō</rt></ruby><ruby>门<rt>mén</rt></ruby><ruby>课程<rt>kè chéng</rt></ruby>” 。

**<ruby>外<rt>wài</rt></ruby><ruby>键<rt>jiàn</rt></ruby>（Foreign Key）：** <ruby>学号<rt>xué hào</rt></ruby><ruby>是<rt>shì</rt></ruby><ruby>成<rt>chéng</rt></ruby><ruby>绩<rt>jì</rt></ruby><ruby>表<rt>biǎo</rt></ruby><ruby>中的<rt>zhōng de</rt></ruby><ruby>外键<rt>wài jiàn</rt></ruby>，<ruby>关联<rt>guān lián</rt></ruby><ruby>到<rt>dào</rt></ruby><ruby>学<rt>xué</rt></ruby><ruby>生<rt>shēng</rt></ruby><ruby>表<rt>biǎo</rt></ruby><ruby>的<rt>de</rt></ruby><ruby>主键<rt>zhǔ jiàn</rt></ruby> 。