<template>
  <div class="logo-wrap">
    <a class="logo">
      <span
        >B<span class="collapse"
          ><i>a</i><i>r</i><i>a</i><i>k</i><i>h</i><i>o</i><i>v</i></span
        >.</span
      >
    </a>
  </div>
</template>

<script>
export default {
  name: "Logo",
};
</script>

<style scoped lang="scss">
$letter-count: 7;
.logo-wrap {
}

.logo {
  font-size: 2em;
  font-weight: 700;
  display: inline-block;
  transition: all 0.3s ease;
  cursor: pointer;
}

.logo .collapse {
  display: inline-block;
  max-width: 142px;
  transition: max-width 0.3s cubic-bezier(0, 0, 0, 1);
}

$letter-count: 7;

// @for $i from 0 through $letter-count - 1 {
//   .logo .collapse i:nth-of-type(#{$i + 1}) {
//     transition: all 0.2s #{- (0.05-0.3)}s linear;
//   }
// }

.logo:hover .collapse {
  max-width: 142px;
  transition: max-width 0.3s cubic-bezier(0, 0, 0, 1);
}

.logo:hover .collapse i {
  opacity: 1;
  transform: translate(0, 0);
}

@for $i from 0 through $letter-count - 1 {
  .logo:hover .collapse i:nth-of-type(#{$i + 1}) {
    transition: all 0.2s #{$i * 0.05}s linear;
  }
}

.logo-wrap .collapse {
  max-width: 0;
  transition: max-width 0.3s 0.2s cubic-bezier(0, 0, 0, 1);
}

.logo-wrap .collapse i {
  font-style: normal;
  opacity: 0;
  transform: translate(0, -5px);
}

@for $i from 0 through $letter-count - 1 {
  .logo-wrap .collapse i:nth-of-type(#{$i + 1}) {
    transition: all 0.2s #{0.3 - ($i * 0.05)}s linear;
  }
}
</style>
