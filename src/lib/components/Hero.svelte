<script>
  let activeTab = 'Cross-border';
  const tabs = ['Payouts', 'Rewards', 'Cross-border', 'Ramps', 'FX', 'Payroll', 'Billing', 'Debit Cards', 'Treasury', 'Node management'];
</script>

<section class="pt-32 pb-20 px-6 max-w-7xl mx-auto">
  <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 mb-16">
    <div>
      <h1 class="text-5xl md:text-6xl font-medium tracking-tight text-black leading-[1.1] mb-8">
        Products and APIs <br /> for moving money
      </h1>
    </div>
    <div class="flex flex-col justify-end items-start lg:pl-12">
      <p class="text-xl text-gray-600 mb-6 max-w-md leading-relaxed">
        Simple developer tools to send value instantly anywhere in the world on an open network.
      </p>
      <a href="#" class="group inline-flex items-center text-black font-medium hover:opacity-70 transition-opacity">
        Explore Grid 
        <span class="ml-1 group-hover:translate-x-1 transition-transform">→</span>
      </a>
    </div>
  </div>

  <!-- Interactive Visual Section -->
  <div class="rounded-3xl overflow-hidden bg-gray-50 border border-gray-200 shadow-sm">
    <!-- Tabs -->
    <div class="flex overflow-x-auto scrollbar-hide border-b border-gray-200 bg-white/50 backdrop-blur-sm">
      {#each tabs as tab}
        <button 
          class="px-5 py-4 text-sm font-medium whitespace-nowrap transition-colors relative {activeTab === tab ? 'text-black' : 'text-gray-500 hover:text-gray-800'}"
          on:click={() => activeTab = tab}
        >
          {tab}
          {#if activeTab === tab}
            <div class="absolute bottom-0 left-0 right-0 h-0.5 bg-black"></div>
          {/if}
        </button>
      {/each}
    </div>

    <!-- Content Area -->
    <div class="relative h-[500px] bg-[#C19A6B] overflow-hidden group">
      <!-- Background Image Placeholder (Desert) -->
      <img 
        src="https://images.unsplash.com/photo-1509316975850-ff9c5deb0cd9?q=80&w=2560&auto=format&fit=crop" 
        alt="Desert landscape" 
        class="absolute inset-0 w-full h-full object-cover opacity-90 transition-transform duration-700 group-hover:scale-105"
      />
      
      <!-- Floating UI Card -->
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-80 bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-4 text-white shadow-2xl">
        <div class="flex justify-between items-center mb-6">
          <span class="text-xs font-medium text-white/80">Earning 3.0% on every purchase</span>
        </div>
        
        <!-- Transaction 1 -->
        <div class="flex items-center gap-3 mb-4">
          <div class="w-10 h-10 rounded-full bg-orange-500 flex items-center justify-center text-white shrink-0">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm4.5-8c0-1.71-1.39-3.1-3.1-3.1h-4V7H7v2h2.5v8H7v2h2.4v2h2.5v-2h1.5c1.71 0 3.1-1.39 3.1-3.1 0-1.21-.69-2.26-1.7-2.75.99-.49 1.7-1.54 1.7-2.75z"/></svg>
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline">
              <h3 class="text-sm font-medium truncate">BTC Cashback</h3>
              <span class="text-sm font-medium">+ 0.00004</span>
            </div>
            <div class="flex justify-between items-baseline">
              <p class="text-xs text-white/60">Just now</p>
              <p class="text-xs text-white/60">~ $4.84</p>
            </div>
          </div>
        </div>

        <!-- Transaction 2 -->
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 rounded-full bg-white flex items-center justify-center text-gray-900 shrink-0">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 8h1a4 4 0 0 1 0 8h-1"></path><path d="M2 8h16v9a4 4 0 0 1-4 4H6a4 4 0 0 1-4-4V8z"></path><line x1="6" y1="1" x2="6" y2="4"></line><line x1="10" y1="1" x2="10" y2="4"></line><line x1="14" y1="1" x2="14" y2="4"></line></svg>
          </div>
          <div class="flex-1 min-w-0">
            <div class="flex justify-between items-baseline">
              <h3 class="text-sm font-medium truncate">Coffee Kings</h3>
              <span class="text-sm font-medium">$4.92</span>
            </div>
            <div class="flex justify-between items-baseline">
              <p class="text-xs text-white/60">1h ago</p>
              <div class="px-1.5 py-0.5 rounded bg-white/20 text-[10px] font-medium">3%</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Code Block -->
    <div class="bg-gray-50 p-6 border-t border-gray-200 overflow-x-auto">
      <pre class="font-mono text-xs leading-relaxed text-gray-600">
<span class="text-gray-400 select-none">1</span>  <span class="text-gray-400"># Convert USD -> BTC and push to a spark wallet in one request</span>
<span class="text-gray-400 select-none">2</span>
<span class="text-gray-400 select-none">3</span>  <span class="text-purple-600">curl</span> <span class="text-blue-600">-X POST</span> <span class="text-green-600">'https://api.lightspark.com/grid/2025-10-13/quotes'</span> \
<span class="text-gray-400 select-none">4</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Authorization: Basic <base64-encoded-credentials>'</span> \
<span class="text-gray-400 select-none">5</span>    <span class="text-blue-600">-H</span> <span class="text-green-600">'Content-Type: application/json'</span> \
<span class="text-gray-400 select-none">6</span>    <span class="text-blue-600">-d</span> '&#123;
<span class="text-gray-400 select-none">7</span>      <span class="text-blue-800">"source"</span>: &#123;
<span class="text-gray-400 select-none">8</span>        <span class="text-blue-800">"accountId"</span>: <span class="text-green-600">"InternalAccount:e85dcbd6-dced-4ec4-b756-3c3a9ea3d965"</span>
<span class="text-gray-400 select-none">9</span>      &#125;,
<span class="text-gray-400 select-none">10</span>     <span class="text-blue-800">"destination"</span>: &#123;
<span class="text-gray-400 select-none">11</span>       <span class="text-blue-800">"externalAccountDetails"</span>: &#123;
<span class="text-gray-400 select-none">12</span>         <span class="text-blue-800">"customerId"</span>: <span class="text-green-600">"Customer:019542f5-b3e7-1d02-0000-000000000001"</span>,</pre>
    </div>
  </div>
</section>
