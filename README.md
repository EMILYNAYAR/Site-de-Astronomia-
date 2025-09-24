

  return (
    <div className="min-h-screen bg-gray-900 text-white">
      {/* Header */}
      <header className="bg-black/50 backdrop-blur-sm border-b border-gray-700 sticky top-0 z-50">
        <div className="container mx-auto px-4 py-4">
          <div className="flex items-center justify-between">
            <div className="flex items-center space-x-2">
              <div className="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center">
                <span className="text-white font-bold text-lg">🌌</span>
              </div>
              <h1 className="text-2xl font-bold text-blue-400">AstroExplora</h1>
            </div>
            
            <nav className="hidden md:flex space-x-6">
              <a href="#inicio" className="text-white hover:text-blue-400 transition-colors">Início</a>
              <a href="#sistema-solar" className="text-white hover:text-blue-400 transition-colors">Sistema Solar</a>
              <a href="#galeria" className="text-white hover:text-blue-400 transition-colors">Galeria</a>
              <a href="#sobre" className="text-white hover:text-blue-400 transition-colors">Sobre</a>
            </nav>
            
            <button className="md:hidden p-2">
              <svg className="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M4 6h16M4 12h16M4 18h16" />
              </svg>
            </button>
          </div>
        </div>
      </header>

      {/* Hero Section */}
      <section id="inicio" className="relative h-screen flex items-center justify-center overflow-hidden">
        <div className="absolute inset-0 z-0">
          <img 
            src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
            alt="Vast night sky filled with stars, nebula clouds, and the milky way galaxy stretching across the cosmos"
            className="w-full h-full object-cover"
          />
          <div className="absolute inset-0 bg-black/70"></div>
        </div>
        
        <div className="relative z-10 text-center px-4 max-w-4xl">
          <h2 className="text-5xl md:text-7xl font-bold mb-6 text-white">Explorando o Cosmos</h2>
          <p className="text-xl md:text-2xl mb-8 text-gray-300">
            Descubra as maravilhas do universo e os segredos do nosso sistema solar
          </p>
          <button className="bg-blue-600 text-white px-8 py-3 rounded-lg font-semibold hover:bg-blue-700 transition-colors">
            Começar Exploração
          </button>
        </div>
      </section>

      {/* Sistema Solar Section */}
      <section id="sistema-solar" className="py-20 bg-gray-800/30">
        <div className="container mx-auto px-4">
          <h2 className="text-4xl font-bold text-center mb-16 text-blue-400">Nosso Sistema Solar</h2>
          
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
            {/* Mercury */}
            <div 
              className="bg-gray-800 rounded-xl p-6 shadow-lg hover:shadow-xl transition-shadow cursor-pointer"
              onMouseEnter={() => setActivePlanet("Mercúrio")}
              onMouseLeave={() => setActivePlanet(null)}
            >
              <div className="w-20 h-20 bg-yellow-200 rounded-full mx-auto mb-4 flex items-center justify-center">
                <span className="text-gray-800 text-2xl">☿</span>
              </div>
              <h3 className="text-xl font-semibold text-center mb-2 text-white">Mercúrio</h3>
              <p className="text-gray-400 text-center">O planeta mais próximo do Sol e o menor do sistema solar</p>
            </div>

            {/* Venus */}
            <div 
              className="bg-gray-800 rounded-xl p-6 shadow-lg hover:shadow-xl transition-shadow cursor-pointer"
              onMouseEnter={() => setActivePlanet("Vênus")}
              onMouseLeave={() => setActivePlanet(null)}
            >
              <div className="w-20 h-20 bg-yellow-100 rounded-full mx-auto mb-4 flex items-center justify-center">
                <span className="text-gray-800 text-2xl">♀</span>
              </div>
              <h3 className="text-xl font-semibold text-center mb-2 text-white">Vênus</h3>
              <p className="text-gray-400 text-center">O segundo planeta do sistema solar, conhecido como estrela d'alva</p>
            </div>

            {/* Earth */}
            <div 
              className="bg-gray-800 rounded-xl p-6 shadow-lg hover:shadow-xl transition-shadow cursor-pointer"
              onMouseEnter={() => setActivePlanet("Terra")}
              onMouseLeave={() => setActivePlanet(null)}
            >
              <div className="w-20 h-20 bg-blue-500 rounded-full mx-auto mb-4 flex items-center justify-center">
                <span className="text-white text-2xl">🌍</span>
              </div>
              <h3 className="text-xl font-semibold text-center mb-2 text-white">Terra</h3>
              <p className="text-gray-400 text-center">Nosso planeta natal, o único conhecido por abrigar vida</p>
            </div>

            {/* Mars */}
            <div 
              className="bg-gray-800 rounded-xl p-6 shadow-lg hover:shadow-xl transition-shadow cursor-pointer"
              onMouseEnter={() => setActivePlanet("Marte")}
              onMouseLeave={() => setActivePlanet(null)}
            >
              <div className="w-20 h-20 bg-red-500 rounded-full mx-auto mb-4 flex items-center justify-center">
                <span className="text-white text-2xl">♂</span>
              </div>
              <h3 className="text-xl font-semibold text-center mb-2 text-white">Marte</h3>
              <p className="text-gray-400 text-center">O planeta vermelho, alvo de exploração e possível colonização</p>
            </div>
          </div>

          {activePlanet && (
            <div className="mt-12 bg-gray-800 rounded-xl p-8 shadow-lg">
              <h3 className="text-2xl font-semibold mb-4 text-white">Informações sobre {activePlanet}</h3>
              <p className="text-gray-300">
                {activePlanet === "Mercúrio" && "Mercúrio é o menor e mais interno planeta do Sistema Solar, orbitando o Sol a cada 87,969 dias terrestres."}
                {activePlanet === "Vênus" && "Vênus é o segundo planeta do Sistema Solar em ordem de distância a partir do Sol, orbitando-o a cada 224,7 dias."}
                {activePlanet === "Terra" && "A Terra é o terceiro planeta mais próximo do Sol, o mais denso e o quinto maior dos oito planetas do Sistema Solar."}
                {activePlanet === "Marte" && "Marte é o quarto planeta a partir do Sol, o segundo menor do Sistema Solar, atrás apenas de Mercúrio."}
              </p>
            </div>
          )}
        </div>
      </section>

      {/* Galeria */}
      <section id="galeria" className="py-20 bg-gray-900">
        <div className="container mx-auto px-4">
          <h2 className="text-4xl font-bold text-center mb-16 text-blue-400">Galeria Espacial</h2>
          
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div className="bg-gray-800 rounded-xl overflow-hidden shadow-lg">
              <img 
                src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                alt="Colorful nebula cloud with vibrant hues of pink, blue and purple cosmic dust forming star nursery"
                className="w-full h-48 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-semibold mb-2 text-white">Nebulosa de Orion</h3>
                <p className="text-gray-400">Uma das nebulosas mais brilhantes, visível a olho nu no céu noturno.</p>
              </div>
            </div>

            <div className="bg-gray-800 rounded-xl overflow-hidden shadow-lg">
              <img 
                src="https://images.unsplash.com/photo-1533465117350-0e8a6b7c4d8f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                alt="Saturn with its iconic rings surrounded by stars in the blackness of space"
                className="w-full h-48 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-semibold mb-2 text-white">Saturno e Seus Anéis</h3>
                <p className="text-gray-400">O sexto planeta do Sistema Solar, famoso por seu complexo sistema de anéis.</p>
              </div>
            </div>

            <div className="bg-gray-800 rounded-xl overflow-hidden shadow-lg">
              <img 
                src="https://images.unsplash.com/photo-1559152283-0a0956a5a95b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                alt="Total solar eclipse showing the sun's corona and solar prominences during totality"
                className="w-full h-48 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-semibold mb-2 text-white">Eclipse Solar Total</h3>
                <p className="text-gray-400">Fenômeno astronômico que ocorre quando a Lua passa entre a Terra e o Sol.</p>
              </div>
            </div>

            <div className="bg-gray-800 rounded-xl overflow-hidden shadow-lg">
              <img 
                src="https://images.unsplash.com/photo-1462331940025-496dfbfc7564?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" 
                alt="The milky way galaxy stretching across a dark night sky above a mountain landscape"
                className="w-full h-48 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-semibold mb-2 text-white">Via Láctea</h3>
                <p className="text-gray-400">Nossa galácia espiral, lar de bilhões de estrelas incluindo o nosso Sol.</p>
              </div>
            </div>

            <div className="bg-gray-800 rounded-xl overflow-hidden shadow-lg">
              <img 
                src="https://images.unsplash.com/photo-1563299796-1751d3653a8f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                alt="International Space Station orbiting above Earth with visible solar panels and modules"
                className="w-full h-48 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-semibold mb-2 text-white">Estação Espacial</h3>
                <p className="text-gray-400">Laboratório orbital que serve como base para pesquisas em microgravidade.</p>
              </div>
            </div>

            <div className="bg-gray-800 rounded-xl overflow-hidden shadow-lg">
              <img 
                src="https://images.unsplash.com/photo-1540979388789-6cee28a1cdc9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" 
                alt="Northern lights aurora borealis with green and purple curtains over snowy mountain landscape"
                className="w-full h-48 object-cover"
              />
              <div className="p-4">
                <h3 className="text-xl font-semibold mb-2 text-white">Aurora Boreal</h3>
                <p className="text-gray-400">Fenômeno luminoso que ocorre nas regiões polares devido à interação solar.</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer id="sobre" className="bg-gray-800 text-gray-400 py-12">
        <div className="container mx-auto px-4">
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div>
              <h3 className="text-xl font-semibold mb-4 text-white">AstroExplora</h3>
              <p>Explorando as maravilhas do universo e compartilhando o conhecimento astronômico com todos.</p>
            </div>
            
            <div>
              <h3 className="text-xl font-semibold mb-4 text-white">Links Rápidos</h3>
              <ul className="space-y-2">
                <li><a href="#inicio" className="hover:text-blue-400 transition-colors">Início</a></li>
                <li><a href="#sistema-solar" className="hover:text-blue-400 transition-colors">Sistema Solar</a></li>
                <li><a href="#galeria" className="hover:text-blue-400 transition-colors">Galeria</a></li>
              </ul>
            </div>
            
            <div>
              <h3 className="text-xl font-semibold mb-4 text-white">Contato</h3>
              <p>Email: contato@astroexplora.com</p>
              <p className="mt-2">Siga-nos nas redes sociais</p>
              <div className="flex space-x-4 mt-2">
                <a href="#" className="hover:text-blue-400 transition-colors">Twitter</a>
                <a href="#" className="hover:text-blue-400 transition-colors">Instagram</a>
                <a href="#" className="hover:text-blue-400 transition-colors">YouTube</a>
              </div>
            </div>
          </div>
          
          <div className="border-t border-gray-700 mt-8 pt-8 text-center">
            <p>&copy; 2024 AstroExplora. Todos os direitos reservados.</p>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default AstronomyWebsite;
