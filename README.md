<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aprende Inglés Fácil</title>
  <link rel="stylesheet" href="webprincipal.css">
</head>
<body>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: linear-gradient(135deg, #024481 0%, #4982cc 100%);
  color: #333;
  line-height: 1.6;
  overflow-x: hidden;
  animation: pageLoad 0.5s ease-out;
}


header {
  background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.5)), 
              url('https://observatorio.tec.mx/wp-content/uploads/2022/05/maestroprofesorinstructor.jpeg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  color: white;
  padding: 80px 20px;
  text-align: center;
  position: relative;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.header-content {
  max-width: 800px;
  animation: fadeInUp 1s ease-out;
}

.main-title {
  font-size: clamp(3rem, 8vw, 6rem);
  font-weight: 900;
  margin-bottom: 20px;
  background: linear-gradient(45deg, #1050a3, #0c6588, #0b6d83);
  background-size: 300% 300%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradientShift 3s ease-in-out infinite;
  text-shadow: 0 4px 15px rgba(0,0,0,0.3);
}

.subtitle {
  font-size: 1.5rem;
  margin-bottom: 40px;
  opacity: 0.9;
  animation: fadeInUp 1s ease-out 0.3s both;
}


.navigation {
  margin-top: 40px;
}

.nav-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  max-width: 1000px;
}

.nav-card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 20px;
  padding: 30px;
  text-align: center;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  cursor: pointer;
  position: relative;
  overflow: hidden;
  text-decoration: none;
  color: white;
  display: block;
}

.nav-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.1), transparent);
  transition: left 0.5s;
}

.nav-card:hover::before {
  left: 100%;
}

.nav-card:hover {
  transform: translateY(-10px) scale(1.02);
  box-shadow: 0 20px 40px rgba(0,0,0,0.3);
  background: rgba(255, 255, 255, 0.2);
  color: white;
  text-decoration: none;
}

.card-icon {
  font-size: 3rem;
  margin-bottom: 15px;
  display: block;
}

.card-title {
  font-size: 1.3rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.card-desc {
  font-size: 0.95rem;
  opacity: 0.9;
}


.content-container {
  padding: 80px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.topic-section {
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(20px);
  border-radius: 25px;
  padding: 50px;
  margin-bottom: 40px;
  box-shadow: 0 20px 60px rgba(0,0,0,0.1);
  border: 1px solid rgba(255, 255, 255, 0.3);
  animation: slideInUp 0.8s ease-out;
}

.topic-section:nth-child(even) {
  animation-delay: 0.2s;
}

.topic-title {
  font-size: 2.5rem;
  color: #004899;
  margin-bottom: 20px;
  position: relative;
  display: inline-block;
}

.topic-title::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 3px;
  background: linear-gradient(45deg, #4a90e2, #667eea);
  border-radius: 2px;
}

.topic-intro {
  font-size: 1.2rem;
  margin-bottom: 30px;
  color: #666;
}

.grammar-section {
  margin-bottom: 40px;
}

.grammar-title {
  font-size: 1.8rem;
  color: #035caf;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.formula-box {
  background: linear-gradient(135deg, #4790cc, #164285);
  color: white;
  padding: 20px;
  border-radius: 15px;
  text-align: center;
  font-size: 1.3rem;
  font-weight: bold;
  margin: 20px 0;
  box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
  animation: pulse 2s infinite;
}

.examples-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin: 20px 0;
}

.example-card {
  background: #f8f9ff;
  border-left: 4px solid #4a90e2;
  padding: 20px;
  border-radius: 10px;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.example-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(74,144,226,0.1), transparent);
  transition: left 0.8s;
}

.example-card:hover::before {
  left: 100%;
}

.example-card:hover {
  transform: translateX(5px);
  box-shadow: 0 5px 20px rgba(74, 144, 226, 0.2);
}

.verb-tables {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  margin: 30px 0;
}

.verb-table {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.verb-table:hover {
  transform: translateY(-5px);
}

.table-header {
  background: linear-gradient(135deg, #1b69a8, #052270);
  color: white;
  padding: 20px;
  text-align: center;
  font-weight: bold;
  font-size: 1.2rem;
}

.table-content {
  padding: 20px;
}

.verb-pair {
  display: flex;
  justify-content: space-between;
  padding: 10px 0;
  border-bottom: 1px solid #eee;
  transition: background-color 0.3s ease;
}

.verb-pair:hover {
  background-color: #f0f4ff;
}

.verb-pair:last-child {
  border-bottom: none;
}


.play-button {
  display: inline-block;
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: white;
  padding: 15px 40px;
  border: none;
  border-radius: 50px;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
  text-decoration: none;
  margin: 20px 10px;
  position: relative;
  overflow: hidden;
}

.play-button::before {
  content: '🎮 ';
}

.play-button::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  width: 0;
  height: 0;
  background: rgba(255,255,255,0.3);
  border-radius: 50%;
  transform: translate(-50%, -50%);
  transition: width 0.6s, height 0.6s;
}

.play-button:hover::after {
  width: 300px;
  height: 300px;
}

.play-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 15px 35px rgba(102, 126, 234, 0.4);
}


footer {
  background: linear-gradient(135deg, #2c3e50, #3498db);
  color: white;
  text-align: center;
  padding: 40px 20px;
  margin-top: 80px;
}


.scroll-indicator {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  color: white;
  animation: bounce 2s infinite;
}


.nav-card:focus,
.play-button:focus {
  outline: 3px solid #fff;
  outline-offset: 2px;
}


@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes gradientShift {
  0%, 100% { 
    background-position: 0% 50%; 
  }
  50% { 
    background-position: 100% 50%; 
  }
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% { 
    transform: translateX(-50%) translateY(0); 
  }
  40% { 
    transform: translateX(-50%) translateY(-10px); 
  }
  60% { 
    transform: translateX(-50%) translateY(-5px); 
  }
}

@keyframes pulse {
  0% { 
    box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3); 
  }
  50% { 
    box-shadow: 0 15px 40px rgba(102, 126, 234, 0.5); 
  }
  100% { 
    box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3); 
  }
}

