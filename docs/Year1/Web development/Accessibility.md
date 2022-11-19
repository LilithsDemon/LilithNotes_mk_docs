# Accessibility

There are a lot of different things we can use to improve accessibility

## Alt tags

Alt tags go onto images and allow the text to be spoken aloud for people that might have visual imparements, this also allows for increasing SEO.

``` html
<img src="img/img.png" alt="An image of a black cat on a bed">
```

Alt text describes the apperance or function of an image on a page. Alt text is read aloud by screen readers used by visually impared users, displays in place of an image if it fails to load and is index by search engine bots to better understand the content of your page

Alt text uses:
- Adding alternative text to images on your site is a principle of web accessibility.
- Alt attributes enable screen readers to read the information about on-page images for the benefit of a person with complete lack of sight, visually impaired, or who is otherwise unable to view the images on the page.
- Alt text will be displayed in place of an image if an image file cannot load.
- Alt text provides better image context/descriptions to search engine crawlers, helping them to index and rank an image properly in image search. It also provides search engines with contextual information about the content on the page.

## Suitable colour themes

It is very important when creating a website to use suitable colours that match each other and do not "clash".
This is very important for different groups of people such as people with colour blindness or individuals with dyslexia.

Colour blindness is a common problem and affects about 1 in 12 men and 1 in 200 women. Making it estimated to be 300 million people in the world with colour blindness.

This makes it really important to ensure that sites have good colour themes that will not block colour blind people from using it.

It is estimated that the largest type of colour blindess is red/green colour blindness so these are a colour combination that is highly suggested to avoid.

## Label Tag

A label tag is very much like [alt tags](#alt-tags) in that they are read by users with screen readers.

They are used in input elements and are read out when it is focused by a user with a screen reader. This is very useful as it allows the user to be able to know which data they should be putting in and allows a more precise use of the website allowing it to be usebale more more individuals


## Use of HTML tags

HTML has a lot of tags, and they have a lot of benefits of learning and using, some of these include that they have inbuilt styling and can be more easily modified to being better for any accessibilty needs.

For example a button in HTML could be made using:
``` html
<div>Button Text</div> 
```

But it would be more useful to do: 
``` html
<button>Button Text</button> 
```

Using headers allows people with the need of accessibilty to more easily access and use your site and therefore have a better experience on it and use it correctly.