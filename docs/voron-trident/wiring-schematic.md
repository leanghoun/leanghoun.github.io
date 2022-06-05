---
layout: default
title: Wiring Schematic
parent: Voron Trident
permalink: /docs/voron-trident/wiring-schematic
nav_order: 3
---

# Wiring Schematic
{: .no_toc }

---

<main>
	<section id="wiring">
		<div id="image-00">
			<img src="../../../../assets/images/wiring-00-hardware.png" id="00-hardware" />
		</div>
		<div id="image-01" style="display:float;">
			<img src="../../../../assets/images/wiring-01-mains.png" id="01-mains" />
		</div>
		<div id="image-02" style="display:float;">
			<img src="../../../../assets/images/wiring-02-bed.png" id="02-bed" />
		</div>
		<div id="image-03" style="display:float;">
			<img src="../../../../assets/images/wiring-03-dc.png" id="03-dc" />
		</div>
		<div id="image-04" style="display:float;">
			<img src="../../../../assets/images/wiring-04-pi.png" id="04-pi" />
		</div>
		<div id="image-05" style="display:float;">
			<img src="../../../../assets/images/wiring-05-spider-power-motion.png" id="05-spider-power-motion" />
		</div>
		<div id="image-06" style="display:float;">
			<img src="../../../../assets/images/wiring-06-spider-hotend.png" id="06-spider-hotend" />
		</div>
		<div id="image-07" style="display:float;">
			<img src="../../../../assets/images/wiring-07-spider-extras.png" id="07-spider-extras" />
		</div>
		</section>
</main>

[All](javascript: void(0)){: .btn .btn-outline .button00 }
[Mains Wiring](javascript: void(0)){: .btn .btn-outline .button01 }
[Bed Cable Hookup](javascript: void(0)){: .btn .btn-outline .button02 }
[DC Power](javascript: void(0)){: .btn .btn-outline .button03 }
[Raspberry Pi](javascript: void(0)){: .btn .btn-outline .button04 }
[Spider - Power & Motion](javascript: void(0)){: .btn .btn-outline .button05 }
[Spider - Hotend](javascript: void(0)){: .btn .btn-outline .button06 }
[Spider - Extras](javascript: void(0)){: .btn .btn-outline .button07 }
[None](javascript: void(0)){: .btn .btn-outline .button99 }

