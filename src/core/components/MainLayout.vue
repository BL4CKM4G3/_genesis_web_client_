<template>
  <div class="main-layout d-flex align-center col w-100 h-100">
    <div class="d-flex row w-80 h-70">
      <div class="nes-container d-flex row w-80 h-65 is-dark with-title">
        <p class="title">Panel</p>
        <div class="nes-container d-flex col w-25 h-30 is-dark with-title">
          <p class="title">Messages</p>
          <span class="nes-text is-success">Api call from IP: 127.0.0.0</span>
        </div>
        <div class="nes-container d-flex col w-25 h-30 is-dark with-title">
          <p class="title">Errors</p>
          <span class="nes-text is-error">Bad request from IP: 127.0.0.0</span>
        </div>
        <div class="nes-container d-flex col w-25 h-30 is-dark with-title">
          <p class="title">Hosts</p>
          <span class="nes-text is-normal">Service on host: 25.0.1.22</span>
        </div>
      </div>
    </div>
    <div class="d-flex row w-80 h-25">
      <div class="nes-container d-flex row w-80 h-30 is-dark with-title">
        <p class="title">Actions</p>
        <div class="d-flex col w-50 h-10">
          <div class="d-flex row w-25 h-25">
            <section class="h-10">
              <button
                type="button"
                class="nes-btn is-normal h-10"
                onclick="document.getElementById('dialog-api').showModal();"
              >
                Api
              </button>
              <dialog class="nes-dialog is-dark" id="dialog-api">
                <p class="title">Api Actions</p>
                <form method="dialog">
                  <div class="d-flex row">
                    <div class="d-flex col">
                      <button type="button" class="nes-btn is-error">
                        Config
                      </button>
                      <button type="button" class="nes-btn is-normal">
                        Stats
                      </button>
                    </div>
                    <div class="d-flex col">
                      <button type="button" class="nes-btn is-normal">
                        Hosts
                      </button>
                      <button type="button" class="nes-btn is-normal">
                        Actions
                      </button>
                    </div>
                  </div>
                  <div class="d-flex row">
                    <div class="d-flex col">
                      <menu class="dialog-menu">
                        <button class="nes-btn">Cancel</button>
                        <button class="nes-btn is-primary">Confirm</button>
                      </menu>
                    </div>
                  </div>
                </form>
              </dialog>
            </section>
            <section class="h-10">
              <button
                type="button"
                class="nes-btn is-normal h-10"
                onclick="document.getElementById('dialog-db').showModal();"
              >
                Database
              </button>
              <dialog class="nes-dialog is-dark" id="dialog-db">
                <form method="dialog">
                  <p class="title">Database:</p>
                  <div class="d-flex row">
                    <div class="d-flex col">
                      <button class="nes-btn is-primary">Restore</button>
                      <button class="nes-btn is-error">Drop</button>
                    </div>
                    <div class="d-flex col">
                      <button class="nes-btn is-primary">Inspect</button>
                      <button class="nes-btn is-primary">Rules</button>
                    </div>
                  </div>
                  <menu class="dialog-menu">
                    <button class="nes-btn">Cancel</button>
                    <button class="nes-btn is-primary">Confirm</button>
                  </menu>
                </form>
              </dialog>
            </section>
          </div>
          <div class="d-flex row w-25 h-25">
            <section class="h-10">
              <button
                type="button"
                class="nes-btn is-normal h-10"
                onclick="document.getElementById('dialog-git').showModal();"
              >
                Git
              </button>
              <dialog class="nes-dialog is-dark" id="dialog-git">
                <form method="dialog">
                  <p class="title">Git</p>
                  <div class="d-flex row">
                    <div class="d-flex col">
                      <button class="nes-btn is-primary">Fetch</button>
                      <button class="nes-btn is-primary">Checkout</button>
                    </div>
                    <div class="d-flex col">
                      <button class="nes-btn is-primary">Update Branch</button>
                      <button class="nes-btn is-primary">Branches</button>
                    </div>
                  </div>
                  <menu class="dialog-menu">
                    <button class="nes-btn">Cancel</button>
                    <button class="nes-btn is-primary">Confirm</button>
                  </menu>
                </form>
              </dialog>
            </section>
            <section class="h-10">
              <button
                type="button"
                class="nes-btn is-normal h-10"
                onclick="document.getElementById('dialog-charts').showModal();"
              >
                Charts
              </button>
              <dialog class="nes-dialog is-dark" id="dialog-charts">
                <form method="dialog">
                  <p class="title">Charts:</p>
                  <menu class="dialog-menu">
                    <button class="nes-btn">Cancel</button>
                    <button class="nes-btn is-primary">Confirm</button>
                  </menu>
                </form>
              </dialog>
            </section>
          </div>
        </div>
        <div class="d-flex col w-50">
          <div class="d-flex row w-25 h-25">
            <button type="button" class="nes-btn is-primary h-10">
              Import Api
            </button>
            <button type="button" class="nes-btn is-error h-10">Config</button>
          </div>
          <div class="d-flex row w-25 h-25">
            <button type="button" class="nes-btn is-error h-10">
              BlackList
            </button>
            <button type="button" class="nes-btn is-success h-10">
              WhiteList
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../../assets/flex.scss";
@import url("https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap");

* {
  font-family: "Press Start 2P", cursive;
}
.main-layout {
  padding-top: 0.5rem;
  background: linear-gradient(
    152deg,
    rgba(45, 32, 47, 1) 6%,
    rgba(42, 40, 40, 1) 25%,
    rgba(39, 40, 50, 1) 30%,
    rgba(31, 29, 29, 1) 55%,
    rgba(27, 29, 36, 1) 77%,
    rgba(25, 22, 22, 1) 84%
  );
}
</style>