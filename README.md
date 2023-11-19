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
- Smoke tests starts **manually**.
- Nightly images are build once per day, at 2:00 AM UTC, or if [build config is changed](https://github.com/armbian/os/blob/main/userpatches/targets-release-nightly.yaml)
- Manually, when Armbian [release manager](https://github.com/orgs/armbian/teams/release-manager) executes a build action

# Latest smoke tests results:

- installs kernels, dtb and headers that are defined and supported by the board
- runs network and computing performance tests (7z benchmark)
- store armbianmonitor logs

<!--START_SECTION:data-section-->
<table width="100%"><tr><td align="left"><a id=Board ID href=#Board ID><b>Board name</b></a></td><td align=center><b>Kernel version</b></td><td align=center><b>Supported</b></td><td align=left><b>Logs</b></td><td align=right><b>Iperf</b></td><td align=right><b>7z -b</b></td><td align=right><b>Repo</b></td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=center>6.1.62-current-rockchip64</td><td align=center><a href=#rockpi-e><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/gobusalovo><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>843</td><td align=right>3393</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=center>6.1.50-current-rockchip64</td><td align=center><a href=#rockpi-e><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/nonadeyomu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>102</td><td align=right>3400</td><td align=right>stable</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=center>6.6.1-edge-rockchip64</td><td align=center><a href=#rockpi-e><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/wironokehu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>856</td><td align=right>3346</td><td align=right>beta</td></tr><tr><td align="left"><a id=rockpi-e href=#rockpi-e>Rockpi E</a></td><td align=center>6.4.13-edge-rockchip64</td><td align=center><a href=#rockpi-e><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/jufaxihasu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>229</td><td align=right>3379</td><td align=right>stable</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=center>6.1.62-current-sunxi64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/oyutahudaj><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>870</td><td align=right>4402</td><td align=right>beta</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=center>6.1.53-current-sunxi64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/equqeciyiz><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>874</td><td align=right>4260</td><td align=right>stable</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=center>6.6.1-edge-sunxi64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/funezasafo><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>877</td><td align=right>4281</td><td align=right>beta</td></tr><tr><td align="left"><a id=pineh64 href=#pineh64>Pine H64</a></td><td align=center>6.4.12-edge-sunxi64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/varisapele><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>810</td><td align=right>4265</td><td align=right>stable</td></tr><tr><td align="left"><a id=zeropi href=#zeropi>ZeroPi</a></td><td align=center>5.15.137-legacy-sunxi</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/ayilesobom><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>555</td><td align=right>2667</td><td align=right>beta</td></tr><tr><td align="left"><a id=zeropi href=#zeropi>ZeroPi</a></td><td align=center>5.15.127-legacy-sunxi</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/zifipubujo><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>547</td><td align=right>2657</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapim2ultra href=#bananapim2ultra>Banana Pi M2 Ultra</a></td><td align=center>6.1.62-current-sunxi</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/siceponuku><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>776</td><td align=right>2709</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapim2ultra href=#bananapim2ultra>Banana Pi M2 Ultra</a></td><td align=center>6.1.53-current-sunxi</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/esokojumit><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>803</td><td align=right>2710</td><td align=right>stable</td></tr><tr><td align="left"><a id=tinkerboard-2 href=#tinkerboard-2>Tinker Board 2</a></td><td align=center>6.1.62-current-rockchip64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/sagapuhisa><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>6794</td><td align=right>beta</td></tr><tr><td align="left"><a id=tinkerboard-2 href=#tinkerboard-2>Tinker Board 2</a></td><td align=center>6.1.50-current-rockchip64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/ebixebabec><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>853</td><td align=right>6833</td><td align=right>stable</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=center>6.1.62-current-meson64</td><td align=center><a href=#lepotato><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/zuvidorera><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>93</td><td align=right>3809</td><td align=right>beta</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=center>6.1.50-current-meson64</td><td align=center><a href=#lepotato><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/muzajugova><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>91</td><td align=right>3690</td><td align=right>stable</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=center>6.6.1-edge-meson64</td><td align=center><a href=#lepotato><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ebezugiguk><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>89</td><td align=right>3790</td><td align=right>beta</td></tr><tr><td align="left"><a id=lepotato href=#lepotato>Le potato</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=#lepotato><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/soqarovevi><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>89</td><td align=right>3702</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepi5 href=#orangepi5>Orange Pi 5</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#orangepi5><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/wodiyanasa><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>860</td><td align=right>15561</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepi5 href=#orangepi5>Orange Pi 5</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#orangepi5><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/eduyazebit><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>15649</td><td align=right>stable</td></tr><tr><td align="left"><a id=tinkerboard href=#tinkerboard>Tinker Board</a></td><td align=center>6.1.62-current-rockchip</td><td align=center><a href=#tinkerboard><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/unijusiyis><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>5228</td><td align=right>beta</td></tr><tr><td align="left"><a id=tinkerboard href=#tinkerboard>Tinker Board</a></td><td align=center>6.1.50-current-rockchip</td><td align=center><a href=#tinkerboard><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/dusixolihi><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>880</td><td align=right>4812</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=center>n/a</td><td align=center><a href=#khadas-vim3><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><img src=https://img.shields.io/static/v1?label=&message=n/a&color=white></td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=center>n/a</td><td align=center><a href=#khadas-vim3><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><img src=https://img.shields.io/static/v1?label=&message=n/a&color=white></td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=center>n/a</td><td align=center><a href=#khadas-vim3><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><img src=https://img.shields.io/static/v1?label=&message=n/a&color=white></td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=khadas-vim3 href=#khadas-vim3>Khadas VIM3</a></td><td align=center>n/a</td><td align=center><a href=#khadas-vim3><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><img src=https://img.shields.io/static/v1?label=&message=n/a&color=white></td><td align=right>n/a</td><td align=right>n/a</td><td align=right></td></tr><tr><td align="left"><a id=orangepizero href=#orangepizero>Orange Pi Zero</a></td><td align=center>6.1.62-current-sunxi</td><td align=center><a href=#orangepizero><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/mequnekoto><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>89</td><td align=right>2514</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizero href=#orangepizero>Orange Pi Zero</a></td><td align=center>6.1.53-current-sunxi</td><td align=center><a href=#orangepizero><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/risecoluco><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>89</td><td align=right>2541</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=center>6.1.62-current-sunxi64</td><td align=center><a href=#orangepizero2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/eqibacukiq><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>830</td><td align=right>3152</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=center>6.1.53-current-sunxi64</td><td align=center><a href=#orangepizero2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/uviyunadig><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>827</td><td align=right>3133</td><td align=right>stable</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=center>6.6.1-edge-sunxi64</td><td align=center><a href=#orangepizero2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ufuxaxukug><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>820</td><td align=right>3071</td><td align=right>beta</td></tr><tr><td align="left"><a id=orangepizero2 href=#orangepizero2>Orange Pi Zero2</a></td><td align=center>6.4.12-edge-sunxi64</td><td align=center><a href=#orangepizero2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/acataxuteh><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>828</td><td align=right>3158</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=center>6.1.62-current-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/fivixakatu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>5648</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=center>6.1.50-current-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/yedilecuko><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>5547</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=center>6.6.1-edge-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/cuzefoceqa><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>5595</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidc4 href=#odroidc4>Odroid C4</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/emokenuhap><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>5587</td><td align=right>stable</td></tr><tr><td align="left"><a id=bigtreetech-cb1 href=#bigtreetech-cb1>BigTreeTech CB1</a></td><td align=center>6.1.43-legacy-sun50iw9-btt</td><td align=center><a href=#bigtreetech-cb1><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/oxexesaseb><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>89</td><td align=right>2695</td><td align=right>beta</td></tr><tr><td align="left"><a id=bigtreetech-cb1 href=#bigtreetech-cb1>BigTreeTech CB1</a></td><td align=center>6.1.43-legacy-sun50iw9-btt</td><td align=center><a href=#bigtreetech-cb1><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/warununaci><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>90</td><td align=right>2603</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=center>6.1.62-current-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/acacafenum><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>8793</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=center>6.1.50-current-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/vagugaviso><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>912</td><td align=right>8937</td><td align=right>stable</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=center>6.6.1-edge-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/omosejiwam><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>970</td><td align=right>8963</td><td align=right>beta</td></tr><tr><td align="left"><a id=odroidn2 href=#odroidn2>Odroid N2</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=https://www.armbian.com/donate/><img src=https://img.shields.io/static/v1?label=&message=Community&color=white></a></td><td align=left><a href=https://paste.armbian.com/iwojakonep><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>8798</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=#bananapicm4io><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/sariyarupa><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>9496</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=#bananapicm4io><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/galiwegoco><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>840</td><td align=right>9192</td><td align=right>stable</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=#bananapicm4io><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ogacikadep><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>833</td><td align=right>8932</td><td align=right>beta</td></tr><tr><td align="left"><a id=bananapicm4io href=#bananapicm4io>Banana Pi CM4IO</a></td><td align=center>6.4.13-edge-meson64</td><td align=center><a href=#bananapicm4io><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/aqamotirav><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>890</td><td align=right>8736</td><td align=right>stable</td></tr><tr><td align="left"><a id=rock-5b href=#rock-5b>Rock 5B</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#rock-5b><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/lusokotime><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>2268</td><td align=right>15686</td><td align=right>beta</td></tr><tr><td align="left"><a id=rock-5b href=#rock-5b>Rock 5B</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#rock-5b><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ofojesaqes><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>2250</td><td align=right>16063</td><td align=right>stable</td></tr><tr><td align="left"><a id=nanopi-r6s href=#nanopi-r6s>NanoPi R6S</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#nanopi-r6s><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/xanejewebo><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>2250</td><td align=right>15663</td><td align=right>beta</td></tr><tr><td align="left"><a id=nanopi-r6s href=#nanopi-r6s>NanoPi R6S</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#nanopi-r6s><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/jadocodezu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>2250</td><td align=right>15614</td><td align=right>stable</td></tr><tr><td align="left"><a id=nanopi-r6s href=#nanopi-r6s>NanoPi R6S</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#nanopi-r6s><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/jadocodezu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>2250</td><td align=right>15614</td><td align=right>beta</td></tr><tr><td align="left"><a id=nanopi-r6s href=#nanopi-r6s>NanoPi R6S</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#nanopi-r6s><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/jadocodezu><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>2250</td><td align=right>15614</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#khadas-edge2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ofaqaritok><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>360</td><td align=right>15722</td><td align=right>beta</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#khadas-edge2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ofaqaritok><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>360</td><td align=right>15722</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#khadas-edge2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ofaqaritok><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>360</td><td align=right>15722</td><td align=right>stable</td></tr><tr><td align="left"><a id=khadas-edge2 href=#khadas-edge2>Khadas Edge2</a></td><td align=center>5.10.160-legacy-rk35xx</td><td align=center><a href=#khadas-edge2><img src=https://img.shields.io/static/v1?label=&message=Supported&color=green></a></td><td align=left><a href=https://paste.armbian.com/ofaqaritok><img src=https://img.shields.io/static/v1?label=&message=Log&color=blue></a></td><td align=right>360</td><td align=right>15722</td><td align=right>stable</td></tr></table>
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

## Download prebuilt images

- [quarterly released **supported** builds](https://www.armbian.com/download/?device_support=Supported)
- [quarterly released **community maintained** builds](https://www.armbian.com/download/?device_support=Community%20support)
- [automatic released **rolling release** builds](https://github.com/armbian/os/releases/latest) (daily or when code changes)

## Support

- [Using Armbian](https://forum.armbian.com/forum/23-using-armbian/)

## Contact

- [Forums](https://forum.armbian.com) for Participate in Armbian
- IRC: `#armbian` on Libera.chat
- Discord: [https://discord.gg/armbian](https://discord.gg/armbian)
- Follow [@armbian](https://twitter.com/armbian) on X (formerly known as Twitter), [Fosstodon](https://fosstodon.org/@armbian) or [LinkedIn](https://www.linkedin.com/company/armbian).
- Bugs: [issues](https://github.com/armbian/build/issues) / [JIRA](https://armbian.atlassian.net/jira/dashboards/10000)
- Office hours: [Wednesday, 12 midday, 18 afternoon, CET](https://calendly.com/armbian/office-hours)

## License

This software is published under the [GPL-2.0 License license](LICENSE).
