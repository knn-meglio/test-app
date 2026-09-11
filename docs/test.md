| Screen / Component | Main Changes | Need to Test |
| --- | --- | --- |
| **Chat Detail** | `ChatMessageCell`, image cell, warning cell၊ controller နဲ့ header ထဲက declarations တွေ ပြန်စီထားပါတယ်။ Changes အများဆုံးနေရာပါ | Message rendering၊ image၊ warning နဲ့ header |
| **Estate Expense / Income** | `MonthlyProfitLossChartView` ထဲက declarations တွေ ပြန်စီထားပါတယ် | Monthly chart နဲ့ data display |
| **Chat Assessment List** | `AssessmentListCell` ထဲက declarations တွေ ပြန်စီထားပါတယ် | List cell display နဲ့ selection |
| **Auto Chat** | `AutoChatViewActionCreator` ထဲက methods တွေ ပြန်စီထားပါတယ် | Chat actions နဲ့ response flow |
| **Present / Ticket component** | `PresentTicketCell` ထဲက declarations တွေ ပြန်စီထားပါတယ် | Ticket display နဲ့ tap action |
| **Estate Location Edit** | `zipCodeView` ကို အရင်ဖန်တီးသွားလို့ `EstateMemory` မှ postcode ဖတ်တဲ့အချိန် စောသွားပါတယ် | **Postcode prefill၊ address lookup** |
| **Estate Detail Balance** | `titleText` ကို အခြား UI properties တွေထက် အရင်ဖန်တီးသွားပါတယ် | Title၊ buttons နဲ့ budget list |
| **News Detail** | `detailContent` ကို title/date/container ထက် အရင်ဖန်တီးသွားပါတယ် | Content၊ images နဲ့ links |
| **Campaign Carousel** | Selected/default images ကို navigation icons ထက် အရင်ဖန်တီးသွားပါတယ် | Page dots၊ previous/next controls |


# SwiftFormat Spacing Rules

လက်ရှိ configuration ထဲရှိ rules 7 ခု၏ အသုံးပြုပုံနှင့် ပြောင်းလဲသွားမည့် နမူနာများဖြစ်ပါတယ်။

Table ထဲက `↵` သည် newline ကို ဆိုလိုပါတယ်။ `↵↵` သည် ကြားတွင် blank line တစ်ကြောင်းရှိခြင်းကို ဆိုလိုပါတယ်။

| Rule | ဘာအတွက်သုံးသလဲ | Before | After |
| --- | --- | --- | --- |
| `blankLinesAtStartOfScope` | Scope အဖွင့် `{` နောက်ရှိ မလိုအပ်သော blank line ကို ဖယ်ရှားပေးပါတယ်။ | `func run() {↵↵    work()↵}` | `func run() {↵    work()↵}` |
| `blankLinesAtEndOfScope` | Scope အပိတ် `}` မတိုင်ခင်ရှိ မလိုအပ်သော blank line ကို ဖယ်ရှားပေးပါတယ်။ | `func run() {↵    work()↵↵}` | `func run() {↵    work()↵}` |
| `spaceAroundOperators` | Operators နှင့် delimiters အနားရှိ spacing ကို ညှိပေးပါတယ်။ | `let total = a+b` | `let total = a + b` |
| `spaceAroundBraces` | Curly braces `{ }` အပြင်ဘက်ရှိ spacing ကို ညှိပေးပါတယ်။ | `values.map{ $0 }` | `values.map { $0 }` |
| `spaceAroundParens` | Parentheses `( )` အပြင်ဘက်ရှိ spacing ကို syntax အလိုက် ညှိပေးပါတယ်။ | `print (value)` | `print(value)` |
| `spaceInsideParens` | Parentheses `( )` အတွင်း အစနှင့်အဆုံးရှိ မလိုအပ်သော space ကို ဖယ်ရှားပေးပါတယ်။ | `print( value )` | `print(value)` |
| `spaceInsideBrackets` | Square brackets `[ ]` အတွင်း အစနှင့်အဆုံးရှိ မလိုအပ်သော space ကို ဖယ်ရှားပေးပါတယ်။ | `let values = [ 1, 2 ]` | `let values = [1, 2]` |

## Rules အားလုံးပေါင်းပြီး အသုံးပြုသည့် နမူနာ

### Before

```swift
func example () {

    let values = [ 1, 2 ]
    let total = ( 1+2 )
    values.forEach{ print ( $0+total ) }

}
```

### After

```swift
func example() {
    let values = [1, 2]
    let total = (1 + 2)
    values.forEach { print($0 + total) }
}
```

## မှတ်ချက်

- နမူနာများသည် လက်ရှိ configuration အတွက် ဖြစ်ပါတယ်။ `--type-blank-lines` option ပြောင်းပါက type scope များ၏ blank-line ပုံစံ ပြောင်းနိုင်ပါတယ်။
- `blankLinesAtStartOfScope` နှင့် `blankLinesAtEndOfScope` သည် scope အတွင်း အစ/အဆုံးရှိ blank lines ကို ညှိခြင်းဖြစ်ပြီး methods နှစ်ခုကြား blank line ထည့်သည့် `blankLinesBetweenScopes` နှင့် မတူပါဘူး။
- ဒီ rules 7 ခုသည် spacing နှင့် blank lines ကို ညှိပေးခြင်းဖြစ်ပြီး properties/methods များ၏ declaration order ကို မစီပါဘူး။

## Reference

[SwiftFormat Official Rules](https://github.com/nicklockwood/SwiftFormat/blob/main/Rules.md)

