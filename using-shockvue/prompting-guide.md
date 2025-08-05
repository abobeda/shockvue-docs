# Prompting Guide

Shockvue makes editing images easy! Specify what you want to change and the model will follow. It is capable of understanding the context of the image, making it easier to edit them without having to describe in detail what you want to do.

This section covers everything you need to know to get reliable, creative, and consistent results when editing images.

{% hint style="info" %}
To edit an image effectively in Shockvue, crafting a precise prompt is crucial. Be explicit and detailed in your prompts to ensure the desired outcome. Clearly articulate the expected result in words.
{% endhint %}

### 1. Basic object modifications

To make straightforward changes (e.g. color, shape), simple prompts like:

> `"Change the yellow car to red"`

...are often all you need. Shockvue  is smart enough to infer what object you're referring to.

<div><figure><img src="../.gitbook/assets/car.jpg" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/car-red.jpg" alt="" width="563"><figcaption><p>Output: Car changed to red</p></figcaption></figure></div>

### 2. Prompt precision: from quick to complex

#### Quick Edits

Short prompts like `"Change the weather"` may work, but could also alter style or composition.

#### Controlled Edits

Be more specific to control output:

> `"Change the weather to a snowy day in the winter"`

<div><figure><img src="../.gitbook/assets/ipanema.png" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/generated-image-Change-the-weather-to-a-snowy-.jpeg" alt="" width="563"><figcaption><p>Output</p></figcaption></figure></div>

If we add more instructions to our prompt, we can have results which are really similar to the input image.

> _`“Change to daytime while maintaining the same style of the painting”`_

<figure><img src="../.gitbook/assets/paint.jpg" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure>

<figure><img src="../.gitbook/assets/paint-day.jpg" alt="" width="563"><figcaption><p>Output</p></figcaption></figure>

#### Complex Instructions

Add multiple instructions to handle several changes:

> _`"Change the setting to a day time, add a lot of people walking the sidewalk while maintaining the same style of the painting"`_

<figure><img src="../.gitbook/assets/paint-more.jpg" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure>

<figure><img src="../.gitbook/assets/paint-more-day.jpg" alt="" width="563"><figcaption><p>Output</p></figcaption></figure>

When combining edits, clarity is key. Too vague = weird output. Too complex = potential confusion. Stay in the sweet spot.

### 3. Style transfer

When working on style transfer prompts, follow those principles:



1. **Name the specific style**: Instead of vague terms like “make it artistic,” specify exactly what style you want (“Transform to Bauhaus art style,” “Convert to watercolor painting”)
2. **Reference known artists or movements**: For more precise results, include recognizable style references (“Renaissance painting style”, “like a 1960s pop art poster”)
3. **Detail the key characteristics**: If naming the style doesn’t work, it might be good to describe the visual elements that define the style:
   * “_Transform to oil painting with visible brushstrokes, thick paint texture, and rich color depth_”
4. **Preserve what matters**: Explicitly state what elements shouldn’t change:
   * “Change to Bauhaus art style while maintaining the original composition and object placement”

<div><figure><img src="../.gitbook/assets/pearl.jpg" alt=""><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/generated-image-Turn-this-image-into-the-emoji.jpeg" alt=""><figcaption><p>Turn this image into the emoji style of Apple iOS system</p></figcaption></figure></div>

### 4. Using input images

You can also use input images as style references to generate new images. For example, with the prompt: _"Using this style, a raccoon and a fox are having coffee sitting at a cafe terrace at night"_ we get:

<div><figure><img src="../.gitbook/assets/flowers.png" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/generated-image-using-this-style--a-raccoon-an.jpeg" alt="" width="563"><figcaption><p>Output</p></figcaption></figure></div>

> `"Using this style, a dog and a cat are having a tea party seated around a small white table"`

<div><figure><img src="../.gitbook/assets/jap.jpg" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/generated-image-using-this-style--a-dog-and-a-.jpeg" alt="" width="563"><figcaption><p>Output</p></figcaption></figure></div>

### 5. Transform images into different styles

Shockvue lets you transform images in creative ways. On the example below, we restyle our photo into different visual styles and also doing different activities.\
If your goal is to dramatically change the input image, it is generally a good idea to do it step by step like the sequence below:

