<style>
    #container{
        background-color: #ffffff;
    height: 100%;
    width: 100%;
    position: fixed;
    }
    iframe{
        position:absolute;
        width:100%;
        height:95vh;
        bottom:0;
    }
    button{
        width: fit-content;
    height: 4vh;
    border-radius: 0.5rem;
    gap: 0.2rem;
    display: flex
;
    align-items: center;
    justify-content: space-around;
    font-size: 2vh;
    font-weight: bold;
    background-color: #f07167;
    color: #fff;
    cursor: pointer;
    padding-left: 0.2rem;
    padding-right: 0.5rem;
    margin-left: 11vh;
    }
    #title{
        position: absolute;
    top: 0;
    height: 5vh;
    display: flex
;
    justify-content: space-between;
    align-items: center;
    font-size: 1.2rem;
    left: 0;
    right: 0;
    padding-left: 1vw;
    padding-right: 0.5vh;
    color: #0081a7;
    font-weight: bold;
    z-index: 99;
    box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
    }
    span{    font-size: 3vh;}
    @media (max-width: 1100px) {
        #title{
            font-size:0.7rem;
            height:6vh;
  }
  iframe{
    height:94vh;
  }
}
</style>
<script>
 
</script>

<div id = 'container'>
    <div id = 'title'>
        Thư Viện Ảnh 3D: Ngoại Giao Việt Nam Thời kì chống Pháp (tạo bởi Nguyễn Văn Tây - 12a1)
    <button on:click = {()=>{window.location.href = '/weblichsucuateyypro'}}><span class="material-symbols-outlined">
        logout
        </span>Thoát</button>
    </div>
    <iframe src=https://uploads.knightlab.com/scenevr/15896/4482ff53/index.html frameborder="0" allowfullscreen />
</div>