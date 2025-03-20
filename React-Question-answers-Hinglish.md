## Q1: React.js kya hai aur hum ise kyun use karte hain?

<small>React.js ek JavaScript library hai jo user interfaces banane ke liye use hoti hai, khaaskar single-page applications (SPAs) ke liye. Yeh Facebook dwara 2011 mein develop ki gayi thi aur pehle Facebook ke News Feed par implement hui. 2013 mein ise sabke liye open-source kar diya gaya. React developers ko bade web applications banane mein madad karti hai jo data changes ke response mein efficiently update aur render hote hain. Yeh component-based architecture par zor deti hai, jo reusable UI components banane ki suvidha deti hai, aur virtual DOM ka upyog karke performance ko enhance karti hai, jisse actual DOM ke direct manipulations kam ho jaate hain.</small>

## Q2: React.js ke mukhya features kya hain?

<small>React.js ke kai key features hain jo ise dynamic user interfaces banane ke liye lokpriya banate hain:

- **Declarative Syntax:** React ek declarative programming paradigm follow karta hai, jisme developers application ke har state ke liye views design karte hain, aur React data changes hone par components ko efficiently update aur render karta hai. Yeh approach code readability aur maintenance ko enhance karta hai.

- **Component-Based Architecture:** React mein applications encapsulated components ka upyog karke bante hain jo apna khud ka state manage karte hain. Yeh modularity code reuse ko promote karti hai aur development aur maintenance ko simplify karti hai.

- **Virtual DOM:** React ek virtual DOM ka upyog karta hai, jo real DOM ka ek in-memory representation hai. Jab kisi object ka state change hota hai, to virtual DOM sirf us specific object ko real DOM mein update karta hai, jisse performance improve hoti hai aur user experience smoother hota hai.

- **JSX (JavaScript Syntax Extension):** JSX developers ko JavaScript code ke andar HTML-jaise syntax likhne ki suvidha deta hai, jisse code zyada readable aur likhne mein asaan ho jaata hai.

- **One-way Data Binding:** React unidirectional data flow use karta hai, matlab data ek hi direction mein flow karta hai, jo applications ko samajhne aur debug karne mein asaan banata hai.

- **Performance:** React virtual DOM aur efficient diff algorithms jaise techniques ka upyog karke performance ko enhance karta hai, jisse direct DOM manipulations minimize hote hain.

- **Flexibility and Modularity:** React ka component-based architecture developers ko modular aur maintainable code banane ki suvidha deta hai, jisse yeh various projects mein flexible hota hai.

Yeh features milkar React ko dynamic aur responsive web applications banane mein efficient aur lokpriya banate hain.</small>


## Q3: React Hooks kya hain aur inka upyog kyun kiya jata hai?

<small>**Answer:** React Hook ek function hai jo functional components ko state aur lifecycle features use karne ki suvidha deta hai. Ye React 16.8 me introduce kiya gaya tha, jisse class components ki zaroorat khatam ho gayi aur code zyada simple aur readable ban gaya. Hooks state manage karne, side effects handle karne, aur reusability badhane me madad karte hain. Ye React development ko aur efficient aur flexible banate hain, saath hi backward compatibility bhi ensure karte hain. 🚀 </small>


## Q4: Funcitonal or class component mein kya difference hai?
<small> 
React mein, components ko functional ya class components ke roop mein banaya ja sakta hai.

- **Functional Components:** Yeh simple JavaScript functions hote hain jo props ko argument ke roop mein lete hain aur React elements return karte hain. Inke paas apna state ya lifecycle methods nahi hote.

- **Class Components:** Yeh ES6 classes hain jo `React.Component` se extend hoti hain. Inke paas apna state aur lifecycle methods hote hain, jo zyada complex logic aur interactions ko sambhalte hain.

React 16.8 mein Hooks ke aane se, ab functional components bhi state aur side effects manage kar sakte hain, jisse class components ki zarurat kam ho gayi hai.
</small> 


## Q5: Props aur state kya hote hain React mein? Dono mein kya antar hai? 

 <small>
React mein, **props** (yaani "properties") aur **state** dono hi components ke data ko manage karne ke liye use hote hain, lekin inka upyog aur visheshtayein alag-alag hain.

- **Props:** Props wo read-only attributes hain jo ek parent component se child component ko pass kiye jate hain. Ye data ko component hierarchy mein neeche ki taraf flow karne dete hain aur immutable hote hain, yaani child component apne props ko modify nahi kar sakta. Isse ek unidirectional data flow ensure hota hai, jo application ko predictable aur debug karne mein aasan banata hai.

- **State:** State ek mutable data structure hai jo component ki vartaman sthiti ki jankari rakhta hai. Yeh component ke andar hi manage hota hai aur samay ke saath badal sakta hai, aam taur par user ke actions ya network responses ke response mein. Jab ek component ka state badalta hai, React component ko dobara render karta hai taaki updated state reflect ho sake.

**Mukhya Antar:**

- **Mutability (Badalne ki kshamata):** Props immutable hain; state mutable hai.

- **Ownership (Adhikar):** Props parent component dwara control kiye jate hain; state component ke andar manage hota hai.

- **Purpose (Uddeshya):** Props data ko child components tak pahunchane ke liye use hote hain; state component ke andar dynamic data ko manage karne ke liye use hota hai.
</small>

## Q6: React Fiber kya hia? 

 <small> Ye react k 16 version m introduce hua tha, 
 React Fiber ek naya reconciliation engine hai jo React me asynchronous rendering ko support karta hai. Yeh UI ko faster aur smooth banata hai by handling high-priority updates pehle aur baaki rendering ko efficiently manage karta hai. 🚀
 
</small>
