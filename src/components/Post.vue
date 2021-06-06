<template>
  <StackLayout class="post">
    <FlexBoxLayout class="post__profile">
      <StackLayout class="post__imgProfile">
        <Image src="~/assets/davi.png" style="width: 100%" />
      </StackLayout>
      <Label text="daviaugusto.me" />
    </FlexBoxLayout>
    <Image :src="Image" class="post__image" />
    <FlexboxLayout class="post__desc">
      <Label
        text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla libero mi, placerat eu lacus vel, vestibulum varius ipsum."
        textWrap
      />
    </FlexboxLayout>
  </StackLayout>
</template>

<script>
export default {
  props: {
    Image: String,
  },
};
</script>

<style lang="scss" scoped>
.post {
  margin-top: 30;

  &__profile {
    padding: 0 10 10 10;

    label {
      margin-left: 10;
      font-size: 13;
      font-weight: 500;
    }
  }

  &__imgProfile {
    width: 35;
    height: 35;
    border-radius: 100;
    overflow: hidden;
  }

  &__desc {
    padding: 10;

    label {
      font-size: 12;
    }
  }
}
</style>
