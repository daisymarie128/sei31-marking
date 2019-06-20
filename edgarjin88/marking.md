# SEi31 Final Project Marking

## My News
### Author: Monica
Repo: https://github.com/edgarjin88/proejct04

#### General comments

Congradulations on finishing SEi!! You had a great final project with some awesome features! 👏👏 

You had clean professional looking styling which was great. The video streaming you got working was awesome, and you should be very proud of yourself, this is a cool technical feature to hav gotten implemented and you should feel very proud. 

The best part about your presenation was that you could forumlate your own opinion on technical frameworks from what you learnt building your projects and this is a great thing to see in a developer. Mentioning Redux was an overkill was great - it really showed you used it and learnt the bad parts about it. In programing it's not always the best just to use the latest a greatest frameworks, like you learn.

This is a nice artcile written by the creator of Redux, where ven he says Redux is complicated and unneeded for most projects 😀
[redux arctile](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367)

#### Code feedback

It's great to see you have a good understanding of how React works and should be written. To take that further you could make your code more readable by splitting components out to render functions to make things easier.

Example, this part of your code:
```js
renderItem={item => (  //이 item 관한 것들이 반복되서 들어간다.
      //반복문 돌린 결과들이 renderItem에 들어간다. item은 참고로 antd 속성
      <List.Item style={{ marginTop: '20px' }}>
        <Card actions={[<Icon key="stop" type="stop" onClick={onClickStop(item.id)} />]}>
          <Card.Meta description={item.nickname} />
        </Card>
      </List.Item>
    )}
```

could be written like this:
```js
const renderListItem = (item) => {
 return (
	<List.Item style={{ marginTop: '20px' }}>
    <Card actions={[<Icon key="stop" type="stop" onClick={onClickStop(item.id)} />]}>
      <Card.Meta description={item.nickname} />
    </Card>
  </List.Item>
	)
}


...

renderItem={item => renderListItem(item)}
```

consider using `<Reat.Fragment>` or `<>` to render blocks of code without having to wrap them in an empty div.

`postData.split(/(#[^\s]+)/g`

Hashtags can be very dificult to read even for experienced developers. It's best practice to turn your regex pattern into a constant with a descriptive name - to make it easier to read in the future.

For example:
```js
const hashPattern = /(#[^\s]+)/;

postData.split(hashPattern)
```

This makes the pattern easier to be reused in more places as you needed 😀
