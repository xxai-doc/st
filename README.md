<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

E kgothaletswa ho kenya nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) pele, 'me joale `direnv allow` ka mor'a hore u kene bukeng ( [the .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) e tla etsoa ka mokhoa o itekanetseng ka mor'a ho kena bukeng).

Moelelo ke: Phetolelo ea Sechaena ho Sejapane, Sekorea, Senyesemane, phetolelo ea Senyesemane lipuong tse ling kaofela. Haeba u batla feela ho tšehetsa Sechaena le Senyesemane, u ka ngola feela `zh: en` .

Moelelo ke: Phetolelo ea Sechaena ho Sejapane, Sekorea, Senyesemane, phetolelo ea Senyesemane lipuong tse ling kaofela. Haeba u batla feela ho tšehetsa Sechaena le Senyesemane, u ka ngola feela `zh: en` .

* [khoutu ea pele](https://github.com/xxai-art/web)
* [Liphutheloana tsa puo bakeng sa sebaka ka kakaretso](https://github.com/xxai-art/web/tree/main/i18n)
* [Lipakete tsa puo bakeng sa li-module tsa ho kena](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Litokomane tsa Lipuo Tse Ngata Webosaete](https://github.com/xxai-doc)

Puo ea pele ea lenaneo ke [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , e eketsang likarolo tse ling ho latela syntax ea coffeescript, bona [./coffee_plus.md](./coffee_plus.md) .

## Boikemisetso ba liwebsaete le litokomane

Haha holim'a merero e 3 e latelang

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Sehlongoa ke `.mdt` , u ka sebelisa syntax e tšoanang le `<+ ./coffee_plus/import.js>` ho bua ka lifaele tsa ka ntle, le ho hlahisa letšoao le nang le suffix `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Phetolelo ea Markdown e ke ke ea fetolela likhoutu le lihokelo, 'me e tla boloka lipolelo tse fetoletsoeng. Haeba phetolelo e fetotsoe empa taba e ngotsoeng qalong e sa ka ea fetoloa, ho e phetha hape ho ke ke ha hlakola tokiso ea phetolelo.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Lifaele tsa puo bakeng sa ho fetolela liwebsaete tse entsoeng ka `yaml` .

### Document Translation Automation Litaelo

Sheba polokelo ea khoutu [xxai-art/doc](https://github.com/xxai-art/doc)

E kgothaletswa ho kenya nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) pele, 'me joale `direnv allow` ka mor'a hore u kene bukeng ( [the .envrc](https://github.com/xxai-art/doc/blob/main/.envrc) e tla etsoa ka mokhoa o itekanetseng ka mor'a ho kena bukeng).

E le ho qoba khoutu e kholo e fetoletsoeng lipuong tse makholo, ke thehile sebaka se arohaneng sa khoutu bakeng sa puo e 'ngoe le e' ngoe 'me ka theha mokhatlo oa ho boloka khoutu.

Ho beha mofuta oa tikoloho `GITHUB_ACCESS_TOKEN` ebe o sebelisa [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) ho tla iketsetsa polokelo ea khoutu.

Ha e le hantle, u ka boela ua e beha motheong oa khoutu.

Referense script reference [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Script Code e hlalosoa ka tsela e latelang:

[bunx](https://bun.sh/docs/cli/bunx) ke sebaka sa npx, e leng kapele. Ehlile, haeba u sena bun e kentsoeng, u ka sebelisa `npx` ho fapana le hoo.

`bunx mdt zh` renders `.mdt` bukeng ea zh joalo ka `.md` , bona lifaele tse 2 tse hoketsoeng ka tlase

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ke khoutu ea mantlha ea phetolelo (haeba u na le `nodejs` feela tse kentsoeng, empa `bun` le `direnv` ha lia kengoa, u ka boela ua matha `npx i18n` ho fetolela).

E tla hlalosa [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , tlhophiso ea `i18n.yml` tokomaneng ena e tjena:

```
en:
zh: ja ko en
```

Moelelo ke: Phetolelo ea Sechaena ho Sejapane, Sekorea, Senyesemane, phetolelo ea Senyesemane lipuong tse ling kaofela. Haeba u batla feela ho tšehetsa Sechaena le Senyesemane, u ka ngola feela `zh: en` .

Ea ho qetela ke [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , e ntšang litaba lipakeng tsa sehlooho le mongolo oa pele oa `README.md` ea puo ka 'ngoe ho hlahisa mongolo `README.md` . Khoutu e bonolo haholo, u ka e sheba u le mong.

Google API e sebelisoa ho fetolela mahala. Haeba u sa khone ho kena ho Google, ka kopo, lokisa le ho seta moemeli, joalo ka:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Mongolo oa phetolelo o tla hlahisa cache e fetoletsoeng bukeng ea `.i18n` , ka kopo e hlahlobe ka `git status` 'me u e kenye sebakeng sa polokelo ea likhoutu ho qoba liphetolelo tse pheta-phetoang.

Ka kopo, tsamaisa `bunx i18n` nako le nako ha u fetola phetolelo ho ntlafatsa cache.

Haeba mongolo oa pele le phetolelo li fetotsoe ka nako e le 'ngoe, cache e tla ferekanngoa, kahoo haeba u batla ho e fetola, u ka e fetola feela, ebe u matha `bunx i18n` ho ntlafatsa cache.
