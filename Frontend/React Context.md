```ts
import {createContext, useContext, useState} from react

const CyclesContext = createContext({} as any)

function newCycleForm() {
	let {activeCycle, setActiveCycle} = useContext(CyclesContext)

	return (
		<h1>
			NewCycleForm: {activeCycle}
			<button onClick={() => {
				activeCycle = 2
			}}
		>	
			Alterar ciclo ativo
			</button>
		</h1>
	)
}

export function Home() {
	const [activeCycle, setActiveCycle] = useState(0)
	return (
		<CyclesContext.Provider value={{activeCycle, setActiveCycle}}>
			<div>
				<newCycleForm />
			</div>
		</CyclesContext.Provider>
	)
} 
 ```
 