<div><figure><img src="../.gitbook/assets/guy.jpg" alt=""><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/guy-claymation.jpg" alt=""><figcaption><p>Restyled to Claymation</p></figcaption></figure> <figure><img src="../.gitbook/assets/guy-claymation-plants.jpg" alt=""><figcaption><p>Character picking up plants</p></figcaption></figure></div>

For Character consistency, you can follow this framework to keep the same character across edits:



1. **Establish the reference:** Begin by clearly identifying your character



* “This person…” or “The woman with short black hair…”



2. **Specify the transformation:** Clearly state what aspects are changing



* Environment: “…now in a tropical beach setting”&#x20;
* Activity: “…now picking up weeds in a garden”&#x20;
* Style: “Transform to Claymation style while keeping the same person”



3. **Preserve identity markers:** Explicitly mention what should remain consistent



* “…while maintaining the same facial features, hairstyle, and expression”&#x20;
* “…keeping the same identity and personality”&#x20;
* “…preserving their distinctive appearance”

### 6. Text editing in images

Shockvue can edit visible text in signs, posters, and labels using this format:

> `Replace 'original text' with 'new text'`

<div><figure><img src="../.gitbook/assets/generated-image-poster.jpg" alt=""><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/generated-image-poster-love.jpg" alt=""><figcaption><p>Replace red text from "bleed" to "love"; keep the font style.</p></figcaption></figure></div>

**Text Editing Best Practices**



* Use clear, readable fonts when possible. Complex or stylized fonts may be harder to edit
* Specify preservation when needed. For example: “Replace ‘joy’ with ‘BFL’ while maintaining the same font style and color”
* Keep text length similar - Dramatically longer or shorter text may affect layout



### 7. Zone Edit (Beta)

Zone Edit is a powerful (experimental) feature that allows you to apply your edits to specific areas of an image. By selecting one or more zones, you can tell the AI exactly where to focus the changes described in your prompt, leaving the rest of the image untouched.

This gives you precise control over the editing process, enabling you to perform targeted modifications, additions, or removals with greater accuracy.

It is also possible to use Visual cues to suggest to the model where to make edits. This can be particularly helpful when you want to make targeted changes to specific areas of an image. By providing visual markers or reference points, you can guide the model to focus on particular regions.

<div><figure><img src="../.gitbook/assets/zone.png" alt=""><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/zone-edi.jpg" alt="" width="563"><figcaption><p>Add hats in the selected areas</p></figcaption></figure></div>

**How It Works**

When you activate Zone Edit, you can draw rectangular masks directly onto your image. These masks define the areas where your prompt will be applied. The AI then uses these "visual cues" to understand the context of your edit, ensuring that the changes are constrained to the highlighted regions.

For example, you can select a person's shirt and use the prompt "change to a red shirt" to modify only the color of the shirt, without affecting the background or the person's face.

**How to Use It**



1. **Activate Zone Edit:** Click on the **Zone Edit** icon (a square) in the editing toolbar. This will enable pencil mode.
2. **Select Areas:** Click and drag on the image to draw one or more rectangular zones where you want to apply your edit.
3. **Write Your Prompt:** Describe the change you want to make within the selected areas. When making distinct changes to two sections of an image, refer to 'in the selected area' for the first section and 'in the second selected area' for the second section. Do not describe the sections as "orange area" or "lime area."
4. **Apply the Edit:** Click the **Edit** button to generate the image. The AI will apply the prompt's instructions exclusively to the zones you defined.

### 8. When results don’t match expectations

#### General Troubleshooting Tip <a href="#general-troubleshooting-tip" id="general-troubleshooting-tip"></a>

If the model is changing elements you want to keep unchanged, be explicit about preservation in your prompt. For example: _“everything else should stay black and white”_ or “_maintain all other aspects of the original image_.”

#### [​](https://docs.bfl.ai/guides/prompting_guide_kontext_i2i#character-identity-changes-too-much)Character identity changes too much <a href="#character-identity-changes-too-much" id="character-identity-changes-too-much"></a>

When transforming a person (changing their clothing, style, or context), it’s easy to lose their unique identity features if prompts aren’t specific enough.

