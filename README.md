# Affiche
When the user clicks on View, the message containing the first and last name is displayed
App.js : 
import React, { useState } from 'react';
export default function App() {
  const [nom, SetNom] = useState();
  const [prenom, SetPrenom] = useState();
  const [Information, SetInformation] = useState();
  function INSCRIPT() {
    SetInformation(`nom ${nom} prenom ${prenom}`);
  }
  return (
    <div>
      <div>
        <h2></h2>
        <label>Nom : </label>
        <input
          type="text"
          onChange={(e) => {
            SetNom(e.target.value);
          }}
        />
      </div>
      <div>
        <h2></h2>
        <label>Prenom :</label>
        <input
          type="text"
          onChange={(e) => {
            SetPrenom(e.target.value);
          }}
        />
      </div>
      <button onClick={INSCRIPT}>Afficher</button>
      <p>{Information}</p>
    </div>
  );
}
