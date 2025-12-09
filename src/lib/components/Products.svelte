<script>
  // No script needed
</script>

<div class="space-y-32 pb-32">
  <!-- Grid Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Grid</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Commands for money.</strong> One API/SDK to send, receive, and settle value globally—fiat, stablecoins, or bitcoin. Always real-time, always low cost.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View docs</a>
      </div>
    </div>
    <div class="bg-gray-50 rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Grid Visualization -->
      <div class="relative w-full max-w-md">
        <div class="flex justify-between items-center">
          <!-- Central Hub -->
          <div class="w-16 h-16 bg-black rounded-lg flex items-center justify-center relative z-10">
            <svg width="32" height="32" viewBox="0 0 24 24" fill="white"><path d="M3 3h7v7H3V3zm11 0h7v7h-7V3zm0 11h7v7h-7v-7zM3 14h7v7H3v-7z"/></svg>
          </div>
          
          <!-- Endpoints -->
          <div class="flex flex-col gap-3">
            {#each ['Send', 'Receive', 'Convert', 'Hold', 'Ramp', 'Program', 'Identity'] as item, i}
              <div class="flex items-center gap-4">
                <div class="w-24 h-[1px] bg-gradient-to-r from-black/20 to-transparent transform rotate-180 origin-left"></div>
                <div class="flex items-center gap-2">
                  <div class="w-3 h-3 rounded-full" style="background-color: hsl({i * 50}, 70%, 50%)"></div>
                  <span class="text-xs font-medium text-gray-600">{item}</span>
                </div>
              </div>
            {/each}
          </div>
        </div>
        <!-- Connecting lines (simplified) -->
        <svg class="absolute inset-0 w-full h-full pointer-events-none" style="z-index: 0;">
          <defs>
            <linearGradient id="lineGradient" x1="0%" y1="0%" x2="100%" y2="0%">
              <stop offset="0%" stop-color="#000" stop-opacity="0.1" />
              <stop offset="100%" stop-color="#000" stop-opacity="0" />
            </linearGradient>
          </defs>
          <!-- Curved lines would go here, but using straight CSS lines above for simplicity -->
        </svg>
      </div>
    </div>
  </section>

  <!-- Connect Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Connect</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">Enterprise-grade Bitcoin.</strong> Lightspark handles node management, key management, liquidity, channel balancing, and routing—so your team can focus on product development and growth.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View docs</a>
      </div>
    </div>
    <div class="bg-[#E8F5E9] rounded-3xl overflow-hidden min-h-[400px] relative">
      <div class="absolute inset-0 p-8 font-mono text-xs leading-none text-[#4CAF50] opacity-50 break-all overflow-hidden select-none">
        {Array(2000).fill(0).map(() => Math.random().toString(36).substring(2, 3)).join('')}
      </div>
      <div class="absolute inset-0 bg-gradient-to-b from-transparent to-[#E8F5E9]"></div>
    </div>
  </section>

  <!-- Spark Section -->
  <section class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
    <div>
      <h3 class="text-4xl font-medium mb-6">Spark</h3>
      <p class="text-xl text-gray-600 mb-8 leading-relaxed">
        <strong class="text-black">A powerful Bitcoin Layer 2.</strong> Move bitcoin and bitcoin-native assets (including stablecoins) instantly, at near-zero cost, while staying fully connected to Bitcoin's infrastructure.
      </p>
      <div class="flex flex-col gap-2">
        <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
          Learn more 
          <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
        </a>
        <a href="#" class="text-sm text-gray-400 hover:text-black transition-colors">View docs</a>
      </div>
    </div>
    <div class="bg-black rounded-3xl p-12 flex items-center justify-center min-h-[400px]">
      <!-- Phone Mockup -->
      <div class="relative w-64 h-[500px] bg-gray-900 rounded-[3rem] border-8 border-gray-800 shadow-2xl overflow-hidden">
        <!-- Screen Content -->
        <div class="absolute inset-0 bg-black p-4 text-white">
          <div class="flex justify-between items-center mb-6 pt-2">
            <span class="text-xs font-medium">Wallet</span>
            <div class="w-6 h-6 rounded-full bg-gray-700"></div>
          </div>
          <div class="mb-8">
            <div class="text-2xl font-bold">$12,450.00</div>
            <div class="text-xs text-green-400">+2.4% today</div>
          </div>
          <div class="space-y-3">
             <div class="bg-gray-800/50 p-3 rounded-xl flex items-center gap-3">
               <div class="w-8 h-8 rounded-full bg-orange-500"></div>
               <div class="flex-1">
                 <div class="text-xs font-medium">Bitcoin</div>
                 <div class="text-[10px] text-gray-400">0.45 BTC</div>
               </div>
               <div class="text-xs">$12,300</div>
             </div>
             <div class="bg-gray-800/50 p-3 rounded-xl flex items-center gap-3">
               <div class="w-8 h-8 rounded-full bg-blue-500"></div>
               <div class="flex-1">
                 <div class="text-xs font-medium">USD Coin</div>
                 <div class="text-[10px] text-gray-400">150 USDC</div>
               </div>
               <div class="text-xs">$150.00</div>
             </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</div>
