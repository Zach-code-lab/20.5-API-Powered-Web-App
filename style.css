document.getElementById("searchBtn").addEventListener("click", () => {
  const name = document.getElementById("pokeInput").value.toLowerCase();

  fetch(`https://pokeapi.co/api/v2/pokemon/${name}`)
    .then(response => response.json())
    .then(data => {
      document.getElementById("output").innerHTML = `
        <h2>${data.name}</h2>
        <img src="${data.sprites.front_default}">
        <p>Height: ${data.height}</p>
        <p>Weight: ${data.weight}</p>
        <p>Base XP: ${data.base_experience}</p>
      `;
    })
    .catch(() => {
      document.getElementById("output").innerHTML = "Pokémon not found.";
    });
});
