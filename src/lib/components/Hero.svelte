<script>
  let activeTab = 'USDC';
  const tabs = ['USDC', 'USDT', 'DAI', 'Multi-chain'];
</script>

<section class="pt-32 pb-20 px-6 max-w-7xl mx-auto">
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
    <div>
      <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-white leading-[1.1] mb-8">
        Turn stablecoins into <br /> spendable currency
      </h1>
    </div>
    <div class="flex flex-col justify-end items-start lg:pl-12">
      <p class="text-xl text-gray-400 mb-6 max-w-md leading-relaxed">
        Access your crypto wealth globally. Convert stablecoins to local currency instantly with multi-chain support and zero banking fees.
      </p>
      <a href="#" class="group inline-flex items-center text-white font-medium hover:opacity-70 transition-opacity">
        Get Started 
        <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
      </a>
    </div>
  </div>

  <!-- Interactive Visual Section -->
  <div class="rounded-3xl overflow-hidden bg-gray-950 border border-gray-900 shadow-sm">
    <!-- Tabs -->
    <div class="flex overflow-x-auto scrollbar-hide border-b border-gray-900 bg-black/50 backdrop-blur-sm">
      {#each tabs as tab}
        <button 
          class="px-5 py-4 text-sm font-medium whitespace-nowrap transition-colors relative {activeTab === tab ? 'text-white' : 'text-gray-500 hover:text-gray-300'}"
          on:click={() => activeTab = tab}
        >
          {tab}
          {#if activeTab === tab}
            <div class="absolute bottom-0 left-0 right-0 h-0.5 bg-primary-500"></div>
          {/if}
        </button>
      {/each}
    </div>

    <!-- Content Area -->
    <div class="relative h-[500px] bg-gradient-to-br from-primary-500 to-primary-700 overflow-hidden group">
      <!-- Background Pattern -->
      <div class="absolute inset-0 opacity-10">
        <div class="absolute inset-0" style="background-image: radial-gradient(circle at 2px 2px, white 1px, transparent 0); background-size: 40px 40px;"></div>
      </div>
      
      <!-- Floating UI Card -->
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-80 bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-5 text-white shadow-2xl">
        <div class="flex justify-between items-center mb-6">
          <span class="text-xs font-medium text-white/80">Convert & Spend</span>
          <span class="text-xs font-medium text-white/60">Instant</span>
        </div>
        
        <!-- Conversion Display -->
        <div class="bg-white/10 backdrop-blur-sm rounded-xl p-4 mb-4">
          <div class="flex items-center justify-between mb-3">
            <div class="flex items-center gap-2">
              <div class="w-8 h-8 rounded-full bg-blue-500 flex items-center justify-center text-white text-xs font-bold">
                $
              </div>
              <span class="text-sm font-medium">USDC</span>
            </div>
            <span class="text-lg font-bold">500.00</span>
          </div>
          <div class="flex justify-center my-2">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <path d="M12 5v14M19 12l-7 7-7-7"/>
            </svg>
          </div>
          <div class="flex items-center justify-between">
            <div class="flex items-center gap-2">
              <div class="w-8 h-8 rounded-full bg-green-500 flex items-center justify-center text-white text-xs font-bold">
                $
              </div>
              <span class="text-sm font-medium">USD</span>
            </div>
            <span class="text-lg font-bold">499.50</span>
          </div>
        </div>

        <!-- Transaction Details -->
        <div class="space-y-2 text-xs">
          <div class="flex justify-between text-white/60">
            <span>Network Fee</span>
            <span class="text-white">$0.50</span>
          </div>
          <div class="flex justify-between text-white/60">
            <span>Processing Time</span>
            <span class="text-white">~2 seconds</span>
          </div>
          <div class="flex justify-between text-white/60">
            <span>Chain</span>
            <span class="text-white">Ethereum</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Code Block -->
    <div class="bg-black p-6 border-t border-gray-900 overflow-x-auto">
      <pre class="font-mono text-xs leading-relaxed text-gray-400">
<span class="text-gray-600 select-none">1</span>  <span class="text-gray-600"># Convert USDC to local currency in one API call</span>
<span class="text-gray-600 select-none">2</span>
<span class="text-gray-600 select-none">3</span>  <span class="text-primary-400">curl</span> <span class="text-primary-300">-X POST</span> <span class="text-green-400">'https://api.stables.money/v1/convert'</span> \
<span class="text-gray-600 select-none">4</span>    <span class="text-primary-300">-H</span> <span class="text-green-400">'Authorization: Bearer YOUR_API_KEY'</span> \
<span class="text-gray-600 select-none">5</span>    <span class="text-primary-300">-H</span> <span class="text-green-400">'Content-Type: application/json'</span> \
<span class="text-gray-600 select-none">6</span>    <span class="text-primary-300">-d</span> '&#123;
<span class="text-gray-600 select-none">7</span>      <span class="text-blue-400">"from"</span>: &#123;
<span class="text-gray-600 select-none">8</span>        <span class="text-blue-400">"currency"</span>: <span class="text-green-400">"USDC"</span>,
<span class="text-gray-600 select-none">9</span>        <span class="text-blue-400">"amount"</span>: <span class="text-green-400">"500"</span>,
<span class="text-gray-600 select-none">10</span>       <span class="text-blue-400">"chain"</span>: <span class="text-green-400">"ethereum"</span>
<span class="text-gray-600 select-none">11</span>     &#125;,
<span class="text-gray-600 select-none">12</span>     <span class="text-blue-400">"to"</span>: &#123;
<span class="text-gray-600 select-none">13</span>       <span class="text-blue-400">"currency"</span>: <span class="text-green-400">"USD"</span>,
<span class="text-gray-600 select-none">14</span>       <span class="text-blue-400">"destination"</span>: <span class="text-green-400">"bank_account_id"</span>
<span class="text-gray-600 select-none">15</span>     &#125;
<span class="text-gray-600 select-none">16</span>   &#125;'</pre>
    </div>
  </div>
</section>
