---
Başlık   : Özel Efektler ile .animate()
seviye: Yeni başlayanlar için
kaynak: http://jqfundamentals.com/legacy
özellik:
    - jQuery Temelleri
---
jQuery ile istenilen CSS özelliklerinı `.animate()` metotu ile hareketli hale getirilebilir. `.animate()` metodun kullanarak bir efektini hareketli hale getirelim.

```
// Custom effects with .animate()
$( "div.funtimes" ).animate({
		left: "+=50",
		opacity: 0.25
	},
	300, // Duration
	function() { // Callback when the animation is finished
		console.log( "done!" );
	}
);
```
**Not:** Renk özelliklerini `.animate()` metotun kullanrak yapılamaz. Renk özelliklerini 
[color plugin](http://github.com/jquery/jquery-color) eklentisini kullanarak kolayca gerçekleştilebilir. Renk eklentisi hakkında kitabımızın sonlarına doğru bahsedeceğiz.


### Easing

Tanım: Easing describes the manner in which an effect occurs — whether
the rate of change is steady, or varies over the duration of the animation.
jQuery easing için sadece iki metot içerir: hareket alanı ve doğrusal alan. Hareket efektileri için daha fazla hareket yaptırmak istiyorsanız "easing plugins" eklentisi mevcuttur.

jQuery 1.4 versiyonunda `.animate()` metotun kullanarak easing kullanılabilir.

```
// Per-property easing
$( "div.funtimes" ).animate({
	left: [ "+=50", "swing" ],
	opacity: [ 0.25, "linear" ]
}, 300 );
```

easing üzerinde daha fazla bilgi için, burasını takip edin
[Animation documentation on api.jquery.com](http://api.jquery.com/animate/).
