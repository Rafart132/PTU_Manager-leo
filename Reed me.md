# PTU Manager · Asistente para Pokémon Tabletop United 1.05

Una web offline-first para gestionar tu ficha de entrenador, tu equipo Pokémon, el combate en mesa y compartir todo con tu grupo. Sin servidor, sin cuentas, sin instalar nada.

## ¿Cómo la uso?

1. Entra a `https://TU_USUARIO.github.io/ptu-manager/`
2. La primera vez te guiará un asistente paso a paso
3. Todo se guarda automáticamente en tu navegador
4. Para compartir con tu grupo: **Compartir ficha → Generar código → pegar en el chat**

## ¿Cómo lo despliego en GitHub Pages?
En tu computadora
git clone https://github.com/TU_USUARIO/ptu-manager.git
cd ptu-manager
copiar todos los archivos aquí
git add .
git commit -m "Primera versión"
git push


Luego en GitHub → **Settings → Pages** → Source: `main / root`. En 1-2 minutos tienes URL pública.

## ¿Cómo agrego más Pokémon?

Edita `data/pokedex.json`. Cada entrada sigue este formato:

```json
"Bulbasaur": {
  "es": "Bulbasaur",
  "t": ["Planta", "Veneno"],
  "hp": 5, "atk": 5, "def": 5, "spa": 7, "spd": 7, "spe": 5,
  "abilities": {
    "basic": ["Confianza", "Fotosíntesis"],
    "advanced": ["Clorofila", "Manto Hoja"],
    "high": "Coraje"
  },
  "evo": { "next": "Ivysaur", "at": 15, "final": "Venusaur", "finalAt": 30 },
  "size": { "h": 0.7, "w": 6.9, "cat": "Pequeño", "wc": 1 },
  "skills": { "athl": "3d6+2", "acro": "2d6", "combat": "2d6", "stealth": "2d6", "percep": "2d6", "focus": "2d6+1" },
  "moves": {
    "level": [
      { "lvl": 1, "name": "Placaje", "t": "Normal" },
      { "lvl": 3, "name": "Gruñido", "t": "Normal" }
    ]
  }
}