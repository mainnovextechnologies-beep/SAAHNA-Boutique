# SAAHNA Boutique — React + Vite Demo

A polished, responsive boutique website demo inspired by SAAHNA, a personalised fashion boutique in Vijayawada, Andhra Pradesh. Includes collections, services, an enquiry form, demo-only floating call/WhatsApp actions, responsive navigation, SEO metadata, JSON-LD structured data, robots.txt, sitemap.xml and favicon.

## Run locally

```bash
npm install
npm run dev
```

Production build:

```bash
npm run build
npm run preview
```

## Configuration

Edit `src/config.js` for the business name, location, phone, email, hours, theme colours, image URLs, collection cards, services and SEO content. Edit `index.html` for canonical URL and JSON-LD if the domain or business changes. Update `public/robots.txt` and `public/sitemap.xml` to the final production domain.

## Demo behaviour

`demoMode: true` is set in the config. All call and WhatsApp buttons show a polite demo notice. The enquiry form validates locally and displays the notice; it does not send, save or store form details. This intentional behaviour is suitable for a client preview. Before a live launch, implement the desired real WhatsApp/call behaviour, update the contact details with the owner's permission, and remove the demo-only warning.

## SEO launch checklist

- Replace `https://example.com/` in canonical URL, JSON-LD, sitemap and robots.txt with the actual production domain.
- Confirm all business contact details, address, hours, images and service claims with the owner.
- Add a real logo, original product photos, social links and a custom domain favicon.
- Verify the domain in Google Search Console, submit `/sitemap.xml`, and test structured data.
- Add analytics and a privacy notice if you introduce analytics, lead storage or third-party forms.

## Important

This is a demonstration site, not the official website of the business. Product photos are remote illustrative images and product availability is not represented. Obtain permission before publishing another business's identity, logo, images or contact information. The sample domain is intentionally `example.com` and must be changed before deployment.


## Collections and Google Maps
- The collections grid contains 38 configurable collection cards in `src/config.js`.
- Update `mapsQuery` and `mapsUrl` in `src/config.js` to the client's real business name/address. The map embed uses a Google Maps search iframe and does not require a Maps Embed API key. Confirm the exact pin before publishing.
- For an official Maps Embed API implementation, see https://developers.google.com/maps/documentation/embed/quickstart; that API requires an API key.


### Image reliability fix
The project includes local fallback fashion images in `public/images/`. If an external image URL fails or is blocked, the page automatically switches to a bundled local image instead of showing a broken/blank image. Replace the demo imagery with client-approved photos before production.
