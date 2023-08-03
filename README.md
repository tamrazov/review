# CODE REVIEW
### Сделай код-ревью кода. Найдите все ошибки (Ошибки оформления — синтаксис и линтер, ошибки best practice, и т.д) и исправьте их. Отправьте Pull-request на проверку или отправьте файл с исправленным кодом на проверку на почту ...

```js
function Function-Main(
  user,

  order

) {
  var userName = user ? user['name'] ? user.name : 'noname' : 'unknown'

  let userActive = user?.id ? true : false

  let params = {}

  window.localStorage.setItem('user', `${userName}`)

  export function createOrder = async (params) => {
      return await fetch('api/v1/create_order' + '?' + new URLSearchParams(params), { method: 'GET' })
        .then(() => console.warn('Заказ успешно создан'))
        .catch(console.error)
  }

  if(userActive) {
    params = Object.assign( params, { id: order.id, userId: +user.id && '', } )

    if(order.id) {
      createOrder(params)
    } else {
      return console.log('Невозможно выполнить заказ')
    }
  } else {
    return console.log('Юзер не активен')
  }

  return console.log('Чтото пошло не так')
}
```

