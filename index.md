## OKTHAPIANGROUP

ini adalah website yang khusus menginfokan info yang sedang tranding di masyarakat, bukan untuk merugikan pihak2 tertentu, tapi untuk mencoba berkontribusi dalam situasi tersebut.

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>

<script>
$(document).ready(function(){
var d = new Date();
var month = new Array();
  month[0] = "Januari";
  month[1] = "Februari";
  month[2] = "Maret";
  month[3] = "April";
  month[4] = "Mei";
  month[5] = "Juni";
  month[6] = "Juli";
  month[7] = "Agustus";
  month[8] = "September";
  month[9] = "Oktober";
  month[10] = "November";
  month[11] = "Desember";

$("#date").html(d.getDate() + " " + month[d.getMonth()] + " " + d.getFullYear());
    $.ajax({async: true, cache: true, url: "https://api.kawalcorona.com/indonesia/", success: function(result){
     $("#positif").html(result[0].positif);
     $("#sembuh").html(result[0].sembuh);
     $("#meninggal").html(result[0].meninggal);
    }});
});
</script>

div class="datax">
<div class="title">
<h1>covid-19 indonesia : <span id="date"></span></h1>
</div>
<div id="show1" class="positif">
<div id="positif" class="angka">

</div>
<span class="detail">Positif</span>
</div>
<div id="show2" class="sembuh">
<div id="sembuh" class="angka"></div>
<span class="detail">Sembuh</span>
</div>
<div id="show3" class="meninggal">
<div id="meninggal" class="angka"></div>
<span class="detail">Meninggal</span>
</div>
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/okthapian/covid-19/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
