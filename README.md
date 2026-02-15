<h1 align="center">
  <img src="https://img.icons8.com/ios-filled/50/ff0000/moon-symbol.png" width="18"/>
  Pablo | Front-End Developer
  <img src="https://img.icons8.com/ios-filled/50/ff0000/drop-of-blood.png" width="18"/>
</h1>


<p align="center">
  🔥 Aprendiz em HTML, CSS & JavaScript <br>
  ⚔️ Evoluindo para dominar o Full Stack
</p>

```diff
+ Nome: Pablo
+ Classe: Front-End Developer
+ Especialidade: HTML,CSS,Javascript
+ Status: Subindo de nível constantemente ⚡
```

<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Minhas Linguagens GitHub</title>

<style>
body {
    background: #0d1117;
    color: #fff;
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 40px;
}

h1 {
    margin-bottom: 30px;
}

.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.card {
    background: #161b22;
    padding: 20px;
    width: 200px;
    border-radius: 12px;
    box-shadow: 0 0 15px rgba(0,0,0,0.5);
    transition: 0.3s;
}

.card:hover {
    transform: scale(1.05);
}

.bar {
    height: 8px;
    background: #30363d;
    border-radius: 10px;
    margin-top: 10px;
    overflow: hidden;
}

.fill {
    height: 100%;
    background: #58a6ff;
}
</style>
</head>
<body>

<h1>🚀 Minhas Linguagens Mais Usadas</h1>

<div class="container" id="languages"></div>

<script>
const username = "pablo-br-3";

async function getLanguages() {
    const repos = await fetch(`https://api.github.com/users/${pablo-br-3}/repos?per_page=100`)
        .then(res => res.json());

    let languageCount = {};

    for (const repo of repos) {
        if (repo.language) {
            languageCount[repo.language] = 
                (languageCount[repo.language] || 0) + 1;
        }
    }

    const total = Object.values(languageCount)
        .reduce((a, b) => a + b, 0);

    const sorted = Object.entries(languageCount)
        .sort((a, b) => b[1] - a[1]);

    const container = document.getElementById("languages");

    sorted.forEach(([lang, count]) => {
        const percentage = ((count / total) * 100).toFixed(1);

        container.innerHTML += `
            <div class="card">
                <h3>${lang}</h3>
                <p>${percentage}%</p>
                <div class="bar">
                    <div class="fill" style="width:${percentage}%"></div>
                </div>
            </div>
        `;
    });
}

getLanguages();
</script>

</body>
</html>

