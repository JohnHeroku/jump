###### Tips
* 通过[caddy](https://github.com/caddyserver/caddy/releases)|[xray](https://github.com/XTLS/Xray-core/releases)|[acme.sh](https://github.com/acmesh-official/acme.sh)配置`vless(xtls) + vmess + trojan + ss+xray-plugin + naiveproxy`**共用443端口**  
* 参考：[xray](https://github.com/XTLS/Xray-examples)  &&  [lxhao61](https://github.com/lxhao61/integrated-examples)
* 安装:
```bash
bash <(curl -s https://raw.githubusercontent.com/mixool/across/master/xray/xray_whatever_uuid.sh) my.domain.com
```
* 卸载:
```bash
apt purge caddy -y
bash <(curl -L https://raw.githubusercontent.com/XTLS/Xray-install/main/install-release.sh) --remove; systemctl disable xray; systemctl stop xray; rm -rf /usr/local/etc/xray /var/log/xray
/root/.acme.sh/acme.sh --uninstall; rm -rf /root/.acme.sh
```
