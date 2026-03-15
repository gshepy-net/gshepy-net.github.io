---
layout: default
---

<a href="{{ site.gshepy__api_url }}/update/installer" id="link_download">Скачать установщик</a>

<script>
    const urlBase = new URL('update', '{{ site.gshepy__api_url }}');

    const urlEndpoint = new URL('./get_last_version', urlBase);

    let response = fetch(urlEndpoint, {
        method: 'GET',
    })
    .then(response => {
        if (!response.ok) {
            throw new Error('Network response was not ok');
        }

        return response.json();
    })
    .then(data => {
        console.log('Success:', data);

        const url = new URL('.' + data.url_path, urlBase);

        document.getElementById("link_download").href = url.toString();
    })
    .catch(error => {
        console.error('Error:', error);
    });
</script>
