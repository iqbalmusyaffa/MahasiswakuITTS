# MahasiswakuITTS
Aplikasi Career Development Center 

Step 1:
Install `NativeBase` dan dependencies nya dengan mengeksekusi command berikut ini pada terminal

```
npm install native-base
```

```
npx expo install react-native-svg
```

```
npx expo install react-native-safe-area-context
```

Step 2:
Patch `NativeBase` (Jika Muncul Warning SSRProvider) dengan membuka file `node_modules/native-base/src/core/NativeBaseProvider.tsx` Cari dan lihat pada baris ke 97 dan ubah <SSRProvider>{children}</SSRProvider> menjadi:

```
{React.version >= '18' ? children : <SSRProvider>{children}</SSRProvider>}
```

Step 3:
Pada terminal, jalankan command: 

```
npx patch-package native-base
```

