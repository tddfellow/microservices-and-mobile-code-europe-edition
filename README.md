# MicroServices and Mobile

(APIdays Paris 2016)



<img src="../my-presentation-template/me.jpeg" class="photo-me">

## Oleksii Fedorov

Software Craftsperson

[@waterlink000](https://twitter.com/waterlink000)


<!-- -- data-background="url(./Pivotal_WhiteOnTeal.png) no-repeat center" data-background-size="cover"  -->



## Example of the DSL


<div class="presented-code">
// microservice A

{
  "subscribe": {
    "event": "user_has_liked_item",
    "actions": [
      {
        "request":
          "/recommendations/${event.item_id}",
        "publish": "received_recommendations"
      }
    ]
  }
}
</div>


<div class="presented-code">
// microservice B

{
  "subscribe": {
    "event": "received_recommendations",
    "actions": [
      {
        "render": { view": "item_list",
            "data": "${event.response.items}" }
      }
    ]
  }
}
</div>



## Bottom Line



## Thanks
