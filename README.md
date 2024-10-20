# Исправленный конфиг для госулсуг
На MacOS в госулугах не видны сертификаты, притом что все остальное с ним работает. Решение проблемы - нужно в конфиге плагина госуслуг добавить секцию


Путь к конфигу
```
/Library/Internet Plug-Ins/IFCPlugin.plugin/Contents/ifc.cfg
```


Секция которую нужно добавить, в блок params
```
  { name  = "CryptoPro CSP";
    alias = "cprocsp";
    type  = "pkcs11";
    alg   = "gost2001";
    model = "CPPKCS 3";
    lib_mac   = "/opt/cprocsp/lib/libcppkcs11.dylib";
  },
```