* Try to be more specific about identity markers (“maintain the exact same face, hairstyle, and distinctive features”)
* **Example**: _“Transform the man into a viking warrior while preserving his exact facial features, eye color, and facial expression”_

<div><figure><img src="../.gitbook/assets/man.jpg" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/man viking.jpg" alt="" width="563"><figcaption><p>Vague prompt result</p></figcaption></figure></div>

<div><figure><img src="../.gitbook/assets/man-viking-detailed.jpg" alt=""><figcaption><p>Detailed prompt result</p></figcaption></figure> <figure><img src="../.gitbook/assets/man-viking-focused.jpg" alt=""><figcaption><p>Focused prompt result</p></figcaption></figure></div>

**Vague prompts replace identity:**

* **Prompt:** _“Transform the person into a Viking”_ → Complete replacement of facial features, hair, and expression

**Detailed prompts preserve identity:**

* **Prompt:** _“Transform the man into a viking warrior while preserving his exact facial features, eye color, and facial expression”_ → Maintains core identity while changing context

**Focused prompts change only what’s needed:**

* **Prompt:** _“Change the clothes to be a viking warrior”_ → Keeps perfect identity while only modifying the specified element

**Why this happens?**&#x54;he verb “transform” without qualifiers often signals to _Kontext_ that a complete change is desired. It might be useful to use other words for example in this context if you want to maintain specific aspects of the original image.

#### [​](https://docs.bfl.ai/guides/prompting_guide_kontext_i2i#composition-control)Composition Control <a href="#composition-control" id="composition-control"></a>

When editing backgrounds or scenes, you often want to keep the subject in exactly the same position, scale, and pose. Simple prompts can sometimes change some of those aspects.&#x20;

**Simple prompts causing unwanted changes:**



* **Prompt:** _“He’s now on a sunny beach”_ → Subject position and scale shift
* **Prompt:** _“Put him on a beach”_ → Camera angle and framing change

<div><figure><img src="../.gitbook/assets/oldman.jpg" alt="" width="563"><figcaption><p>Input image</p></figcaption></figure> <figure><img src="../.gitbook/assets/oldman-beach.jpg" alt=""><figcaption><p>Simple beach prompt</p></figcaption></figure> <figure><img src="../.gitbook/assets/oldman-beach-prompt.jpg" alt=""><figcaption><p>Put on beach prompt</p></figcaption></figure></div>

**Precise prompts maintain exact positioning:**



* **Prompt:** _“Change the background to a beach while keeping the person in the exact same position, scale, and pose. Maintain identical subject placement, camera angle, framing, and perspective. Only replace the environment around them”_ → Better preservation of subject

**Why this happens?**

Vague instructions like _“put him on a beach”_ leave too much to interpretation. _Kontext_ might choose to:



* Adjust the framing to match typical beach photos
* Change the camera angle to show more of the beach
* Reposition the subject to better fit the new setting

#### [​](https://docs.bfl.ai/guides/prompting_guide_kontext_i2i#style-isn%E2%80%99t-applying-correctly)Style isn’t applying correctly <a href="#style-isn-e2-80-99t-applying-correctly" id="style-isn-e2-80-99t-applying-correctly"></a>

When applying certain styles, simple prompts might create inconsistent results or lose important elements of the original composition. We could see that in the example above.

**Basic style prompts can lose important elements:**



* **Prompt:** _“Make it a sketch”_ → While the artistic style is applied, some details are lost.

**Precise style prompts maintain structure:**



* **Prompt:** _“Convert to pencil sketch with natural graphite lines, cross-hatching, and visible paper texture”_ → Preserves the scene while applying the style. You can see more details in the background; more cars are also appearing on the image.

<figure><img src="../.gitbook/assets/man-gun.jpg" alt=""><figcaption><p>Input image</p></figcaption></figure>

<div><figure><img src="../.gitbook/assets/man-gun-basic-sketch.jpg" alt=""><figcaption><p>Basic sketch prompt</p></figcaption></figure> <figure><img src="../.gitbook/assets/man-gun-precise-sketch.jpg" alt=""><figcaption><p>Precise sketch prompt</p></figcaption></figure></div>
