# Layouts padronizados

Caso seja necessário, é possível utilizar um layout padrão para toda uma aplicação, mudando apenas o conteúdo a ser exibido.

- Definição do layout
```js
import { Outlet } from "react-router-dom"
import { Header } from "../components/Header"

export function DefaultLayout() {
  return (
    <div>
      <Header />
      <Outlet />
    </div>
  )
}
```

O componente outlet será responsável por alterar para o conteúdo desejado.

- Configuração das rotas
```js
import { Route, Routes } from "react-router-dom"
import { Home } from "./pages/Home"
import { History } from "./pages/History"
import { DefaultLayout } from "./layouts/DefaultLayout"

export function Router() {
  return (
    <Routes>
      <Route path="/" element={<DefaultLayout />}>
        <Route path="/" element={<Home />} />
        <Route path="/history" element={<History />} />
      </Route>
    </Routes>
  )
}
```

Para configurar, basta envolver as rotas por um componente ``<Route>`` com element para o layout default.
OBS.: Os paths se somam, logo, se o path do primeiro ``<Route>`` ser ``/admin`` e conter uma rota ``/products`` dentro dele, a rota para acessar o products será ``/admin/products``
