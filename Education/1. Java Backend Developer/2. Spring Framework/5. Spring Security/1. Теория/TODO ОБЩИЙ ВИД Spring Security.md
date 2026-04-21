Аутентификация определяется интерфейсом `AuthenticationManager`, или его реализацией `ProviderManager`

Именно в них определяется "цепочка" (список) того, как происходит аутентификация

Сама аутентификация описывается в классах `AuthenticatonProvider`. 
`ProviderManager` делегирует аутентификацию СПИСКУ из `AuthenticatonProvider`

> ВОПРОС
> Узнать какие AuthenticationProvider обычно используются, кроме обычных DaoAuthNProvider, и какой-то JwtProvider

Если же пользователь делает НЕАУТЕНТИФИЦИРОВАННЫЙ запрос на ресурс, то для отправки запроса данных от него используется `AuthenticationEntryPoint`, или его частные реализации
- `LoginUrlAuthenticationEntryPoint` - для формы, и 
- `BasicAuthenticationEntryPoint` - для basic аутентификации)

А данные от пользователя "ловит" `AbstractAuthenticationProcessingFilter` или его реализации
- `UsernamePasswordAuthenticationFilter`
- `BasicAuthenticationFilter`

---

