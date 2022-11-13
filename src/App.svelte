<script>
  import carpetIcon from "./assets/carpeticon.png";
  import AnimatedElement from "./components/AnimatedElement.svelte";
  import Card from "./components/Card.svelte";
  import LinkButton from "./components/LinkButton.svelte";
  import Katex from "./components/Katex.svelte";
  import LoopingCoins from "./assets/coinsanimation.svg";
  import BTandRTFlow from "./assets/rtinvesting.svg";
  import TradingLoop from "./assets/trading.svg";
  import Lamp from "./assets/lamp.png";
  import { Tabs, Tab, TabList, TabPanel } from "svelte-tabs";
  import FaDiscord from "svelte-icons/fa/FaDiscord.svelte";
  import FaTwitter from "svelte-icons/fa/FaTwitter.svelte";
  import FaEnvelope from "svelte-icons/fa/FaEnvelope.svelte";
  import FaGithub from "svelte-icons/fa/FaGithub.svelte";
  import TiDocument from "svelte-icons/ti/TiDocument.svelte";

  const math = "price=\\frac{total backing}{carpet supply}";
</script>

<main class="flex flex-col text-white">
  <section
    class="flex flex-col justify-center w-full bg-gradient-to-b from-indigo-800 to-indigo-400"
  >
    <div class="text-center flex flex-col gap-6 p-4">
      <div class="flex flex-row justify-center">
        <img src={carpetIcon} alt="" class="w-48" />
      </div>
      <AnimatedElement>
        <h1 class="text-5xl font-bold">The number go up coin</h1>
      </AnimatedElement>
      <AnimatedElement
        ><div class="flex flex-row justify-center">
          <p class="text-xl max-w-5xl">
            Carpet DeFi is a low risk DeFi protocol around the CARPET token that
            always rises in value through Protocol Owned Liquidity 2.0 and a
            simple mathematical formula.
          </p>
        </div>
      </AnimatedElement>
      <div class="flex flex-row gap-6 justify-center mt-4">
        <!-- 
        <LinkButton href="https://app.carpetde.fi" text="Enter the dapp" />
        -->
        <LinkButton href="https://docs.carpetde.fi" text="Read the docs" />
      </div>
    </div>
    <div
      class="bubble bg-indigo-300 py-6 mt-8 sm:py-8 md:py-12 transition-all delay-200 ease-in"
    />
  </section>
  <section class="flex flex-col justify-center w-full bg-indigo-300">
    <div class="bg-carpets-rising">
      <div class="flex flex-row justify-center">
        <Card class="max-w-2xl mx-4" innerClass="text-center text-xl space-y-3">
          <h2 class="text-center text-2xl font-semibold uppercase">
            How does number go up work?
          </h2>

          <Tabs>
            <TabList>
              <Tab>Trading</Tab>
              <Tab>Lending</Tab>
              <Tab>Investing</Tab>
            </TabList>

            <TabPanel>
              <div class="space-y-6">
                <AnimatedElement>
                  <div class="flex flex-row justify-center">
                    <img src={TradingLoop} alt="" class="w-96" />
                  </div>
                </AnimatedElement>
                <AnimatedElement>
                  <div class="space-y-6">
                    <p>
                      You can only buy and sell CARPET with the Counter, our
                      protocol-owned exchange. CARPET is minted on buy and
                      burned on sell.
                    </p>
                    <p>
                      Each CARPET is backed by an amount of stablecoins in the
                      Backing Treasury. This calculation is a simple formula.
                    </p>
                    <p class="text-3xl"><Katex {math} /></p>
                    <p>
                      There is a trade tax, for example if you pay 1000$, you
                      might only get 700$ worth of CARPET. This fee serves to
                      grow the price.
                    </p>
                  </div>
                </AnimatedElement>
              </div>
            </TabPanel>

            <TabPanel>
              <div class="space-y-6">
                <AnimatedElement>
                  <div class="flex flex-row justify-center">
                    <img src={LoopingCoins} alt="" class="w-96" />
                  </div>
                </AnimatedElement>
                <AnimatedElement>
                  <div class="space-y-6">
                    <p>
                      While your tokens sit in the Backing Treasury, they don't
                      just collect dust. They are placed into DeFi lending
                      platforms such as Aave and other safe yield sources.
                    </p>
                    <p class="font-bold">
                      This means even without any trades, your stablecoins are
                      put to work inside safe yield sources to grow the backing
                      treasury further.
                    </p>
                  </div>
                </AnimatedElement>
              </div>
            </TabPanel>

            <TabPanel>
              <div class="space-y-6">
                <AnimatedElement>
                  <div class="flex flex-row justify-center">
                    <img src={BTandRTFlow} alt="" class="w-96" />
                  </div>
                </AnimatedElement>
                <AnimatedElement>
                  <div class="space-y-6">
                    <p>
                      On every trade, a part of the fee is split between the
                      Risk Treasury, for protocol expenses and other treasuries.
                    </p>
                    <p>
                      The funds going into the Risk Treasury is managed by our
                      core team and placed into moderate-risk investments.
                    </p>
                    <p>
                      A part of the profits from these investments will flow
                      back into the backing treasury.
                    </p>
                  </div>
                </AnimatedElement>
              </div>
            </TabPanel>
          </Tabs>
        </Card>
      </div>
      <div
        class="flex flex-col justify-center w-full pb-8 bg-gradient-radial from-indigo-800 to-black bg-fixed bg-cover text-center bg-no-repeat"
      >
        <div class="w-full bg-no-repeat bg-center bg-cover bg-curve-2" />
        <div class="flex flex-row justify-center mt-2 text-4xl gap-8">
          <a href="https://discord.gg/AcNX7ygdju">
            <div class="w-[1em]"><FaDiscord /></div>
          </a>

          <a href="https://twitter.com/CarpetDeFi">
            <div class="w-[1em]"><FaTwitter /></div>
          </a>
          <a href="https://github.com/Carpet-DeFi">
            <div class="w-[1em]"><FaGithub /></div>
          </a>

          <a href="mailto://cybertelx@proton.me">
            <div class="w-[1em]"><FaEnvelope /></div>
          </a>

          <a href="https://docs.carpetde.fi">
            <div class="w-[1.2em]"><TiDocument /></div>
          </a>
        </div>
        <i class="mb-32" />
        <div class="flex flex-row justify-center">
          <img src={Lamp} alt="" class="w-24" />
        </div>
      </div>
    </div>

    <footer class="bg-blue-800 py-4 text-center">
      <p>This website is licensed under the GNU General Public License 3.0.</p>
      <p>Copyleft 🄯 Operator 2022, all rights reversed.</p>
    </footer>
    <!-- 
    <div
      class="flex flex-col justify-center w-full bg-stacked-waves bg-no-repeat bg-fixed bg-cover"
    >
      <h2 class="text-center text-3xl font-semibold mt-8">Protocol stats</h2>
      <div class="flex flex-row justify-center">
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 m-4 w-full max-w-4xl">
          <AnimatedElement>
            <Card innerClass="space-y-2">
              <h3 class="font-semibold uppercase">TVL</h3>
              <p class="text-2xl">$420,696,969</p>
            </Card>
          </AnimatedElement>
          <AnimatedElement>
            <Card innerClass="space-y-2">
              <h3 class="font-semibold uppercase">Carpet Price</h3>
              <p class="text-2xl">$4.2069 per CARPET</p>
            </Card>
          </AnimatedElement>
          <AnimatedElement>
            <Card innerClass="space-y-2">
              <h3 class="font-semibold uppercase">Today's Volume</h3>
              <p class="text-2xl">$420,696</p>
              <p>this stat resets at midnight utc</p>
            </Card>
          </AnimatedElement>

          <AnimatedElement>
            <Card innerClass="space-y-2">
              <h3 class="font-semibold uppercase">Today's Largest Buy</h3>
              <p class="text-2xl">$420</p>
              <p>this stat resets at midnight utc</p>
            </Card>
          </AnimatedElement>
        </div>
      </div>
      <i class="mb-64" />
    </div>-->
  </section>
</main>

<style>
  p,
  span {
    @apply font-medium;
  }
  :global(.svelte-tabs li.svelte-tabs__tab) {
    @apply text-indigo-400 uppercase delay-100 transition-all font-semibold px-6 border-0 py-2 mx-1 mb-4 bg-white rounded-xl;
  }
  :global(.svelte-tabs li.svelte-tabs__selected) {
    @apply text-indigo-600 bg-blue-200;
  }
</style>
