# Prettier Konfigürasyonu

Bu belge, kod biçimlendiricisi olarak popüler olan ve geliştiricilerin biçimlendirme ayrıntılarıyla uğraşmadan temiz, iyi biçimlendirilmiş kod yazmalarına yardımcı olan Prettier'ın yapılandırılması ve kullanımı için bilgi ve talimatlar sağlar. Belgede, Prettier'ın nasıl yükleneceği ve yapılandırılacağı hakkında bilgiler yanı sıra, biçimlendirme hatalarını kontrol etmek ve düzeltmek için `package.json` dosyanıza betikler eklemek için nasıl yapılacağına dair bilgiler de yer almaktadır.

# Prettier

Prettier, kod tabanınızın tutarlı ve okunması kolay olmasına yardımcı olan bir kod biçimlendiricidir. Biçimlendirme ayrıntılarıyla uğraşmadan temiz, iyi biçimlendirilmiş kod yazmak isteyen geliştiriciler için popüler bir araçtır.

Bir Prettier yapılandırması, kodunuzu nasıl biçimlendireceğini Prettier'a söyleyen bir yapılandırma dosyasıdır. Bir Prettier yapılandırması oluşturarak, kodunuzun takımınızın kodlama tarzı veya kişisel tercihlerinize uygun olarak biçimlendirilmesini özelleştirebilirsiniz.

## Kullanımı

Prettier'ı yüklemek için terminale aşağıdaki komutu çalıştırın:

```bash
$ yarn add --dev --exact prettier
```

Kurduktan sonra, Prettier için bir yapılandırma dosyası oluşturabilirsiniz. Aşağıdaki komutu çalıştırarak `@itservtechnology/prettier-config` paketini bir temel yapılandırma olarak kullanabilirsiniz:

```bash
$ yarn add --dev @itservtechnology/prettier-config
```

Daha sonra, `package.json` dosyanızı düzenleyerek yapılandırmayı dahil edebilirsiniz:

```json
{
  // ...
  "prettier": "@itservtechnology/prettier-config"
}
```

Bu, Prettier'ın `@itservtechnology/prettier-config` tarafından sağlanan yapılandırma dosyasını kullanmasını sağlayacaktır.

## Betikler

Prettier kontrolleri ve düzeltmeleri için `package.json` dosyanıza betikler eklemek için aşağıdaki satırları ekleyebilirsiniz:

```json
{
  "scripts": {
    "prettier:check": "prettier --check '**/*.{js,jsx,ts,tsx,json,md}'",
    "prettier:fix": "prettier --write '**/*.{js,jsx,ts,tsx,json,md}'"
  }
}
```

`prettier:check` betiği dosyalarınızı biçimlendirme hataları için kontrol edecek ve `prettier:fix` betiği dosyalarınızı Prettier yapılandırmanıza uygun olarak otomatik biçimlendirecektir. Bu betikleri aşağıdaki gibi `yarn run` komutunu kullanarak çalıştırabilirsiniz:

```bash
yarn run prettier:check
yarn run prettier:fix
```

---

Notion AI tarafından oluşturuldu.
