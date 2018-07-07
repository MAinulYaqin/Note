# Note

## Bilangan ganjil genap || Odd Even number

```JavaScript
const ganjilGenap1 = (e) => {
  if (e % 2 === 0) {
    console.log('genap || even');
  } else {
    console.log('ganjil || odd');
  }
}

__result__
 ganjilGenap1(6) == 'genap || even';
 ganjilGenap1(7) == 'ganjil || odd';

```

## Bilangan ganjil genap || Odd Even Number + looping

```JavaScript
const ganjilGenap2 = (e) => {
  for(var i = 0; i <= e; i++) {
     if (i % 2 === 0) {
	console.log(i +' angka genap || even number')
     } else {
	console.log(i +' adalah ganjil || odd number')
     }
  }
}

__result__
ganjilGenap3(20) =

0 adalah genap || even number
1 adalah ganjil || odd number
2 adalah genap || even number
3 adalah ganjil	|| odd number
4 adalah genap	|| even number
...

```

## Perpangkatan (btw, bahasa inggrisnya apaan anjir)

```JavaScript
var perpangkatan = (panjangAngka, angkaPangkat) => {
   for(var i = 0; i <= panjangAngka; i+=angkaPangkat) {
      console.log(i)
   }
}

__result__
// Angka akan di loop sampai 20
// dengan perpankatan 2, jadi.. 2, 4, 6, 8 ...
perpangkatan(20, 2) = 0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20
```

## Balik Kata

```JavaScript
function balikKata(kata){
   return kata.split("").reverse().join("");
}

__result__
console.log(balikKata("Halo saya AinulBedjo")); = "ojdeBluniA ayas olaH"
```

## Hitung Kata || word count

```JavaScript
function hitungAngka(kata) {
   var split = kata.split("")
   var Hitung = split.length
   return Hitung
}

__result__
console.log(hitungAngka('Siap satu dua...')) = '3' dor! :v
```

## Palindrome

example('eye') kalo dibaca dari belakang tetep eye
axample('katak') tetep katak

```JavaScript
function palindrome(str) {
   var pembanding = str.split('').reverse().join('')
   if (str === pembanding) {
       return true
    } else {
       return false
    }
       return str
}

__result__
console.log(palindrome('eye')) = true;
console.log(palindrome('ainul')) = false;
console.log(palindrome('katak')) = true;
```

## Palindrome - 2 GG version

```JavaScript
function palindrome2(str) {
  var kata = str.toLowerCase().replace(/[\W_]/g, '');
  var pembanding = kata.split('').reverse().join('')

  return kata === pembanding
}

__result__
console.log(palindrome('Kasur, Rusak')) = true;
console.log(palindrome('Ini tentu salah')) = false;
```

## Hitung huruf vokal a,i,u,e,o

```JavaScript
function vokalWordCount(str) {
  return (str.match(/[aiueo]/g) || [])
}

__result__
console.log(vokalWordCount('Halo panggil saya AinulBedjo')) =
(10) ["a", "o", "a", "i", "a", "a", "i", "u", "e", "o"]
```

## ROT13 chaesar chiper

```JavaScript
var str = `Lb, fb unir lbh orra cynlvat gung arj Zrfbcrgf tnzr? Gubfr arj Zrtnybalpuvqnr naq Oenqlcbqvqnr gurl nqqrq ner cerggl pbby. Npghnyyl, V jbhyq tb nf sne nf fnlvat gung vg vf abj zl yvsr'f qrnerfg nzovgvba gb bognva n "Vasyngnoyr Fybgu Zbafgre`
var ouput = ''

for (var i = 0; i < str.length; i++) {
	var c = str[i];

	if (c.match(/[a-zA-Z]/gi)) {
		var code = str.charCodeAt(i)

		if ((code >= 65) && (code <= 90)) {
			c = String.fromCharCode(((code - 65 + 13) % 26) + 65);
		} else if ((code >= 97) && (code <= 122)) {
			c = String.fromCharCode(((code - 97 + 13) % 26) + 97);
		}
	}
	ouput += c;
}
console.log(ouput)
```
