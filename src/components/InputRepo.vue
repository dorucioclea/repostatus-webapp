<template>
  <div id="input-repo">
    <div class="d-flex justify-content-center py-5 mt-3">
      <div class="repo-chooser">
        <span>
          <GithubIcon class="github-icon" size="25" />
        </span>
        <span class="repo-text">
          <p>Choose GitHub Repo</p>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import { GithubIcon } from "vue-feather-icons";

export default {
  name: "InputRepo",
  components: {
    GithubIcon
  }
};
</script>

<style lang="scss" scoped>
.repo-chooser {
  @extend .rounded-cust-sm;
  @extend .shadow-lg-green;

  width: 350px;
  background: $green;
  cursor: pointer;
  color: $black;
  padding: 25px 10px;
  display: flex;
  justify-content: center;
  transition: 0.3s ease;

  &:hover {
    background: darken($green, 10);
    transition: 0.3s ease;
  }

  .github-icon {
    margin-right: 5px;
  }

  .repo-text {
    margin-left: 8px;
    font-size: 1.1em;
    font-weight: 500;

    p {
      margin: 0 auto;
    }
  }
}
</style>