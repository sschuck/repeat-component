repeat-component
================

ng-like {{#repeat things }} block helper for Meteor-UI {{/repeat}}
include prototypical $parent context in each nest:
```HTML
     <div class="container">
        <div class="row">
            <h1>#repeat things =  #for things by <a href="github.com/charlesjshort/repeat-component">charlesjshort&nbsp;<i class="ion-social-github"></i></a></h1>
            <h2 class="well">#each with prototype scope <p class="well"> $parent, $index, $first, $last, $odd, $even, $middle</p></h2> 
        </div>
        <div class="row">
          {{#repeat things }}
          <div class="col-sm-6">
          <h2 class="{{ getColor }}">{{ indexRoot }}</h2>
            <ul class="list-group">
              {{#for things }}
                <div class="col-sm-6">
                <li class="list-group-item">
                <h4 class="{{ getColor }} list-group-item-heading">{{ indexRoot }}</h4>
                <ul class="list-group">
                    {{#repeat things }}
                    <div class="col-sm-6">
                    <li class="list-group-item">
                    <h4 class="{{ getColor }} list-group-item-heading">{{ indexRoot }}</h4>
                    <ul class="list-group">
                      {{#for things }}
                      <div class="col-sm-6">
                          <li class="{{ getColor }} list-group-item">{{ indexRoot }}</li>
                      </div>
                      {{/for}}
                  </ul>
                    </li>
                    </div>
                  {{/repeat}}
              </ul>
              </li>
              </div>
              {{/for}}
          </ul>
        </div>
          {{/repeat}}
      </div>
    </div><!-- /.container !-->
```