@keyframes pageLoad {
  from { 
    opacity: 0; 
  }
  to { 
    opacity: 1; 
  }
}


@media (max-width: 768px) {
  .nav-grid {
    grid-template-columns: 1fr;
  }
  
  .topic-section {
    padding: 30px 20px;
  }
  
  .examples-grid {
    grid-template-columns: 1fr;
  }
  
  .verb-tables {
    grid-template-columns: 1fr;
  }
  
  .main-title {
    font-size: 3rem;
  }
}

@media (max-width: 480px) {
  .header-content {
    padding: 0 10px;
  }
  
  .topic-section {
    padding: 20px 15px;
    margin-bottom: 20px;
  }
  
  .nav-card {
    padding: 20px;
  }
  
  .content-container {
    padding: 40px 10px;
  }
}
</style>


  <header>
    <div class="header-content">
      <h1 class="main-title">APRENDE INGLÉS</h1>
      <p class="subtitle">Domina los temas clave para avanzar en inglés de forma divertida e interactiva</p>
      
      <nav class="navigation">
        <div class="nav-grid">
          <a href="#past-simple" class="nav-card">
            <span class="card-icon">⏰</span>
            <div class="card-title">SIMPLE PAST</div>
            <div class="card-desc"></div>
          </a>
          
          <a href="#comparativos-superlativos" class="nav-card">
            <span class="card-icon">📊</span>
            <div class="card-title">COMPARATIVES AND SUPERLATIVES</div>
            <div class="card-desc"></div>
          </a>
          
          
          <a href="#present-prefect"  class="nav-card" >
            <span class="card-icon">🚀</span>
            <div class="card-title">PRESENT PERFECT</div>
            <div class="card-desc"></div>
          </a>
          
          <a href="#future-simple" class="nav-card">
            <span class="card-icon">💡</span>
            <div class="card-title">FUTURE SIMPLE</div>
            <div class="card-desc"></div>
          </a>

        </div>
      </nav>
    </div>
    
   
  </header>

  <div class="content-container">
    <section id="past-simple" class="topic-section">
      <h2 class="topic-title">📚 SIMPLE PAST</h2>
      <p class="topic-intro">El simple past en inglés se usa para describir acciones que ocurrieron y terminaron en un momento específico en el pasado. Se forma agregando -ed (o -d si el verbo termina en -e) a la forma infinitiva de los verbos regulares. Los verbos irregulares tienen formas de pasado únicas que deben memorizarse. </p>

      <div class="grammar-section">
        <h3 class="grammar-title">✅ 1. Forma Afirmativa</h3>
        <div class="formula-box">
          Sujeto + Verbo en Pasado + Complemento
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>🔄 Verbos Regulares</h4>
            <p>Agregan <strong>-ed</strong> al final</p>
            <p><em>"She <strong>visited</strong> her grandmother yesterday."</em></p>
          </div>
          
          <div class="example-card">
            <h4>⚡ Verbos Irregulares</h4>
            <p>Cambian su forma completamente</p>
            <p><em>"They <strong>went</strong> to the park last Sunday."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">❌ 2. Forma Negativa</h3>
        <div class="formula-box">
          Sujeto + did not (didn't) + Verbo Base + Complemento
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <p><em>"I <strong>did not watch</strong> TV."</em></p>
            <p><em>"She <strong>didn't visit</strong> her friend."</em></p>
          </div>
          <div class="example-card">
            <p><em>"He <strong>didn't eat</strong> the cake."</em></p>
            <p><em>"We <strong>didn't go</strong> to the party."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">❓ 3. Forma Interrogativa</h3>
        <div class="formula-box">
          Did + Sujeto + Verbo Base + Complemnto + question mark (?)
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <p><em>"Did you <strong>visit</strong> your cousin?"</em></p>
            <p><em>"Did they <strong>finish</strong> their homework?"</em></p>
          </div>
          <div class="example-card">
            <p><em>"Did she <strong>see</strong> the movie?"</em></p>
            <p><em>"Did he <strong>buy</strong> the book?"</em></p>
          </div>
        </div>
      </div>

      <div class="verb-tables">
        <div class="verb-table">
          <div class="table-header">Verbos Regulares</div>
          <div class="table-content">
            <div class="verb-pair"><span>walk</span><span>walked</span></div>
            <div class="verb-pair"><span>play</span><span>played</span></div>
            <div class="verb-pair"><span>study</span><span>studied</span></div>
            <div class="verb-pair"><span>watch</span><span>watched</span></div>
            <div class="verb-pair"><span>listen</span><span>listened</span></div>
          </div>
        </div>
        
        <div class="verb-table">
          <div class="table-header">Verbos Irregulares</div>
          <div class="table-content">
            <div class="verb-pair"><span>go</span><span>went</span></div>
            <div class="verb-pair"><span>eat</span><span>ate</span></div>
            <div class="verb-pair"><span>see</span><span>saw</span></div>
            <div class="verb-pair"><span>buy</span><span>bought</span></div>
            <div class="verb-pair"><span>come</span><span>came</span></div>
          </div>
        </div>
      </div>

      <div style="text-align: center;">
        <a href="file:///C:/Users/usuario/Downloads/html_file.html" class="play-button">JUGAR AHORA</a>
      </div>
    </section>

    <section id="comparativos-superlativos" class="topic-section">
      <h2 class="topic-title">📈 COMPARATIVES AND SUPERLATIVES</h2>
      <p class="topic-intro">Se usan para comparar cosas o personas, estableciendo diferencias o destacando características únicas.</p>

      <div class="grammar-section">
        <h3 class="grammar-title">⚖️ Comparativos</h3>
        <p>Los comparativos en inglés se utilizan para expresar diferencias entre dos elementos, utilizando adjetivos en grado comparativo. Se forman generalmente añadiendo "-er" al final de los adjetivos de una sílaba o utilizando "more" antes de los adjetivos más largos. También existen comparativos irregulares como "good" que se convierte en "better". </p>
        <div class="formula-box">
          Adjetivo + -er + thanㅤㅤㅤㅤㅤㅤ/ㅤㅤㅤㅤㅤㅤmore + adjetivo + than
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>📏 Adjetivos Cortos (1-2 sílabas)</h4>
            <p><em>"She is <strong>taller than</strong> her sister."</em></p>
            <p><em>"This book is <strong>easier than</strong> the other."</em></p>
            <p><em>"My car is <strong>faster than</strong> yours."</em></p>
          </div>
          
          <div class="example-card">
            <h4>📚 Adjetivos Largos (3+ sílabas)</h4>
            <p><em>"This movie is <strong>more interesting than</strong> the last one."</em></p>
            <p><em>"English is <strong>more difficult than</strong> Spanish."</em></p>
            <p><em>"She is <strong>more intelligent than</strong> him."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">🏆 Superlativos</h3>
        <p>En inglés, los superlativos (el grado más alto de un adjetivo) se forman de manera similar a los comparativos. Para adjetivos de una o dos sílabas, se añade "-est" al final del adjetivo y se agrega "the" antes del adjetivo. Para adjetivos de tres o más sílabas, se utiliza "the most" antes del adjetivo. </p>
        <div class="formula-box">
          the + adjetivo + -estㅤㅤㅤㅤㅤㅤ/ㅤㅤㅤㅤㅤㅤthe most + adjetivo
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>📏 Adjetivos Cortos</h4>
            <p><em>"He is <strong>the tallest</strong> in the class."</em></p>
            <p><em>"This is <strong>the easiest</strong> exercise."</em></p>
            <p><em>"She is <strong>the youngest</strong> student."</em></p>
          </div>
          
          <div class="example-card">
            <h4>📚 Adjetivos Largos</h4>
            <p><em>"This is <strong>the most beautiful</strong> place."</em></p>
            <p><em>"She is <strong>the most intelligent</strong> student."</em></p>
            <p><em>"It's <strong>the most expensive</strong> car."</em></p>
          </div>
        </div>
      </div>

      <div class="verb-tables">
      
        
        <div class="verb-table">
          <div class="table-header">Adjetivos Irregulares</div>
          <div class="table-content">
            <div class="verb-pair"><span>good</span><span>better / best</span></div>
            <div class="verb-pair"><span>bad</span><span>worse / worst</span></div>
            <div class="verb-pair"><span>far</span><span>farther / farthest</span></div>
            <div class="verb-pair"><span>little</span><span>less / least</span></div>
            <div class="verb-pair"><span>much/many</span><span>more / most</span></div>
          </div>
        </div>
      </div>

      <div style="text-align: center;">
        <a href="file:///C:/Users/usuario/Downloads/comparativos.html" class="play-button">JUGAR AHORA</a>
      </div>
    </section>

    <section id="present-prefect" class="topic-section">
      <h2 class="topic-title">🚀 PRESENT PERFECT</h2>
      <p class="topic-intro">El Presente Perfecto en inglés (Present Perfect) se forma con el verbo auxiliar "have" o "has" (dependiendo del sujeto) seguido del participio pasado (past participle o P.P) del verbo principal. Este tiempo verbal se utiliza para hablar de acciones que ocurrieron en el pasado, pero que tienen relevancia o un impacto en el presente. </p>

      <div class="grammar-section">
        <h3 class="grammar-title">✅ Forma Afirmativa</h3>
        
        <div class="formula-box">
          Sujeto + Has / Have + verbo P.P + Complemeto
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
             <h4>👥 Con Have (I, You, We, They)</h4>
            <p><em>"I <strong>have visited</strong> Paris twice."</em></p>
            <p><em>"They <strong>have finished</strong> their homework."</em></p>
            <p><em>"We <strong>have lived</strong> here for 5 years."</em></p>
          </div>
          
          <div class="example-card">
             <h4>👤 Con Has (He, She, It)</h4>
            <p><em>"She <strong>has worked</strong> there since 2020."</em></p>
            <p><em>"He <strong>has eaten</strong> breakfast already."</em></p>
            <p><em>"It <strong>has rained</strong> all morning."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">❌ Forma Negativa</h3>
        
        <div class="formula-box">
          Sujeto + Has not / Have not (Hasn´t / Haven´) + verbo P.P + Complemeto
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>👥 Haven't</h4>
            <p><em>"I <strong>haven't seen</strong> that movie."</em></p>
            <p><em>"They <strong>haven't arrived</strong> yet."</em></p>
            <p><em>"We <strong>haven't finished</strong> the project."</em></p>
          </div>
          
          <div class="example-card">
             <h4>👤 Hasn't</h4>
            <p><em>"She <strong>hasn't called</strong> me today."</em></p>
            <p><em>"He <strong>hasn't done</strong> his chores."</em></p>
            <p><em>"It <strong>hasn't stopped</strong> raining."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">❓ Forma Interrogativa</h3>
        
        <div class="formula-box">
           Has / Have + Sujeto + verbo P.P + Complemeto + question mark (?)
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
             <h4>👥 Have you...?</h4>
            <p><em>"<strong>Have you ever been</strong> to London?"</em></p>
            <p><em>"<strong>Have they finished</strong> their work?"</em></p>
            <p><em>"<strong>Have we met</strong> before?"</em></p>
          </div>
          
          <div class="example-card">
           <h4>👤 Has he/she...?</h4>
            <p><em>"<strong>Has she arrived</strong> yet?"</em></p>
            <p><em>"<strong>Has he studied</strong> for the exam?"</em></p>
            <p><em>"<strong>Has it been</strong> difficult?"</em></p>
          </div>
        </div>
      </div>

      <div class="verb-tables">
        <div class="verb-table">
          <div class="table-header">Participios Regulares</div>
          <div class="table-content">
            <div class="verb-pair"><span>work</span><span>worked</span></div>
            <div class="verb-pair"><span>study</span><span>studied</span></div>
            <div class="verb-pair"><span>play</span><span>played</span></div>
            <div class="verb-pair"><span>watch</span><span>watched</span></div>
            <div class="verb-pair"><span>listen</span><span>listened</span></div>
          </div>
        </div>
        
        <div class="verb-table">
          <div class="table-header">Participios Irregulares</div>
          <div class="table-content">
            <div class="verb-pair"><span>go</span><span>gone</span></div>
            <div class="verb-pair"><span>eat</span><span>eaten</span></div>
            <div class="verb-pair"><span>see</span><span>seen</span></div>
            <div class="verb-pair"><span>do</span><span>done</span></div>
            <div class="verb-pair"><span>write</span><span>written</span></div>
          </div>
        </div>
      </div>

      <div style="text-align: center;">
        <a href="file:///C:/Users/usuario/Downloads/presentperfect.html" class="play-button">JUGAR AHORA</a>
      </div>
    </section>

    <section id="future-simple" class="topic-section">
      <h2 class="topic-title">🚀 FUTURE SIMPLE</h2>
      <p class="topic-intro">El Presente Perfecto en inglés (Present Perfect) se forma con el verbo auxiliar "have" o "has" (dependiendo del sujeto) seguido del participio pasado (past participle) del verbo principal. Este tiempo verbal se utiliza para hablar de acciones que ocurrieron en el pasado, pero que tienen relevancia o un impacto en el presente. </p>

      <div class="grammar-section">
        <h3 class="grammar-title">✅ Forma Afirmativa</h3>
        
        <div class="formula-box">
          Sujeto + will + verbo + Complemeto
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>🔮 Predicciones</h4>
            <p><em>"It <strong>will rain</strong> tomorrow."</em></p>
            <p><em>"She <strong>will be</strong> a great doctor."</em></p>
            <p><em>"The team <strong>will win</strong> the match."</em></p>
          </div>
          
          <div class="example-card">
             <h4>💭 Decisiones Espontáneas</h4>
            <p><em>"I <strong>will help</strong> you with that."</em></p>
            <p><em>"We <strong>will go</strong> to the cinema tonight."</em></p>
            <p><em>"He <strong>will call</strong> you later."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">❌ Forma Negativa</h3>
        
        <div class="formula-box">
          Sujeto + will not (won´t) + verbo + Complemeto
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>🚫 Will not</h4>
            <p><em>"I <strong>will not forget</strong> your birthday."</em></p>
            <p><em>"They <strong>will not arrive</strong> on time."</em></p>
            <p><em>"It <strong>will not be</strong> easy."</em></p>
          </div>
          
          <div class="example-card">
            <h4>🚫 Won't (Contracción)</h4>
            <p><em>"She <strong>won't come</strong> to the party."</em></p>
            <p><em>"We <strong>won't finish</strong> today."</em></p>
            <p><em>"He <strong>won't understand</strong> this."</em></p>
          </div>
        </div>
      </div>  

      <div class="grammar-section">
        <h3 class="grammar-title">❓ Forma Interrogativa</h3>
        
        <div class="formula-box">
         Will + Sujeto + verbo + Complemeto + question mark (?)
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>❓ Preguntas Generales</h4>
            <p><em>"<strong>Will you come</strong> to my party?"</em></p>
            <p><em>"<strong>Will they finish</strong> the project?"</em></p>
            <p><em>"<strong>Will it rain</strong> tomorrow?"</em></p>
          </div>
          
          <div class="example-card">
           <h4>❓ Preguntas con Wh-</h4>
            <p><em>"<strong>When will you arrive</strong>?"</em></p>
            <p><em>"<strong>What will she do</strong> next?"</em></p>
            <p><em>"<strong>Where will we meet</strong>?"</em></p>
          </div>
        </div>
      </div>

       <div class="grammar-section">
        <h3 class="grammar-title">✅ Forma Afirmativa</h3>
        
        <div class="formula-box">
          Sujeto + be going to + verbo + Complemeto
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>🔮 Predicciones</h4>
            <p><em>"It<strong>is going to rain</strong> tomorrow."</em></p>
            <p><em>"She <strong>is going to win</strong> the competition."</em></p>
            <p><em>"They <strong>are going to travel</strong> to Spain next year."</em></p>
          </div>
          
          <div class="example-card">
             <h4>💭 Decisiones Planificadas</h4>
            <p><em>"I <strong>am going to start </strong> a new diet next week."</em></p>
            <p><em>"We <strong>are going to visit</strong> our grandparents this weekend."</em></p>
            <p><em>"He <strong>is going to buy</strong> a new laptop tomorrow."</em></p>
          </div>
        </div>
      </div>

      <div class="grammar-section">
        <h3 class="grammar-title">❌ Forma Negativa</h3>
        
        <div class="formula-box">
          Sujeto + not going to + verbo + Complemeto
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>🚫 am-is-are/not</h4>
            <p><em>"I am <strong> not going to watch</strong> TV tonight."</em></p>
            <p><em>"They are <strong>not going to play</strong> soccer today."</em></p>
            <p><em>"He is<strong>not going to eat</strong>  dessert."</em></p>
          </div>
          
          <div class="example-card">
            <h4>🚫 aren't-isn't(Contracción)</h4>
            <p><em>"She <strong>isn't going to attend</strong>  the meeting."</em></p>
            <p><em>"We <strong>aren't going to travel</strong> this summer."</em></p>
            <p><em>"He <strong> isn't going to eat</strong> dessert."</em></p>
          </div>
        </div>
      </div>  

      <div class="grammar-section">
        <h3 class="grammar-title">❓ Forma Interrogativa</h3>
        
        <div class="formula-box">
          Sujeto + going to + verbo + Complemeto + question mark (?)
        </div>
        
        <div class="examples-grid">
          <div class="example-card">
            <h4>❓ Preguntas Generales</h4>
            <p><em>"Are you<strong> going to study</strong> tonight?"</em></p>
            <p><em>"Is she<strong>going to buy</strong> a new phone?"</em></p>
            <p><em>"Are they <strong>going to visit</strong> us this weekend?"</em></p>
          </div>
          
          <div class="example-card">
           <h4>❓ Preguntas con Wh-</h4>
            <p><em>"What are<strong> you going to do</strong>  tomorrow?"</em></p>
            <p><em>"Where is<strong> she going to travel</strong> next summer?"</em></p>
            <p><em>"Why is<strong>he going to quit</strong> his job?"</em></p>
          </div>
        </div>
      </div>

      <div class="verb-tables">
      
        
        <div class="verb-tables">
        <div class="verb-table">
          <div class="table-header">Usos del Future Simple</div>
          <div class="table-content">
            <div class="verb-pair"><span>Predicciones</span><span>It will be sunny</span></div>
            <div class="verb-pair"><span>Promesas</span><span>I will help you</span></div>
            <div class="verb-pair"><span>Decisiones</span><span>I'll take the bus</span></div>
            <div class="verb-pair"><span>Ofertas</span><span>I'll carry that</span></div>
            <div class="verb-pair"><span>Amenazas</span><span>I'll tell mom!</span></div>
          </div>
        </div>
        
        <div class="verb-table">
          <div class="table-header">Expresiones de Tiempo</div>
          <div class="table-content">
            <div class="verb-pair"><span>tomorrow</span><span>mañana</span></div>
            <div class="verb-pair"><span>next week</span><span>próxima semana</span></div>
            <div class="verb-pair"><span>in the future</span><span>en el futuro</span></div>
            <div class="verb-pair"><span>soon</span><span>pronto</span></div>
            <div class="verb-pair"><span>later</span><span>más tarde</span></div>
          </div>
        </div>
      </div>
      

      </div>
       <div style="text-align: center;">
        <a href="file:///C:/Users/usuario/Downloads/futuretense.html" class="play-button">JUGAR AHORA</a>
      </div>


    </section>  

      

  </div>

  <footer>
    <p>© 2025 Aprende Inglés Fácil | Diseñado con ❤️ para tu aprendizaje</p>
  </footer>
</body>
</html>
