TypeScript-এ কিছু বিশেষ Type রয়েছে, যেগুলো Value কীভাবে Assign এবং ব্যবহার করা হবে তা নিয়ন্ত্রণ করে। এর মধ্যে গুরুত্বপূর্ণ তিনটি Type হলো `any`, `unknown` এবং `never`। এগুলোর পার্থক্য বোঝা নিরাপদ ও নির্ভরযোগ্য Application তৈরিতে সাহায্য করে।

 

`any` Type ব্যবহার করলে TypeScript-এর অধিকাংশ Type Checking বন্ধ হয়ে যায়। অর্থাৎ আপনি যেকোনো ধরনের Value Assign করতে পারবেন এবং TypeScript-এর Compiler সাধারণত কোনো Error দেখাবে না। তবে এর কারণে Runtime Error হতে পারে।

```typescript
let value: any = "Hello";
value.toFixed(); // Runtime Error
```

অন্যদিকে, `unknown` Type যেকোনো ধরনের Value গ্রহণ করতে পারে। কিন্তু কোনো Operation করার আগে Value-এর Type Check করতে হয়। এজন্য এটি `any`-এর তুলনায় বেশি নিরাপদ।

```typescript
let value: unknown = "Hello";

if (typeof value === "string") {
    console.log(value.toUpperCase());
}
```

এখানে TypeScript প্রথমে পরীক্ষা করছে Value-টি String কি না। String হলে পরবর্তী Operation করার অনুমতি দিচ্ছে।

`never` Type এমন Value নির্দেশ করে, যা কখনো ঘটতে পারে না। সাধারণত যেসব Function সবসময় Error Throw করে অথবা কখনো Execution শেষ করে না, সেখানে এটি ব্যবহার করা হয়।

```typescript
function throwError(message: string): never {
    throw new Error(message);
}
```

TypeScript-এর Type System-এ `unknown` হলো Safe Top Type, কারণ যেকোনো Value এটিতে Assign করা যায়। কিন্তু Type Check ছাড়া এটিকে অন্য Specific Type-এ Assign করা যায় না। অন্যদিকে, `any` Type Safety-এর নিয়মগুলো এড়িয়ে যায়। আর `never` হলো Bottom Type, যা সব Type-এ Assign করা যায়।

অনির্দিষ্ট Type-এর Value নিয়ে কাজ করার সময় `any`-এর পরিবর্তে `unknown` ব্যবহার করা উচিত। কারণ এটি Type Safety নিশ্চিত করতে সাহায্য করে। প্রয়োজন ছাড়া `any` ব্যবহার করা উচিত নয় এবং Impossible Value বা Unreachable Code বোঝাতে `never` ব্যবহার করা হয়।