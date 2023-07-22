Styling HTML `<input/>` Element:
This article will provide you take a close look on how to style form inputs, it will not include common properties.

1. Understanding HTML Input:

By default, input apperance is predefined by user agent (web browser),     without any css, that's why it doesn't take the full width of its parent.

According to MDN, an input element is either a replaced element or a widget based on its type attribute.

HTML spec also says that an <input> element can be replaced, because <input> elements of the "image" type are replaced elements similar to <img>. However, other form controls, including other types of <input> elements, are explicitly listed as non-replaced elements (the spec describes their default platform-specific rendering with the term "Widgets").



2. Input and CSS Properties:





3. Input and Psuedo Elemets:

 ::before & ::after- Similar to all replaced element in HTML, it is not possible to use psuedo elements with input (depending on the type attribute), for example, ::before + after. - There is a simple trick to use pusedo elements:

results:

Note: adding padding-right in case of long text, it won't overlap with the image. it sould be at least the same with of the image.





::placeholder: change the styling of the placeholder text





4. Input and Psuedo Classes:

:placeholder-shown- :placeholder-show targets input elements that has a placeholder, unlike ::placeholder which targets the placeholder.- :placeholder-shown can still affect the styling of the placeholder text, since it’s a parent element (e.g. font-size).- some browsers makes placeholder text of input elements semi-transparent. When setting a custom color for placeholder text, keep in mind that it will appear lighter then the color you used. A way to fix that is adding opacity:1;‌

:in-range & :out-of-range

results:



:valid & :invalid



results:







Call to action

رسالة تحفز القارء على التفاعل أو التعليق أو طلب رأيه

hashtags

هاشتاغز مرتبطة بالمحتوى

authors
كاتب المنشور
مصمم المنشور
تم النشر بواسطة



















**Styling HTML \`<input/>\` Element:**
`This article will provide you take a close look on how to style form inputs, it will not include common properties.`

`1. Understanding HTML Input:`

- By default, input apperance is predefined by user agent (web browser),     without any css, that's why it doesn't take the full width of its parent.
- According to MDN, an input element is either a **replaced element** or a **widget** based on its type attribute.

> `HTML spec also says that an <input> element can be replaced, because <input> elements of the "image" type are replaced elements similar to <img>. However, other form controls, including other types of <input> elements, are explicitly listed as non-replaced elements (the spec describes their default platform-specific rendering with the term "Widgets").`

---

`2. Input and CSS Properties:`

![Input-CSS-Properties.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b015fbbaff51af7fe49291/download/Input-CSS-Properties.png)

---

`3. Input and Psuedo Elemets`:

- ` ::before & ::after`
  \- Similar to all replaced element in HTML, it is not possible to use psuedo elements with input (depending on the type attribute), for example, ::before + after. - There is a simple trick to use pusedo elements:
  ![before-after-code.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b016b02188149a0d8f9686/download/before-after-code.png)
  results:

`Note: adding` padding-right `in case of long text, it won't overlap with the image. it sould be at least the same with of the image.`

![before-after-result.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b017364b4630158bee8f00/download/before-after-result.png)

‌

- ::placeholder: change the styling of the placeholder text
  ![placeholder.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b0179fe5149b6a25505892/download/placeholder.png)

---

`4. Input and Psuedo Classes`:

- `:placeholder-shown`
  \- **:placeholder-show** targets input elements that has a placeholder, unlike **::placeholder** which targets the placeholder.
  \- **:placeholder-shown** can still affect the styling of the placeholder text, since it’s a parent element (e.g. font-size).
  \- some browsers makes placeholder text of input elements semi-transparent. When setting a custom color for placeholder text, keep in mind that it will appear lighter then the color you used. A way to fix that is adding **opacity:1;**
  ‌
- `:in-range & :out-of-range`
  ![in-range%26out-of-range.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b01842f1c162073436e445/download/in-range%26out-of-range.png)
  results:

![range-example.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b01864315c221b383f2ec5/download/range-example.png)

- `:valid & :invalid`
  ![invalid\_vs\_valid.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b0187684bd027ff3cd78aa/download/invalid_vs_valid.png)

results:

![vaild-invalid-example.png](https://trello.com/1/cards/64a86575eca5634a5e345827/attachments/64b0188d916a6617bd17d748/download/vaild-invalid-example.png)

‌

‌

**Call to action**

رسالة تحفز القارء على التفاعل أو التعليق أو طلب رأيه

**hashtags**

هاشتاغز مرتبطة بالمحتوى

**authors**
كاتب المنشور
مصمم المنشور
تم النشر بواسطة
