<template>
  <section class="contributing-container">
    <NyanCat />
    <SeparatorSingleLine />
    <div class="bg-secondary">
      <div class="container contributing-container-text">
        <div class="inner-text">
          <h4>{{ $t('message.contributing.title') }}</h4>
          <p>
            <b>Schrödinger Hat</b> {{ $t('message.contributing.is-a-project') }}
            <a class="external-link-color" href="https://github.com/Schrodinger-Hat" target="_blank"
              >GitHub</a
            >.
          </p>
          <p v-html="$t('message.contributing.cta')"></p>
          <p class="social">
            <a href="https://opencollective.com/schrodinger-hat" target="_blank">
              <i class="fas fa-donate external-link-color"></i>
            </a>
            <a href="https://www.facebook.com/schrodingerhat" target="_blank">
              <i class="fab fa-facebook external-link-color"></i>
            </a>
            <a href="https://twitter.com/schrodinger_hat" target="_blank">
              <i class="fab fa-twitter external-link-color"></i>
            </a>
            <a href="https://www.linkedin.com/company/schrodinger-hat/" target="_blank">
              <i class="fab fa-linkedin external-link-color"></i>
            </a>
            <a href="https://www.instagram.com/schrodinger_hat/" target="_blank">
              <i class="fab fa-instagram external-link-color"></i>
            </a>
            <a href="https://discord.gg/RTXr8A3eFn" target="_blank">
              <i class="fab fa-discord external-link-color"></i>
            </a>
          </p>
        </div>
        <div class="inner-text">
          <h4 style="padding: 15px 0">Community Partners</h4>
          <div class="partner-image">
            <a href="https://www.grusp.org/" target="_blank" class="sponsor-image">
              <img width="200" src="/img/grusp.jpeg" alt="Grusp Logo" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import NyanCat from '@/components/NyanCat.vue';
import SeparatorSingleLine from '@/components/separator/SingleLine.vue';

export default {
  name: 'Contributing',
  props: {},
  components: {
    NyanCat,
    SeparatorSingleLine,
  },
};
</script>

<!-- da rifare -->
<style scoped lang="scss">
.contributing-container {
  position: relative;

  .background-svg {
    width: 100%;
    margin-bottom: -15px;

    .single-line {
      fill: $bg-secondary;
    }
  }

  .bg-secondary {
    background-color: $bg-secondary;
    padding: 2em 0 0 0;
  }

  .social {
    a {
      padding: 0 0.5em;
      font-size: 1.2em;
    }
  }
}

.contributing-container-text {
  width: 100%;
  text-align: center;
  margin: 0px auto;

  .inner-text {
    padding: 0 0.5em;
    h4 {
      font-size: 2.2em;
      margin: 0 0;
    }
  }
}

@media (min-width: 56.25em) {
  .contributing-container {
    .background-svg {
      margin-bottom: -5px;
    }

    .bg-secondary {
      padding: 2em 0 12em 0;
    }
  }
}

.#{$dark-mode-class} {
  .contributing-container {
    .background-svg {
      margin-bottom: -5px;
      .single-line {
        fill: $dark-bg-secondary;
      }
    }

    .bg-secondary {
      background-color: $dark-bg-secondary;
    }
  }
}
</style>
