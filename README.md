# diamanteverde

<itEm>
<title>[B] UltraPeliculas HD[/B] Estrenos </title>
<link>$doregex[makelist2]</link>

<regex>
<name>makelist2</name>
<listrepeat><![CDATA[
<title>[makelist2.param2]</title>
<link>$doregex[makelist]</link>
<fanart>[makelist2.param1]</fanart>
<thumbnail>[makelist2.param1]</thumbnail>
]]></listrepeat>
<expres>poster"[\w\W\s]{0,15}src="(.*?)"[\w\W\s]{0,3}alt="(.*?)"[\w\W\s]{0,175}href="(.*?)"</expres>
<page>https://www.ultrapeliculashd.com</page>
</regex>

<regex>
<name>makelist</name>
<listrepeat><![CDATA[
<title>[makelist2.param2]   server:openload/[makelist.param1]</title>
<urlsolve>https://openload.co/embed/[makelist.param1]</urlsolve>
<fanart>[makelist2.param1]</fanart>
<thumbnail>[makelist2.param1]</thumbnail>
]]></listrepeat>
<expres>openload.co\/embed\/(.*?)"</expres>
<page>[makelist2.param3]</page>
</regex>

<thumbnail>https://raw.githubusercontent.com/blackghostaddon/gray/master/img/peliculas.png</thumbnail><fanart>https://i.pinimg.com/originals/3e/e3/d9/3ee3d9017f9183b51d384fbec5efc293.jpg</fanart></item>



	
	
















<itm>
<title>[B]PeliculasDK / Estrenos[/B]       </title>
 <link>$doregex[makelist3]</link>



<regex>
   <name>makelist3</name>
   <listrepeat><![CDATA[
       <title>Pagina [makelist3.param1]</title>

<link>$doregex[makelist2]</link>
<thumbnail>https://raw.githubusercontent.com/blackghostaddon/gray/master/img/peliculas.png</thumbnail>
   ]]></listrepeat>
   <expres><![CDATA[paginado:"(.*?)";]]></expres>
   <page>https://raw.githubusercontent.com/blackghostaddon/gray/master/kozm.txt</page>
   <cookieJar></cookieJar>
</regex>



<regex>
<name>makelist2</name>
<listrepeat><![CDATA[
<title> [makelist2.param2]   idioma:[makelist2.param4] </title>
<link>$doregex[makelist]</link>
<thumbnail>[makelist2.param3]</thumbnail>
<fanart>[makelist2.param3]</fanart>
]]></listrepeat>
<expres><![CDATA[href="(.*?)"[\w\W\s]{0,2}title="(.*?)"[\w\W\s]{0,7}src="(.*?)"[\w\W\s]{0,300}idioma/(.*?)"]]></expres>
<page>http://www.peliculasdk.com/ver/estrenos/page/[makelist3.param1]</page>
 </regex>



<regex>
   <name>makelist</name>
   <listrepeat><![CDATA[
          <title>[makelist2.param2]</title>
          <link>$doregex[id3]</link>
		  <thumbnail>[makelist2.param3]</thumbnail>
		<fanart>[makelist2.param3]</fanart>
   ]]></listrepeat>
   <expres><![CDATA[open\("(.*?)"]]></expres>
   <page>[makelist2.param1]</page>
   <cookieJar></cookieJar>
</regex>



<regex>
<name>id3</name>
<expres><![CDATA[#$pyFunction
def GetLSProData(page_data,Cookie_Jar,m):
    import urlresolver
    url = 'https://openload.co/embed/[makelist.param1]/'
    try:
        u = urlresolver.resolve(url)
    except:
        u = 'http://adryantv.org/error.mp4'
    return u
]]></expres>
<page></page>
</regex>
<thumbnail>https://raw.githubusercontent.com/blackghostaddon/gray/master/img/peliculas.png</thumbnail><fanart>https://i.pinimg.com/originals/3e/e3/d9/3ee3d9017f9183b51d384fbec5efc293.jpg</fanart></item>







































<itm>
<title>[B]CINETUX COM[/B]  Estrenos [Audio Latino]    </title>
<link>$doregex[makelist3]</link>



<regex>
<name>makelist3</name>
<listrepeat><![CDATA[
<title>Pagina [makelist3.param1]</title>
<link>$doregex[makelist2]</link>
]]></listrepeat>
<expres>'(.*?)'</expres>
<page>'1''2''3''4''5''6''7''8''9''10''11''12''13''14''15''16''17''18''19''20''21''22''23''24''25'</page>
</regex>


   <regex>
<name>makelist2</name>
<listrepeat><![CDATA[
<title>[makelist2.param3]</title>
<link>$doregex[makelist]</link>
<thumbnail>http:[makelist2.param2]</thumbnail>
]]></listrepeat>
<expres>href="(.*?)"[\w\W\s]{0,80}src="(.*?)".*?Title">(.*?)<</expres>
<page>http://www.cinetux.com/peliculas/page/[makelist3.param1]</page>
</regex>




<regex>
<name>makelist</name>
<listrepeat><![CDATA[
<title>[makelist2.param3]        openload/[makelist.param1]</title>
<urlsolve>https://openload.co/[makelist.param1]</urlsolve>
<thumbnail>[makelist2.param3]</thumbnail>
<fanart>[makelist2.param2]</fanart>
]]></listrepeat>
<expres>(https:\/\/.*?)&amp;quot</expres>
<page>[makelist2.param1]</page>
</regex>
<thumbnail>https://raw.githubusercontent.com/blackghostaddon/gray/master/img/peliculas.png</thumbnail><fanart>https://i.pinimg.com/originals/3e/e3/d9/3ee3d9017f9183b51d384fbec5efc293.jpg</fanart>
 </item>
