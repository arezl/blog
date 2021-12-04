## 初始化handler     

TcpMsg.Ins.RegistEventHandler

handler注册TcpMsg 和 中转广播 委托action;

       public abstract class MsgHandler<T> where T : new()
        {
            public static readonly T Ins = new T();
            public abstract void InitHandler();
        }


​        
    public class BagHandler : MsgHandler<BagHandler>
        {
            public Action OnBagChange;
            public Dictionary<int, long> ItemMap = new Dictionary<int, long>();
            public override void InitHandler()
            {
                TcpMsg.Ins.RegistEventHandler(ResBagInfo.MsgId, onResBagInfo);
                TcpMsg.Ins.RegistEventHandler(ResItemChange.MsgId, onResItemChange);
            }
    
            void onResBagInfo(BaseMessage msg)
            {
                var res = (ResBagInfo)msg;
                ItemMap = res.itemDic;
                OnBagChange?.Invoke();
            }


## UI显示



     public class BagWindow : MonoBehaviour
    void OnDestroy()
        {
            BagHandler.Ins.OnBagChange -= onBagChange;
        }
      void Awake()
            {
                CloseBtn.onClick.AddListener(() => Destroy(gameObject));
                BagHandler.Ins.OnBagChange += onBagChange;
                onBagChange();
            }
        void onBagChange()
        {
            foreach (var kv in cacheMap)
                Destroy(kv.Value.gameObject);
            cacheMap.Clear();
    
            var map = BagHandler.Ins.ItemMap;
            foreach(var kv in map)
## 登录后触发其他的 action handler初始化

```
   public class LoginHandler : MsgHandler<LoginHandler>
    {
        public Action OnUserInfoChange;
        public UserInfo UserData { get; set; }
        public override void InitHandler()
        {
            //登陆系统服务器下行消息监听
            TcpMsg.Ins.RegistEventHandler(ResLogin.MsgId, onResLogin);
            TcpMsg.Ins.RegistEventHandler(ResLevelUp.MsgId, onResLevelUp);
            TcpMsg.Ins.RegistEventHandler(ResNotice.MsgId, onResNotice);
            TcpMsg.Ins.RegistEventHandler(ResChangeName.MsgId, onResChangeName);
        }

        void onResLogin(BaseMessage msg)
        {
            var res = (ResLogin)msg;
            if(res.code != 0)
            {
                Debug.LogError("登陆失败，code=" + res.code);
                return;
            }
            Debug.Log("登陆成功");
            UserData = res.userInfo;
            OnUserInfoChange?.Invoke();
            SceneManager.LoadScene("Main");
        }

```

### action

```
 
	///<summary>背包</summary> 
		///<summary>道具</summary>	 
		///<summary>反序列化，读取数据</summary>	 
	///<summary>使用道具</summary>	D:\Downloads\GeekServer\UnityDemo\Assets\Scripts\Generate\Messages\DemoBag.cs	126	2 
	///<summary>道具变化</summary>	D:\Downloads\GeekServer\UnityDemo\Assets\Scripts\Generate\Messages\DemoBag.cs	216	2
		///<summary>变化的道具</summary>	D:\Downloads\GeekServer\UnityDemo\Assets\Scripts\Generate\Messages\DemoBag.cs	223	3 
		
		
		
			public class MsgFactory
	{
		///<summary>通过msgId构造msg</summary>
		public static BaseMessage Create(int msgId)
		{
			switch(msgId)
			{
				//背包
				case 112001: return new Geek.Client.Message.DemoBag.ReqBagInfo();
				case 112002: return new Geek.Client.Message.DemoBag.ResBagInfo();
				case 112003: return new Geek.Client.Message.DemoBag.ReqUseItem();
				case 112004: return new Geek.Client.Message.DemoBag.ReqSellItem();
				case 112005: return new Geek.Client.Message.DemoBag.ResItemChange();
				
				//登陆
				case 111001: return new Geek.Client.Message.DemoLogin.ReqLogin();
				case 111002: return new Geek.Client.Message.DemoLogin.ResLogin();
				case 111003: return new Geek.Client.Message.DemoLogin.ResLevelUp();
				case 111004: return new Geek.Client.Message.DemoLogin.ResNotice();
				case 111005: return new Geek.Client.Message.DemoLogin.ReqChangeName();
				case 111006: return new Geek.Client.Message.DemoLogin.ResChangeName();
				
				//玩家快照
				case 101201: return new Geek.Client.Message.Login.ReqLogin();
				case 101202: return new Geek.Client.Message.Login.ReqReLogin();
				case 101101: return new Geek.Client.Message.Login.ResLogin();
				case 101102: return new Geek.Client.Message.Login.ResReLogin();
				case 101303: return new Geek.Client.Message.Login.HearBeat();
				case 101103: return new Geek.Client.Message.Login.ResPrompt();
				case 101104: return new Geek.Client.Message.Login.ResUnlockScreen();
				
				//举例各种结构写法
				case 111101: return new Geek.Client.Message.Sample.ReqTest();

```

public class t_languageContainer : BaseContainer

