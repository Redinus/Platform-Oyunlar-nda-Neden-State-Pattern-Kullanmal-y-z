Merhaba burada platform oyunlarında neden state pattern kulanmamız gerektiğinin kod mantiğini kısaca anlatıcam ilk başta standar bir state yani temel durumlarımızın iskeletini abstract class ile yapıyoruz.
Örneğin:


using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public abstract class State 
{
    public abstract void EnterState();
    public abstract void UpdateState();
    public abstract void LeaveState();
}



Daha sonra bir state machine oluşturuyoruz state machin ise genel hatlarıyla bizim stateleirmizi (Durumlarımızı) tanımlayan ve yöneten kodumuzdur bir nevi beğin gibi düşünebiliriz. Bu temeleri analtığıma göre buradan sonra stateleri ve bu örnekte vereceğimiz platform örneğindeki stateleri kabaca oluşturalım. Temel olarak bazı yeteneklerimiz ele alıcaz durumlarımız kısaca yeteneklerimiz olucak. Tabiki bu stateleri aynı zamanda statemachinede tanıtmamız gerekmektedir burada state iskeleti dışında bir kod paylaşmayacam yani kısaca tüm kodlar mantıksal kalacaktır. Pkei bizim yeteneklerimiz ne olucak bu güzel bir soru platform oyunlarında dash , ışınlanma ,dayanıklılık artırma (Kalkan) ve halat atma gibi mekanikler gayet yeterli olacaktır. Peki biz bu durumları nasıl oluşturucaz öncelikle her biri için bir script yazıcaz toplamda State , StateMachine , TeleportState , DashState , ShieldState ve HookState olmak üzere 6 Scriptimiz olucak bu durumlara istediğimz durumda neler olucağını yazıca ve bu durumları state machinde tanımlayım yöneticez. 
Stateler:
TeleportState 
DashState 
ShieldState 
HookState

Kısaca state pattern bu şekilde kullanılır. Umarım faydalı olmuştur.
