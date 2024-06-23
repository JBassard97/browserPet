<script lang="js">
  const outline = {
    fill: "transparent",
    stroke: "black",
    "stroke-width": "0.1", // stroke-width in quotes because the - requires it
  };
</script>

<svg class="room-outline" viewBox="0 0 100 100" preserveAspectRatio="none">
  <rect class="back-wall" x="15" y="20" width="70" height="50" {...outline} />
  <polygon class="left-wall" points="15,20 0,10, 0,80 15,70" {...outline} />
  <polygon class="right-wall" points="85,20 100,10 100,80 85,70" {...outline} />
  <polygon
    class="ceiling"
    points="15,20 0,10 0,0 100,0 100,10 85,20"
    {...outline}
  />
  <polygon
    class="floor"
    points="15,70 0,80 0,100 100,100 100,80 85,70"
    {...outline}
  />
  <ellipse class="rug-outer" cx="50" cy="85" rx="40" ry="10" {...outline} />
  <ellipse class="rug-inner" cx="50" cy="85" rx="30" ry="7" {...outline} />
  <rect class="door" x="60" y="40" width="20" height="30" {...outline} />
  <ellipse class="doorknob" cx="75" cy="55" rx="1" ry="1" {...outline}/>
</svg>

<style>
  .room-outline {
    height: 100%;
    width: 100%;
    z-index: -5;
  }
</style>
