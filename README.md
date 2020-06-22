# Firebase JS SDK custom errors messages

This repo aims to show local error messages to user when an exception occurs. Feel 
free to add  translation of your language.

## sample usage
```js
const firebaseErrors = {
    'auth/user-not-found': 'Bu emaile ait herhangi bir kullanıcı bulunamadı!',
    'auth/email-already-in-use': 'Bu email adresi daha sistemde mevcut',
    'auth/invalid-email': 'Geçersiz email adresi',
    'auth/operation-not-allowed': 'Email-Şifre kayıt işlemi için izin verilmedi.',
    'auth/weak-password': 'Girilen şifre yeterince güçlü değil'
  };
  auth.createUserWithEmailAndPassword("mailaddress@example.com", "123456").then(cred => {
      console.log(cred.user);
  }).catch(error => {
     alert(firebaseErrors[error.code] || error.message);
  })
```

[Here](https://firebase.google.com/docs/reference/js/firebase.auth.Auth#methods_1) is the list of JS SKD methods and error messages.