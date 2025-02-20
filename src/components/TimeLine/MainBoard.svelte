<style>
  :global(.triggerAlbum) {
    background-color: #00afb9;
    color: #fdfcdc;
    padding: 0.6rem;
    padding-inline: 0.8rem;
    border: none;
    border-radius: 1rem;
    cursor: pointer;
    margin-top: 1rem;
    display: flex
;
    align-items: center;
    gap: 0.5rem;
    font-weight: bold;
    font-size: 1rem;
    transition:0.2s;
}
:global(.triggerAlbum:hover) {
  background-color: #fed9b7;
    color: #f07167;
}
:global(#timeline-embed){
  height:100vh !important;
}
</style>

<script>
  import { onMount } from 'svelte';

  let timeline_config = {
    "lang": "vi",
    "height": "600",
    "start_at_slide": 0,
    "language": "vi",
    "font": "none"
  };

  let timelineContainer;
  let timelineData = null;

  onMount(async () => {
    const res = await fetch('data.json');
    timelineData = await res.json();
    console.log(timelineData);

    // Kiểm tra và khởi tạo TimelineJS nếu có dữ liệu
    if (window.TL && timelineData) {
      new TL.Timeline(timelineContainer, timelineData, timeline_config);
    } else {
      console.error("Không thể tải dữ liệu TimelineJS.");
    }

    // Lắng nghe sự kiện click trên timelineContainer
    timelineContainer.addEventListener("click", (event) => {
      if (event.target && event.target.classList.contains("triggerAlbum")) {
        window.location.href = '/viewsphere'
        console.log("asssssssssssssss")
      }
    });
  });
</script>

<!-- Timeline Container -->
<div bind:this={timelineContainer} id="timeline-embed" style="width: 100%; height: 600px;"></div>
