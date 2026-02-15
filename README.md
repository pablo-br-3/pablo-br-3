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
const username = "pablo-br-3";
const reposContainer = document.getElementById("repos");

fetch(`https://api.github.com/users/${username}/repos`)
  .then(response => response.json())
  .then(data => {
    data.forEach(repo => {
      const repoCard = document.createElement("div");
      repoCard.classList.add("repo-card");

      repoCard.innerHTML = `
        <h3>${repo.name}</h3>
        <p>${repo.description ? repo.description : "Sem descrição."}</p>
        <div class="repo-stats">
          ⭐ ${repo.stargazers_count}
          🍴 ${repo.forks_count}
          🧠 ${repo.language ? repo.language : "N/A"}
        </div>
      `;

      reposContainer.appendChild(repoCard);
    });
  })
  .catch(error => console.error("Erro ao buscar repositórios:", error));

<img width="1536" height="1024" alt="ChatGPT Image 14_02_2026, 23_07_58" src="https://github.com/user-attachments/assets/80366130-a3b2-498f-ac74-2684087239df" />
