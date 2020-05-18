---
layout: post
title: Using Colab for Deep Learning
date: 2020-05-18 13:32:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: colab_logo2.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Colab, GPU,]
---
Google Colaboratory or simply "colab" is a Jupyter-esque environment which provides a platform for writing and executing python code in browser. Colab notebook enviornment runs on cloud and the ipython notebooks are stored in google drive. The availablity of free GPU's and easy sharing is what really distinguishes any of its contemporaries.

## Starting with Google Colab
### Tip 1 : Connecting with Drive
Mount the drive to the collaboratory.
~~~
from google.colab import drive 
drive.mount('/content/drive')
~~~
This step lets the user read the files present in the mounted google drive and subsequenly write result files to the drive. After mounting, the drive home page can be treated as the root folder.
For example, to read file "news.txt" present in "News_Files" folder in the drive the following code can be used.
```
with open("/content/drive/My Drive/News_Files/news.txt", "rb") as infile:
  outfile.write(infile.read())
```

### Tip 2 : Using free GPU
To start using the free GPU:
> Menu bar --> Runtime --> Change Runtime Type --> GPU
![I and My friends]({{site.baseurl}}/assets/img/change_runtime_type.jpg)

It is important to keep in mind that Google provides limited use of free gpu service. So, use this option only when training and testing the models, not while writing code. 

**Pro Tip -** Some of the models I've trained took significantly longer than than the upper limit of the capacity. I tend to save the checkpoints in the drive regularly (in pytorch using 'torch.save') after a particular number of iterations. After the capacity of the google account I'm using gets drained, I download the ipython notebook and reupload it to another colab account in incognito. Finally, mount it on the original drive account in which saved model was stored and load the saved checkpoint file. This will resume the training process from the checkpoint. All in all, you can use the GPU provided by colab forever given you have access to sufficient number of google accounts. 

### Tip 3 : Installing libraries/modules in colab
All major libraries/modules like pytorch, tensorflow, fastai, opencv etc. are preinstalled in pytorch. If you wish to use a custom library which is not already there in colab or to use a different version of the preinstalled module, you can use !pip install or !apt-get install.

~~~
 !pip install -q matplotlib-venn 
 !pip install tensorflow==1.12.0 
~~~
"!" prompts the notebook cell to treat the code as a command line script. 

### Tip 4 : 

>Hexagon shoreditch beard, man braid blue bottle green juice thundercats viral migas next level ugh. Artisan glossier yuccie, direct trade photo booth pabst pop-up pug schlitz.

Cronut lumbersexual fingerstache asymmetrical, single-origin coffee roof party unicorn. Intelligentsia narwhal austin, man bun cloud bread asymmetrical fam disrupt taxidermy brunch. Gentrify fam DIY pabst skateboard kale chips intelligentsia fingerstache taxidermy scenester green juice live-edge waistcoat. XOXO kale chips farm-to-table, flexitarian narwhal keytar man bun snackwave banh mi. Semiotics pickled taiyaki cliche cold-pressed. Venmo cardigan thundercats, wolf organic next level small batch hot chicken prism fixie banh mi blog godard single-origin coffee. Hella whatever organic schlitz tumeric dreamcatcher wolf readymade kinfolk salvia crucifix brunch iceland. Literally meditation four loko trust fund. Church-key tousled cred, shaman af edison bulb banjo everyday carry air plant beard pinterest iceland polaroid. Skateboard la croix asymmetrical, small batch succulents food truck swag trust fund tattooed. Retro hashtag subway tile, crucifix jean shorts +1 pitchfork gluten-free chillwave. Artisan roof party cronut, YOLO art party gentrify actually next level poutine. Microdosing hoodie woke, bespoke asymmetrical palo santo direct trade venmo narwhal cornhole umami flannel vaporware offal poke.

* Hexagon shoreditch beard
* Intelligentsia narwhal austin
* Literally meditation four
* Microdosing hoodie woke

Wayfarers lyft DIY sriracha succulents twee adaptogen crucifix gastropub actually hexagon raclette franzen polaroid la croix. Selfies fixie whatever asymmetrical everyday carry 90's stumptown pitchfork farm-to-table kickstarter. Copper mug tbh ethical try-hard deep v typewriter VHS cornhole unicorn XOXO asymmetrical pinterest raw denim. Skateboard small batch man bun polaroid neutra. Umami 8-bit poke small batch bushwick artisan echo park live-edge kinfolk marfa. Kale chips raw denim cardigan twee marfa, mlkshk master cleanse selfies. Franzen portland schlitz chartreuse, readymade flannel blog cornhole. Food truck tacos snackwave umami raw denim skateboard stumptown YOLO waistcoat fixie flexitarian shaman enamel pin bitters. Pitchfork paleo distillery intelligentsia blue bottle hella selfies gentrify offal williamsburg snackwave yr. Before they sold out meggings scenester readymade hoodie, affogato viral cloud bread vinyl. Thundercats man bun sriracha, neutra swag knausgaard jean shorts. Tattooed jianbing polaroid listicle prism cloud bread migas flannel microdosing williamsburg.

Echo park try-hard irony tbh vegan pok pok. Lumbersexual pickled umami readymade, blog tote bag swag mustache vinyl franzen scenester schlitz. Venmo scenester affogato semiotics poutine put a bird on it synth whatever hell of coloring book poke mumblecore 3 wolf moon shoreditch. Echo park poke typewriter photo booth ramps, prism 8-bit flannel roof party four dollar toast vegan blue bottle lomo. Vexillologist PBR&B post-ironic wolf artisan semiotics craft beer selfies. Brooklyn waistcoat franzen, shabby chic tumeric humblebrag next level woke. Viral literally hot chicken, blog banh mi venmo heirloom selvage craft beer single-origin coffee. Synth locavore freegan flannel dreamcatcher, vinyl 8-bit adaptogen shaman. Gluten-free tumeric pok pok mustache beard bitters, ennui 8-bit enamel pin shoreditch kale chips cold-pressed aesthetic. Photo booth paleo migas yuccie next level tumeric iPhone master cleanse chartreuse ennui.
