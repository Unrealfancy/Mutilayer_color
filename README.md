# Mutilayer_color
Fast calculation of spectra and CIE colors of multi-layer membrane structures with the help of TMM (Transfer Matrix Method)

本工具主要针对薄膜结构色的计算，通过材料的光学参数，每层的厚度，即可利用TMM(Transfer Matrix method)快速计算出结构的反射光谱[1]，
再利用CIE1931色空间原理计算反射光的颜色状态（可设置光源和视场角）。功能基于matlab app 实现，需要安装Image Processing Toolbox,
可以在附加功能管理器中检查是否安装。

更新V1.10：
增加了偏振选择

参考文献：  
[1]Macleod, H. Angus, and H. Angus Macleod. Thin-film optical filters. CRC press, 2010.
[2]Billmeyer and Saltzman. Principles of Color Technology 3rd Edition. Wiley-Interscience. 2000. ISBN 0-471-19459-X.

使用介绍：  
1，在选择材料里选择材料，点击添加层即将材料添加，可以在表格中修改每层材料的厚度，库里内置了21种材料，如果需要自定义材料，可以点击添加材料
选择包含材料光参的TXT文件，文件要求第一列为波长，范围要大于等于400-800nm,可以是nm也可以是um做单位（文件里不带单位），第二列为n值，第三列为k值，文件名为材料
名称，导入成功后即可添加自定义材料  
2，材料添加完成后点击计算便可在右边结果面板上获得材料的反射光谱，材料的CIE坐标，材料的sRGB颜色,需要注意的是设置材料第一层为衬底，默认值为100nm，
实际为无限厚，即不存在衬底下的反射，因此衬底厚度并无实际意义，默认环境是空气。  
3，支持改变入射角，并且在计算后，可以通过入射角旁的滑条实时观察反射谱对入射角的变化。
4，支持厚度的实时调整，在计算后点击表中对应层材料，表右边会显示滑动条，范围从0-两倍当前厚度，拖动滑条可以看到结果面板的结果实时变动，可以方便分
析材料厚度对反射谱和颜色的影响。  
5，支持调节颜色观测的视场角和光源，视场角2°和10°，光源可选D50,D55,D65,D75
7, 支持自导入光谱计算颜色，点击导入光谱数据，导入光谱第一列为波长范围要大于等于400-800nm,可以是nm也可以是um做单位（文件里不带单位），第二列是反射谱，
范围从0-1  
  
 注意事项：  
 低版本matlab（2018及以下）可能无法在app里看到CIE色空间，只能在打开时的新窗口中显示，如果出现的话，请不要关闭该窗口
    
![image](https://user-images.githubusercontent.com/109337832/181210147-6344766e-8f72-4e28-9c37-dd093a66073c.png)

 
