<p align="center">
  <a href="#build-framework">
   <img src="https://raw.githubusercontent.com/armbian/build/master/.github/armbian-logo.png" alt="Armbian logo" width="144">
  </a><br>
  <strong>Armbian OS</strong><br>
<br>
<a href=https://github.com/armbian/os/actions/workflows/complete-artifact-matrix-all.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/complete-artifact-matrix-all.yml?logo=githubactions&label=Artifacts%20make&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os/actions/workflows/repository-update.yml><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/repository-update.yml?logo=githubactions&label=Repository%20update&style=for-the-badge&branch=main"></a>
<a href=https://github.com/armbian/os#latest-smoke-tests-results><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/armbian/os/smoke-tests.yml?logo=githubactions&label=Smoke%20tests&style=for-the-badge&branch=main"></a>
</p>


# What does this project do?

- Keeps build framework [packages artifacts](https://github.com/orgs/armbian/packages) cache up to date
- Keeps stable [apt.armbian.com](https://apt.armbian.com) and nightly [beta.armbian.com](https://beta.armbian.com) packages repository up to date
- Builds [nightly](https://github.com/armbian/os/releases) and [stable images](https://www.armbian.com/download/) and uploads them to Armbian CDN
- Keep synchronizing the selection of [3rd party](external) applications with Armbian repositories
- Tests install of all packages added onto stable and testing Debian and Ubuntu releases

# How to enable images?

If you want to enable build configurations, edit [yaml config files](userpatches) and send a pull request. ([example](https://github.com/armbian/os/commit/70f3be4f3d96e9a301be751d3ecf3a24394356f9) )

# When is this happening?

- Artifacts cache is updated every eight hours, starting at 0:00 AM UTC
- Repository update starts after **artifacts cache update** is done succesfully.
- Smoke tests starts after **repository update** is done succesfully.
- Nightly images are build once per day, at 5:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a href=""><b>Board name</b></a></td><td align="left"><b>Started</b></td><td align=right><b>Kernel version</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td></tr><tr><td align="left"><a href="https://paste.armbian.com/nuteyefobo">Orange Pi Win</a></td><td align="left">2023-08-20&nbsp;22:54:18</td><td align=right>6.1.45-current-sunxi64</td><td align=right>960</td><td align=right>2882</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bizozegimi">Orange Pi Win</a></td><td align="left">2023-08-20&nbsp;23:08:35</td><td align=right>5.15.93-sunxi64</td><td align=right>390</td><td align=right>2500</td></tr><tr><td align="left"><a href="https://paste.armbian.com/yuwekonazi">Orange Pi Win</a></td><td align="left">2023-08-20&nbsp;23:23:53</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>789</td><td align=right>2752</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iqugilakuk">Orange Pi Win</a></td><td align="left">2023-08-20&nbsp;23:38:08</td><td align=right>6.1.11-sunxi64</td><td align=right>880</td><td align=right>2785</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-20&nbsp;22:45:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-20&nbsp;22:45:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-20&nbsp;22:45:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Tinker Board</a></td><td align="left">2023-08-20&nbsp;22:45:12</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/igejiwomif">Espressobin</a></td><td align="left">2023-08-20&nbsp;23:03:18</td><td align=right>5.15.127-current-mvebu64</td><td align=right>849</td><td align=right>1027</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ozefutezuj">Espressobin</a></td><td align="left">2023-08-20&nbsp;23:26:37</td><td align=right>5.15.93-mvebu64</td><td align=right>727</td><td align=right>1005</td></tr><tr><td align="left"><a href="https://paste.armbian.com/avaridujuy">Pine H64</a></td><td align="left">2023-08-20&nbsp;22:50:58</td><td align=right>6.1.45-current-sunxi64</td><td align=right>840</td><td align=right>3737</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eyefemobin">Pine H64</a></td><td align="left">2023-08-20&nbsp;23:01:31</td><td align=right>5.15.93-sunxi64</td><td align=right>863</td><td align=right>3674</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lozatukawo">Pine H64</a></td><td align="left">2023-08-20&nbsp;23:11:20</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>790</td><td align=right>3588</td></tr><tr><td align="left"><a href="https://paste.armbian.com/eworebaduc">Pine H64</a></td><td align="left">2023-08-20&nbsp;23:22:01</td><td align=right>6.1.11-sunxi64</td><td align=right>870</td><td align=right>3572</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">UEFI x86</a></td><td align="left">2023-08-20&nbsp;23:11:54</td><td align=right>5.15.127-legacy-x86</td><td align=right>827</td><td align=right>4600</td></tr><tr><td align="left"><a href="https://paste.armbian.com/rilebawayo">RockPro 64</a></td><td align="left">2023-08-20&nbsp;22:48:22</td><td align=right>6.1.46-current-rockchip64</td><td align=right>890</td><td align=right>6504</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ihocotabab">RockPro 64</a></td><td align="left">2023-08-20&nbsp;22:55:23</td><td align=right>5.15.93-rockchip64</td><td align=right>898</td><td align=right>6444</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zadiqociku">RockPro 64</a></td><td align="left">2023-08-20&nbsp;23:02:16</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>879</td><td align=right>6409</td></tr><tr><td align="left"><a href="https://paste.armbian.com/lirivusatu">RockPro 64</a></td><td align="left">2023-08-20&nbsp;23:09:16</td><td align=right>6.1.11-rockchip64</td><td align=right>889</td><td align=right>6459</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ewehuyijiw">Rockpi E</a></td><td align="left">2023-08-20&nbsp;22:52:34</td><td align=right>6.1.46-current-rockchip64</td><td align=right>90</td><td align=right>3323</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xivahonosu">Rockpi E</a></td><td align="left">2023-08-20&nbsp;23:06:21</td><td align=right>5.15.93-rockchip64</td><td align=right>91</td><td align=right>2906</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jowajumedi">Rockpi E</a></td><td align="left">2023-08-20&nbsp;23:19:58</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>90</td><td align=right>3277</td></tr><tr><td align="left"><a href="https://paste.armbian.com/moxepapuva">Rockpi E</a></td><td align="left">2023-08-20&nbsp;23:33:04</td><td align=right>6.1.11-rockchip64</td><td align=right>89</td><td align=right>2838</td></tr><tr><td align="left"><a href="https://paste.armbian.com/azesexesey">Odroid C2</a></td><td align="left">2023-08-20&nbsp;22:53:09</td><td align=right>6.1.46-current-meson64</td><td align=right>880</td><td align=right>3954</td></tr><tr><td align="left"><a href="https://paste.armbian.com/osihoxexeb">Odroid C2</a></td><td align="left">2023-08-20&nbsp;23:04:27</td><td align=right>6.1.11-meson64</td><td align=right>820</td><td align=right>4031</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xoxurakace">Odroid C2</a></td><td align="left">2023-08-20&nbsp;23:14:43</td><td align=right>6.4.11-edge-meson64</td><td align=right>880</td><td align=right>4025</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uzuhedoruw">Odroid C2</a></td><td align="left">2023-08-20&nbsp;23:25:57</td><td align=right>6.2.0-rc3-meson64</td><td align=right>888</td><td align=right>4017</td></tr><tr><td align="left"><a href="https://paste.armbian.com/cisipufula">NanoPi R6S</a></td><td align="left">2023-08-20&nbsp;22:44:13</td><td align=right>5.10.160-legacy-rk35xx</td><td align=right>2250</td><td align=right>15725</td></tr><tr><td align="left"><a href="https://paste.armbian.com/rapexilaru">Orange Pi 3 LTS</a></td><td align="left">2023-08-20&nbsp;22:49:31</td><td align=right>6.1.45-current-sunxi64</td><td align=right>870</td><td align=right>3893</td></tr><tr><td align="left"><a href="https://paste.armbian.com/usumosufos">Orange Pi 3 LTS</a></td><td align="left">2023-08-20&nbsp;22:59:19</td><td align=right>5.15.93-sunxi64</td><td align=right>860</td><td align=right>3837</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wesahagito">Orange Pi 3 LTS</a></td><td align="left">2023-08-20&nbsp;23:08:35</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>877</td><td align=right>3843</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sadibuhuye">Orange Pi 3 LTS</a></td><td align="left">2023-08-20&nbsp;23:18:24</td><td align=right>6.1.11-sunxi64</td><td align=right>874</td><td align=right>3811</td></tr><tr><td align="left"><a href="https://paste.armbian.com/azagemamad">Odroid C4</a></td><td align="left">2023-08-20&nbsp;22:49:18</td><td align=right>6.1.46-current-meson64</td><td align=right>890</td><td align=right>5606</td></tr><tr><td align="left"><a href="https://paste.armbian.com/guposemupe">Odroid C4</a></td><td align="left">2023-08-20&nbsp;22:57:54</td><td align=right>6.1.11-meson64</td><td align=right>880</td><td align=right>5491</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uheyujoraq">Odroid C4</a></td><td align="left">2023-08-20&nbsp;23:06:09</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>5657</td></tr><tr><td align="left"><a href="https://paste.armbian.com/usedopebiz">Odroid C4</a></td><td align="left">2023-08-20&nbsp;23:14:47</td><td align=right>6.2.0-rc3-meson64</td><td align=right>860</td><td align=right>5561</td></tr><tr><td align="left"><a href="https://paste.armbian.com/umaqisuyow">Rockpi 4B</a></td><td align="left">2023-08-20&nbsp;22:47:55</td><td align=right>6.1.46-current-rockchip64</td><td align=right>881</td><td align=right>6436</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jafisuraze">Rockpi 4B</a></td><td align="left">2023-08-20&nbsp;22:55:17</td><td align=right>5.15.93-rockchip64</td><td align=right>960</td><td align=right>6182</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zixufojapa">Rockpi 4B</a></td><td align="left">2023-08-20&nbsp;23:02:47</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>880</td><td align=right>6133</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wulirubona">Rockpi 4B</a></td><td align="left">2023-08-20&nbsp;23:10:21</td><td align=right>6.1.11-rockchip64</td><td align=right>790</td><td align=right>6075</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sojuwadaga">NanoPi M4</a></td><td align="left">2023-08-20&nbsp;22:46:57</td><td align=right>6.1.46-current-rockchip64</td><td align=right>880</td><td align=right>6606</td></tr><tr><td align="left"><a href="https://paste.armbian.com/duxexoqeli">NanoPi M4</a></td><td align="left">2023-08-20&nbsp;22:54:17</td><td align=right>5.15.93-rockchip64</td><td align=right>929</td><td align=right>6646</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ihumaqeduk">NanoPi M4</a></td><td align="left">2023-08-20&nbsp;23:01:30</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>940</td><td align=right>6706</td></tr><tr><td align="left"><a href="https://paste.armbian.com/unimemidey">NanoPi M4</a></td><td align="left">2023-08-20&nbsp;23:08:28</td><td align=right>6.1.11-rockchip64</td><td align=right>840</td><td align=right>6693</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iracecelas">Banana Pi Pro</a></td><td align="left">2023-08-20&nbsp;22:54:37</td><td align=right>6.1.45-current-sunxi</td><td align=right>421</td><td align=right>1024</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zorevapade">Banana Pi Pro</a></td><td align="left">2023-08-20&nbsp;23:10:14</td><td align=right>5.15.93-sunxi</td><td align=right>314</td><td align=right>1027</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nifiqihusu">Banana Pi Pro</a></td><td align="left">2023-08-20&nbsp;23:24:52</td><td align=right>6.4.10-edge-sunxi</td><td align=right>398</td><td align=right>1011</td></tr><tr><td align="left"><a href="https://paste.armbian.com/anosagodic">ZeroPi</a></td><td align="left">2023-08-20&nbsp;23:12:13</td><td align=right>5.15.126-legacy-sunxi</td><td align=right>552</td><td align=right>2656</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vemiqupegu">ZeroPi</a></td><td align="left">2023-08-20&nbsp;23:23:17</td><td align=right>5.4.88-sunxi</td><td align=right>547</td><td align=right>2765</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xelecoteki">ZeroPi</a></td><td align="left">2023-08-20&nbsp;23:33:15</td><td align=right>6.1.45-current-sunxi</td><td align=right>611</td><td align=right>2655</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uxuxabeguw">ZeroPi</a></td><td align="left">2023-08-20&nbsp;23:44:29</td><td align=right>5.15.93-sunxi</td><td align=right>555</td><td align=right>2761</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uhukucohij">ZeroPi</a></td><td align="left">2023-08-20&nbsp;23:54:53</td><td align=right>6.4.10-edge-sunxi</td><td align=right>555</td><td align=right>2657</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jusasajico">Cubietruck</a></td><td align="left">2023-08-20&nbsp;23:11:16</td><td align=right>6.1.45-current-sunxi</td><td align=right>389</td><td align=right>985</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ubosabekir">Cubietruck</a></td><td align="left">2023-08-20&nbsp;23:33:21</td><td align=right>5.15.93-sunxi</td><td align=right>335</td><td align=right>989</td></tr><tr><td align="left"><a href="https://paste.armbian.com/rowatekupe">NanoPi R4S</a></td><td align="left">2023-08-20&nbsp;22:48:45</td><td align=right>6.1.46-current-rockchip64</td><td align=right>940</td><td align=right>6443</td></tr><tr><td align="left"><a href="https://paste.armbian.com/axecuhiluk">NanoPi R4S</a></td><td align="left">2023-08-20&nbsp;22:57:13</td><td align=right>5.15.93-rockchip64</td><td align=right>870</td><td align=right>6398</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ilibokirap">NanoPi R4S</a></td><td align="left">2023-08-20&nbsp;23:05:11</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>950</td><td align=right>6427</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vicedevibi">NanoPi R4S</a></td><td align="left">2023-08-20&nbsp;23:13:21</td><td align=right>6.1.11-rockchip64</td><td align=right>910</td><td align=right>6486</td></tr><tr><td align="left"><a href="https://paste.armbian.com/julonafeva">Odroid N2</a></td><td align="left">2023-08-20&nbsp;22:44:57</td><td align=right>6.1.46-current-meson64</td><td align=right>880</td><td align=right>8664</td></tr><tr><td align="left"><a href="https://paste.armbian.com/gebocizago">Odroid N2</a></td><td align="left">2023-08-20&nbsp;22:50:27</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>8721</td></tr><tr><td align="left"><a href="https://paste.armbian.com/noforerihi">Odroid N2</a></td><td align="left">2023-08-20&nbsp;22:55:42</td><td align=right>6.4.11-edge-meson64</td><td align=right>880</td><td align=right>8778</td></tr><tr><td align="left"><a href="https://paste.armbian.com/woperomive">Odroid N2</a></td><td align="left">2023-08-20&nbsp;23:01:18</td><td align=right>6.2.0-rc3-meson64</td><td align=right>960</td><td align=right>8743</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zutiguboxo">Orange Pi 3</a></td><td align="left">2023-08-20&nbsp;22:47:16</td><td align=right>6.1.45-current-sunxi64</td><td align=right>846</td><td align=right>4257</td></tr><tr><td align="left"><a href="https://paste.armbian.com/wacigahoyo">Orange Pi 3</a></td><td align="left">2023-08-20&nbsp;22:55:08</td><td align=right>5.15.93-sunxi64</td><td align=right>862</td><td align=right>3917</td></tr><tr><td align="left"><a href="https://paste.armbian.com/elaqiducut">NanoPi Neo 3</a></td><td align="left">2023-08-20&nbsp;22:48:34</td><td align=right>6.1.46-current-rockchip64</td><td align=right>852</td><td align=right>3446</td></tr><tr><td align="left"><a href="https://paste.armbian.com/gapefohuxe">NanoPi Neo 3</a></td><td align="left">2023-08-20&nbsp;22:58:15</td><td align=right>5.15.93-rockchip64</td><td align=right>855</td><td align=right>2613</td></tr><tr><td align="left"><a href="https://paste.armbian.com/awujimalax">NanoPi Neo 3</a></td><td align="left">2023-08-20&nbsp;23:08:04</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>880</td><td align=right>2176</td></tr><tr><td align="left"><a href="https://paste.armbian.com/yupexawowi">NanoPi Neo 3</a></td><td align="left">2023-08-20&nbsp;23:19:01</td><td align=right>6.1.11-rockchip64</td><td align=right>605</td><td align=right>2037</td></tr><tr><td align="left"><a href="https://paste.armbian.com/zixoyadapu">Orange Pi Zero</a></td><td align="left">2023-08-20&nbsp;23:00:21</td><td align=right>5.15.126-legacy-sunxi</td><td align=right>90</td><td align=right>1993</td></tr><tr><td align="left"><a href="https://paste.armbian.com/abokuzobet">Orange Pi Zero</a></td><td align="left">2023-08-20&nbsp;23:15:40</td><td align=right>5.4.88-sunxi</td><td align=right>90</td><td align=right>1657</td></tr><tr><td align="left"><a href="https://paste.armbian.com/opalipamum">Orange Pi Zero</a></td><td align="left">2023-08-20&nbsp;23:32:37</td><td align=right>6.1.45-current-sunxi</td><td align=right>89</td><td align=right>2131</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ahavisuvan">Orange Pi Zero Plus</a></td><td align="left">2023-08-20&nbsp;22:56:31</td><td align=right>6.1.45-current-sunxi64</td><td align=right>770</td><td align=right>2518</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ehuhorulaf">Orange Pi Zero Plus</a></td><td align="left">2023-08-20&nbsp;23:10:57</td><td align=right>5.15.93-sunxi64</td><td align=right>790</td><td align=right>2457</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xahuvucugi">Orange Pi Zero Plus</a></td><td align="left">2023-08-20&nbsp;23:25:27</td><td align=right>6.4.10-edge-sunxi64</td><td align=right>831</td><td align=right>2502</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xugaxecayu">Orange Pi Zero2</a></td><td align="left">2023-08-20&nbsp;22:54:47</td><td align=right>6.1.45-current-sunxi64</td><td align=right>824</td><td align=right>2666</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xosulomare">Orange Pi Zero2</a></td><td align="left">2023-08-20&nbsp;23:12:19</td><td align=right>5.15.93-sunxi64</td><td align=right>662</td><td align=right>1167</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xosulomare">Orange Pi Zero2</a></td><td align="left">2023-08-20&nbsp;23:38:25</td><td align=right>5.15.93-sunxi64</td><td align=right>662</td><td align=right>1167</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xosulomare">Orange Pi Zero2</a></td><td align="left">2023-08-20&nbsp;23:38:27</td><td align=right>5.15.93-sunxi64</td><td align=right>662</td><td align=right>1167</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-20&nbsp;22:51:58</td><td align=right>6.1.46-current-mvebu</td><td align=right>820</td><td align=right>2178</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-20&nbsp;23:00:32</td><td align=right>5.15.93-mvebu</td><td align=right>810</td><td align=right>2180</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-20&nbsp;23:08:44</td><td align=right>6.2.16-edge-mvebu</td><td align=right>810</td><td align=right>2228</td></tr><tr><td align="left"><a href="https://paste.armbian.com/">Clearfog Pro</a></td><td align="left">2023-08-20&nbsp;23:17:26</td><td align=right>6.1.11-mvebu</td><td align=right>829</td><td align=right>2169</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jegiropohu">ODROID M1</a></td><td align="left">2023-08-20&nbsp;22:50:36</td><td align=right>6.3.13-edge-rk3568-odroid</td><td align=right>780</td><td align=right>5129</td></tr><tr><td align="left"><a href="https://paste.armbian.com/atunoxuzej">ODROID M1</a></td><td align="left">2023-08-20&nbsp;23:01:12</td><td align=right>6.1.12-rk3568-odroid</td><td align=right>870</td><td align=right>5258</td></tr><tr><td align="left"><a href="https://paste.armbian.com/adimametog">Tinker Board 2</a></td><td align="left">2023-08-20&nbsp;22:54:01</td><td align=right>6.1.46-current-rockchip64</td><td align=right>902</td><td align=right>6913</td></tr><tr><td align="left"><a href="https://paste.armbian.com/tunejeyuwo">Tinker Board 2</a></td><td align="left">2023-08-20&nbsp;23:01:55</td><td align=right>5.15.93-rockchip64</td><td align=right>880</td><td align=right>6711</td></tr><tr><td align="left"><a href="https://paste.armbian.com/vafiyuvumi">Tinker Board 2</a></td><td align="left">2023-08-20&nbsp;23:09:20</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>903</td><td align=right>6692</td></tr><tr><td align="left"><a href="https://paste.armbian.com/oruqijovij">Tinker Board 2</a></td><td align="left">2023-08-20&nbsp;23:17:11</td><td align=right>6.1.11-rockchip64</td><td align=right>881</td><td align=right>6593</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uyahicidod">Orange Pi 4 LTS</a></td><td align="left">2023-08-20&nbsp;22:48:49</td><td align=right>6.1.46-current-rockchip64</td><td align=right>871</td><td align=right>5262</td></tr><tr><td align="left"><a href="https://paste.armbian.com/geralicace">Orange Pi 4 LTS</a></td><td align="left">2023-08-20&nbsp;22:58:35</td><td align=right>5.15.93-rockchip64</td><td align=right>890</td><td align=right>4050</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ehekagojip">Orange Pi 4 LTS</a></td><td align="left">2023-08-20&nbsp;23:06:59</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>880</td><td align=right>4432</td></tr><tr><td align="left"><a href="https://paste.armbian.com/bipusisaqu">Orange Pi 4 LTS</a></td><td align="left">2023-08-20&nbsp;23:16:58</td><td align=right>6.1.11-rockchip64</td><td align=right>850</td><td align=right>3901</td></tr><tr><td align="left"><a href="https://paste.armbian.com/figiwekana">Le potato</a></td><td align="left">2023-08-20&nbsp;22:55:04</td><td align=right>6.1.46-current-meson64</td><td align=right>93</td><td align=right>3710</td></tr><tr><td align="left"><a href="https://paste.armbian.com/acokemahuj">Le potato</a></td><td align="left">2023-08-20&nbsp;23:08:25</td><td align=right>6.1.11-meson64</td><td align=right>93</td><td align=right>3739</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uqowosigug">Le potato</a></td><td align="left">2023-08-20&nbsp;23:21:46</td><td align=right>6.4.11-edge-meson64</td><td align=right>90</td><td align=right>3685</td></tr><tr><td align="left"><a href="https://paste.armbian.com/uwosoqimaq">Le potato</a></td><td align="left">2023-08-20&nbsp;23:35:33</td><td align=right>6.2.0-rc3-meson64</td><td align=right>93</td><td align=right>3745</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-20&nbsp;22:40:05</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">BigTreeTech CB1</a></td><td align="left">2023-08-20&nbsp;22:40:07</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-20&nbsp;22:40:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-20&nbsp;22:40:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-20&nbsp;22:40:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Banana Pi CM4IO</a></td><td align="left">2023-08-20&nbsp;22:40:10</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="https://paste.armbian.com/hequvupano">Banana Pi M5</a></td><td align="left">2023-08-20&nbsp;22:45:49</td><td align=right>6.1.46-current-meson64</td><td align=right>889</td><td align=right>5556</td></tr><tr><td align="left"><a href="https://paste.armbian.com/nejoxicipu">Banana Pi M5</a></td><td align="left">2023-08-20&nbsp;22:52:11</td><td align=right>6.1.11-meson64</td><td align=right>880</td><td align=right>5542</td></tr><tr><td align="left"><a href="https://paste.armbian.com/jajaveqawu">Banana Pi M5</a></td><td align="left">2023-08-20&nbsp;22:58:10</td><td align=right>6.4.11-edge-meson64</td><td align=right>780</td><td align=right>5514</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ucuyisovow">Banana Pi M5</a></td><td align="left">2023-08-20&nbsp;23:04:27</td><td align=right>6.2.0-rc3-meson64</td><td align=right>880</td><td align=right>5512</td></tr><tr><td align="left"><a href="https://paste.armbian.com/iguzejusiq">Khadas VIM2</a></td><td align="left">2023-08-20&nbsp;22:50:53</td><td align=right>6.1.46-current-meson64</td><td align=right>900</td><td align=right>6032</td></tr><tr><td align="left"><a href="https://paste.armbian.com/cadefizabe">Khadas VIM2</a></td><td align="left">2023-08-20&nbsp;23:02:22</td><td align=right>6.1.11-meson64</td><td align=right>890</td><td align=right>6059</td></tr><tr><td align="left"><a href="https://paste.armbian.com/inagiladab">Khadas VIM2</a></td><td align="left">2023-08-20&nbsp;23:13:23</td><td align=right>6.4.11-edge-meson64</td><td align=right>890</td><td align=right>6075</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sokigaloni">Khadas VIM2</a></td><td align="left">2023-08-20&nbsp;23:24:45</td><td align=right>6.2.0-rc3-meson64</td><td align=right>940</td><td align=right>6016</td></tr><tr><td align="left"><a href="https://paste.armbian.com/ofofalitep">Khadas VIM1</a></td><td align="left">2023-08-20&nbsp;22:49:26</td><td align=right>6.1.46-current-meson64</td><td align=right>91</td><td align=right>3688</td></tr><tr><td align="left"><a href="https://paste.armbian.com/utegenezad">Khadas VIM1</a></td><td align="left">2023-08-20&nbsp;22:59:21</td><td align=right>6.1.11-meson64</td><td align=right>93</td><td align=right>3689</td></tr><tr><td align="left"><a href="https://paste.armbian.com/yizupikaqa">Khadas VIM1</a></td><td align="left">2023-08-20&nbsp;23:09:04</td><td align=right>6.4.11-edge-meson64</td><td align=right>89</td><td align=right>3727</td></tr><tr><td align="left"><a href="https://paste.armbian.com/etixetenag">Khadas VIM1</a></td><td align="left">2023-08-20&nbsp;23:19:02</td><td align=right>6.2.0-rc3-meson64</td><td align=right>88</td><td align=right>3677</td></tr><tr><td align="left"><a href="https://paste.armbian.com/sinelapoyu">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-20&nbsp;22:58:05</td><td align=right>6.1.46-current-rockchip64</td><td align=right>522</td><td align=right>1850</td></tr><tr><td align="left"><a href="https://paste.armbian.com/johagobotu">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-20&nbsp;23:15:34</td><td align=right>5.15.93-rockchip64</td><td align=right>410</td><td align=right>1765</td></tr><tr><td align="left"><a href="https://paste.armbian.com/xetavuyoke">Orange Pi R1 Plus LTS</a></td><td align="left">2023-08-20&nbsp;23:32:06</td><td align=right>6.4.11-edge-rockchip64</td><td align=right>416</td><td align=right>1729</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-20&nbsp;22:40:50</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Rock 5B</a></td><td align="left">2023-08-20&nbsp;22:40:51</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-20&nbsp;22:40:06</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-20&nbsp;22:40:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-20&nbsp;22:40:08</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr><tr><td align="left"><a href="n/a">Orange Pi Zero Plus 2</a></td><td align="left">2023-08-20&nbsp;22:40:09</td><td align=right>n/a</td><td align=right>n/a</td><td align=right>n/a</td></tr></table>
<!--END_SECTION:data-section-->

## Would you like to join spare hardware to this automated testings?

All you need to do is:

- deploy any latest Armbian image to hardware
- provide IP address
- [contact us](https://www.armbian.com/contact/)

Device has to be always on and easily accesible for you to re-image in case of failed upgrade.

## Development

- [Pull request](https://github.com/armbian/build/pulls)
- [Weekly developers meetings](https://forum.armbian.com/events/)
- [Forums for developers](https://forum.armbian.com/forum/4-advanced-users-development/)

## OS download

- [Download](https://www.armbian.com/download/)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on Twitter, [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the GPL-2.0 License license.
