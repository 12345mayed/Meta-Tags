function generateMetaTags() {
    let content = document.getElementById("content").value;
    
    let metaTitle = content.substring(0, 60);  // تحديد 60 حرفًا كحد أقصى
    let metaDescription = content.substring(0, 160); // تحديد 160 حرفًا
    let metaKeywords = content.toLowerCase().split(" ").slice(0, 10).join(", "); // استخراج 10 كلمات مفتاحية

    let metaTags = `
    <meta name="title" content="${metaTitle}">
    <meta name="description" content="${metaDescription}">
    <meta name="keywords" content="${metaKeywords}">
    `;

    document.getElementById("result").textContent = metaTags;
}