<script>
document.addEventListener('DOMContentLoaded', function (event) {
	var wiring = document.getElementById('wiring');
	var image_00 = document.getElementById('image-00');
	var image_01 = document.getElementById('image-01');
	var image_02 = document.getElementById('image-02');
	var image_03 = document.getElementById('image-03');
	var image_04 = document.getElementById('image-04');
	var image_05 = document.getElementById('image-05');
	var image_06 = document.getElementById('image-06');
	var image_07 = document.getElementById('image-07');

	var button00 = document.querySelector('.button00');
	var button01 = document.querySelector('.button01');
	var button02 = document.querySelector('.button02');
	var button03 = document.querySelector('.button03');
	var button04 = document.querySelector('.button04');
	var button05 = document.querySelector('.button05');
	var button06 = document.querySelector('.button06');
	var button07 = document.querySelector('.button07');
	var button99 = document.querySelector('.button99');

	var show01 = true;
	var show02 = true;
	var show03 = true;
	var show04 = true;
	var show05 = true;
	var show06 = true;
	var show07 = true;

	gsap.set(wiring, {height: image_00.offsetHeight});

	button00.addEventListener('click', toggleOpacity);
	button01.addEventListener('click', toggleOpacity);
	button02.addEventListener('click', toggleOpacity);
	button03.addEventListener('click', toggleOpacity);
	button04.addEventListener('click', toggleOpacity);
	button05.addEventListener('click', toggleOpacity);
	button06.addEventListener('click', toggleOpacity);
	button07.addEventListener('click', toggleOpacity);
	button99.addEventListener('click', toggleOpacity);

	function onResize () {
		gsap.set(wiring, {height: image_00.offsetHeight});
		gsap.set(image_01, {y: 0-image_00.offsetHeight});
		gsap.set(image_02, {y: 0-image_00.offsetHeight*2});
		gsap.set(image_03, {y: 0-image_00.offsetHeight*3});
		gsap.set(image_04, {y: 0-image_00.offsetHeight*4});
		gsap.set(image_05, {y: 0-image_00.offsetHeight*5});
		gsap.set(image_06, {y: 0-image_00.offsetHeight*6});
		gsap.set(image_07, {y: 0-image_00.offsetHeight*7});
	}

	function toggleOpacity () {
		var target = this;
		var fade_opacity = .05;
		var fade_button = .5;
		<!--console.log(target.className);-->

		switch (target.className) {
			case "btn btn-outline button00":
				gsap.to(image_01, {duration: .2, opacity: 1});
				gsap.to(image_02, {duration: .2, opacity: 1});
				gsap.to(image_03, {duration: .2, opacity: 1});
				gsap.to(image_04, {duration: .2, opacity: 1});
				gsap.to(image_05, {duration: .2, opacity: 1});
				gsap.to(image_06, {duration: .2, opacity: 1});
				gsap.to(image_07, {duration: .2, opacity: 1});
				gsap.to(button01, {duration: .2, opacity: 1});
				gsap.to(button02, {duration: .2, opacity: 1});
				gsap.to(button03, {duration: .2, opacity: 1});
				gsap.to(button04, {duration: .2, opacity: 1});
				gsap.to(button05, {duration: .2, opacity: 1});
				gsap.to(button06, {duration: .2, opacity: 1});
				gsap.to(button07, {duration: .2, opacity: 1});
				show01 = true;
				show02 = true;
				show03 = true;
				show04 = true;
				show05 = true;
				show06 = true;
				show07 = true;
				break;
			case "btn btn-outline button01":
				if(show01) {
					gsap.to(image_01, {duration: .2, opacity: fade_opacity});
					gsap.to(button01, {duration: .2, opacity: fade_button});
					show01 = false;
				} else {
					gsap.to(image_01, {duration: .2, opacity: 1});
					gsap.to(button01, {duration: .2, opacity: 1});
					show01 = true;
				}
				break;
			case "btn btn-outline button02":
				if(show02) {
					gsap.to(image_02, {duration: .2, opacity: fade_opacity});
					gsap.to(button02, {duration: .2, opacity: fade_button});
					show02 = false;
				} else {
					gsap.to(image_02, {duration: .2, opacity: 1});
					gsap.to(button02, {duration: .2, opacity: 1});
					show02 = true;
				}
				break;
			case "btn btn-outline button03":
				if(show03) {
					gsap.to(image_03, {duration: .2, opacity: fade_opacity});
					gsap.to(button03, {duration: .2, opacity: fade_button});
					show03 = false;
				} else {
					gsap.to(image_03, {duration: .2, opacity: 1});
					gsap.to(button03, {duration: .2, opacity: 1});
					show03 = true;
				}
				break;
			case "btn btn-outline button04":
				if(show04) {
					gsap.to(image_04, {duration: .2, opacity: fade_opacity});
					gsap.to(button04, {duration: .2, opacity: fade_button});
					show04 = false;
				} else {
					gsap.to(image_04, {duration: .2, opacity: 1});
					gsap.to(button04, {duration: .2, opacity: 1});
					show04 = true;
				}
				break;
			case "btn btn-outline button05":
				if(show05) {
					gsap.to(image_05, {duration: .2, opacity: fade_opacity});
					gsap.to(button05, {duration: .2, opacity: fade_button});
					show05 = false;
				} else {
					gsap.to(image_05, {duration: .2, opacity: 1});
					gsap.to(button05, {duration: .2, opacity: 1});
					show05 = true;
				}
				break;
			case "btn btn-outline button06":
				if(show06) {
					gsap.to(image_06, {duration: .2, opacity: fade_opacity});
					gsap.to(button06, {duration: .2, opacity: fade_button});
					show06 = false;
				} else {
					gsap.to(image_06, {duration: .2, opacity: 1});
					gsap.to(button06, {duration: .2, opacity: 1});
					show06 = true;
				}
				break;
			case "btn btn-outline button07":
				if(show07) {
					gsap.to(image_07, {duration: .2, opacity: fade_opacity});
					gsap.to(button07, {duration: .2, opacity: fade_button});
					show07 = false;
				} else {
					gsap.to(image_07, {duration: .2, opacity: 1});
					gsap.to(button07, {duration: .2, opacity: 1});
					show07 = true;
				}
				break;
			case "btn btn-outline button99":
				gsap.to(image_01, {duration: .2, opacity: fade_opacity});
				gsap.to(image_02, {duration: .2, opacity: fade_opacity});
				gsap.to(image_03, {duration: .2, opacity: fade_opacity});
				gsap.to(image_04, {duration: .2, opacity: fade_opacity});
				gsap.to(image_05, {duration: .2, opacity: fade_opacity});
				gsap.to(image_06, {duration: .2, opacity: fade_opacity});
				gsap.to(image_07, {duration: .2, opacity: fade_opacity});
				gsap.to(button01, {duration: .2, opacity: fade_button});
				gsap.to(button02, {duration: .2, opacity: fade_button});
				gsap.to(button03, {duration: .2, opacity: fade_button});
				gsap.to(button04, {duration: .2, opacity: fade_button});
				gsap.to(button05, {duration: .2, opacity: fade_button});
				gsap.to(button06, {duration: .2, opacity: fade_button});
				gsap.to(button07, {duration: .2, opacity: fade_button});
				show01 = false;
				show02 = false;
				show03 = false;
				show04 = false;
				show05 = false;
				show06 = false;
				show07 = false;
				break;
		}
	}

	window.addEventListener('resize', onResize);
	window.addEventListener('load', onResize);
})
</script>