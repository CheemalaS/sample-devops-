# sample-devops-
const addScript = () =&gt; {
    const script = document.createElement("script");
    script.src = '&lt;url-of-the-script&gt;';
    script.async = true;
    script.onload = function() {
        // Do something
    };
    document.head.appendChild(script);
}

useEffect(() =&gt; {
    addScript();
    return () =&gt; {
        // remove the script on component unmount
    };
}, []);

 ----------------------- 
const addScript = () =&gt; {
    const script = document.createElement("script");
    script.src = '&lt;url-of-the-script&gt;';
    script.async = true;
    script.onload = function() {
        // Do something
    };
    document.head.appendChild(script);
}

useEffect(() =&gt; {
    addScript();
    return () =&gt; {
        // remove the script on component unmount
    };
}, []);

 ----------------------- 
const [dbData,setDbData] = useState([]);

useEffect(()=&gt;{
  const dbReqFunc = async () =&gt; {
    // req your dynamic data here and set the data fetched to dbData
    // using setDbData(...)
  };

  dbReqFunc();
},[]);  // Making the call on component loading (Modify accordingly based on 
        // needs)


useEffect(()=&gt;{
  if(dbData.length&gt;0){
    const elem = document.createElement('div');
    dbData.map(data=&gt; {

        // based on data returned modify accordingly

        const script = document.createElement("script");
        script.src = '...script-url...';
        script.async = true;
        script.onload = function() {
          // Do something
        };
     
        //...other script fields...       

        elem.appendChild(script);
      });
     
     // attach elem to body
     document.body.appendChild(elem);

     return ()=&gt;{
      // clean-up function
        document.body.removeChild(elem);
     };
  }

},[dbData]);

 ----------------------- 
const [dbData,setDbData] = useState([]);

useEffect(()=&gt;{
  const dbReqFunc = async () =&gt; {
    // req your dynamic data here and set the data fetched to dbData
    // using setDbData(...)
  };

  dbReqFunc();
},[]);  // Making the call on component loading (Modify accordingly based on 
        // needs)


useEffect(()=&gt;{
  if(dbData.length&gt;0){
    const elem = document.createElement('div');
    dbData.map(data=&gt; {

        // based on data returned modify accordingly

        const script = document.createElement("script");
        script.src = '...script-url...';
        script.async = true;
        script.onload = function() {
          // Do something
        };
     
        //...other script fields...       

        elem.appendChild(script);
      });
     
     // attach elem to body
     document.body.appendChild(elem);

     return ()=&gt;{
      // clean-up function
        document.body.removeChild(elem);
     };
  }

},[dbData]);

 ----------------------- 
function App() {
  const ref = useRef();

  useEffect(() =&gt; {
    /* convert your HTML string into DocumentFragment*/
    const node = document.createRange().createContextualFragment(HTML);
    ref.current.appendChild(node);
  }, []);

  return (
    &lt;div&gt;
      &lt;h1&gt;HTML String&lt;/h1&gt;
      &lt;div&gt;
        &lt;div ref={ref}&gt;&lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  );
}


class App extends React.Component {
  constructor(props) {
    super(props);
    this.ref = React.createRef();
  }

  componentDidMount() {
    const node = document.createRange().createContextualFragment(HTML);
    this.ref.current.appendChild(node);
  }

  render() {
    return (
      &lt;div&gt;
        &lt;h1&gt;HTML String&lt;/h1&gt;
        &lt;div&gt;
          &lt;div ref={this.ref}&gt;&lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    );
  }
}


 ----------------------- 
function App() {
  const ref = useRef();

  useEffect(() =&gt; {
    /* convert your HTML string into DocumentFragment*/
    const node = document.createRange().createContextualFragment(HTML);
    ref.current.appendChild(node);
  }, []);

  return (
    &lt;div&gt;
      &lt;h1&gt;HTML String&lt;/h1&gt;
      &lt;div&gt;
        &lt;div ref={ref}&gt;&lt;/div&gt;
      &lt;/div&gt;
    &lt;/div&gt;
  );
}


class App extends React.Component {
  constructor(props) {
    super(props);
    this.ref = React.createRef();
  }

  componentDidMount() {
    const node = document.createRange().createContextualFragment(HTML);
    this.ref.current.appendChild(node);
  }

  render() {
    return (
      &lt;div&gt;
        &lt;h1&gt;HTML String&lt;/h1&gt;
        &lt;div&gt;
          &lt;div ref={this.ref}&gt;&lt;/div&gt;
        &lt;/div&gt;
      &lt;/div&gt;
    );
  }
}
