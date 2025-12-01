<meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QURESHI X ARMY 🗿 SIM & CNIC Information Lookup</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background:
              linear-gradient(
                135deg,
                rgba(26, 42, 108, 0.85) 0%,
                rgba(178, 31, 31, 0.85) 50%,
                rgba(253, 187, 45, 0.85) 100%
              ),
              url('https://img.sanishtech.com/u/3be8278fb47e5a02dc83d804732bc915.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;

            color: #333;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .container {
            width: 100%;
            max-width: 1100px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            overflow: hidden;
            margin-top: 30px;
        }
        
        header {
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            color: white;
            padding: 25px;
            text-align: center;
        }
        
        h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .content {
            padding: 30px;
        }
        
        .input-section {
            margin-bottom: 30px;
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
        }
        
        .input-group {
            display: flex;
            margin-bottom: 15px;
        }
        
        input {
            flex: 1;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 8px 0 0 8px;
            font-size: 1.1rem;
            transition: border-color 0.3s;
        }
        
        input:focus {
            outline: none;
            border-color: #1a2a6c;
        }
        
        button {
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
            color: white;
            border: none;
            padding: 0 25px;
            border-radius: 0 8px 8px 0;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button:disabled {
            background: #cccccc;
            cursor: not-allowed;
            transform: none;
        }
        
        .search-type {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
        }
        
        .search-option {
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
        }
        
        .search-option input {
            width: 18px;
            height: 18px;
        }
        
        .examples {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .example-btn {
            background: #e9ecef;
            color: #333;
            border: 1px solid #ced4da;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        .example-btn:hover {
            background: #dee2e6;
        }
        
        .result-section {
            display: none;
        }
        
        .result-section.active {
            display: block;
        }
        
        .loading {
            text-align: center;
            padding: 40px;
            display: none;
        }
        
        .loading.active {
            display: block;
        }
        
        .spinner {
            border: 5px solid #f3f3f3;
            border-top: 5px solid #1a2a6c;
            border-radius: 50%;
            width: 50px;
            height: 50px;
            animation: spin 1s linear infinite;
            margin: 0 auto 15px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* RESULT STYLING */
        .result-card {
            background-color: #f9f9f9;
            border-radius: 12px;
            padding: 25px;
            margin-top: 20px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease;
        }
        
        .result-card:hover {
            transform: translateY(-5px);
        }
        
        .success-result {
            border-left: 6px solid #28a745;
            background: linear-gradient(to right, #f9f9f9, #f0f9f0);
        }
        
        .error-result {
            border-left: 6px solid #dc3545;
            background: linear-gradient(to right, #f9f9f9, #fdf0f0);
        }
        
        .result-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
            padding: 20px;
            background: linear-gradient(135deg, #e3f2fd, #f3e5f5);
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .searched-value {
            font-size: 1.4rem;
            font-weight: 700;
            color: #1a2a6c;
        }
        
        .search-type-badge {
            display: inline-block;
            padding: 5px 12px;
            border-radius: 15px;
            font-weight: 600;
            font-size: 0.8rem;
            margin-left: 10px;
            background: #1a2a6c;
            color: white;
        }
        
        .sim-count {
            display: inline-block;
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 1rem;
            background-color: #28a745;
            color: white;
        }
        
        .result-status {
            display: inline-block;
            padding: 8px 20px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 1rem;
        }
        
        .status-found {
            background-color: #E8F5E9;
            color: #2E7D32;
        }
        
        .status-error {
            background-color: #FFEBEE;
            color: #C62828;
        }
        
        .sim-cards-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }
        
        .sim-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            border-top: 4px solid #1a2a6c;
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .sim-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(to right, #1a2a6c, #b21f1f);
        }
        
        .sim-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }
        
        .sim-number {
            font-size: 1.4rem;
            font-weight: 700;
            color: #1a2a6c;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .sim-number::before {
            content: '📞';
            font-size: 1.2rem;
        }
        
        .sim-details {
            margin-top: 15px;
        }
        
        .detail-row {
            display: flex;
            margin-bottom: 12px;
            padding-bottom: 12px;
            border-bottom: 1px solid #f0f0f0;
        }
        
        .detail-label {
            font-weight: 600;
            color: #555;
            width: 100px;
            flex-shrink: 0;
        }
        
        .detail-value {
            color: #333;
            flex: 1;
        }
        
        .person-name {
            font-size: 1.2rem;
            font-weight: 600;
            color: #b21f1f;
            margin-bottom: 5px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .person-name::before {
            content: '👤';
            font-size: 1rem;
        }
        
        .single-result {
            background: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            margin: 20px 0;
            border-left: 6px solid #1a2a6c;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .info-card {
            background: #f8f9fa;
            border-radius: 10px;
            padding: 18px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
            border-left: 4px solid #1a2a6c;
            transition: transform 0.2s;
        }
        
        .info-card:hover {
            transform: translateY(-3px);
        }
        
        .info-label {
            font-size: 0.85rem;
            color: #666;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .info-value {
            font-size: 1.1rem;
            font-weight: 600;
            color: #333;
        }
        
        .no-data {
            text-align: center;
            padding: 40px;
            color: #666;
            font-style: italic;
        }
        
        .no-data svg {
            margin-bottom: 15px;
            opacity: 0.5;
        }
        
        .credit {
            text-align: center;
            margin-top: 25px;
            padding: 15px;
            background: linear-gradient(to right, #e3f2fd, #f3e5f5);
            border-radius: 10px;
            font-weight: 600;
            color: #555;
            font-size: 1rem;
        }
        
        footer {
            margin-top: 30px;
            text-align: center;
            color: white;
            font-size: 0.9rem;
            opacity: 0.9;
        }

        @media (max-width: 768px) {
            .container {
                margin-top: 10px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .input-group {
                flex-direction: column;
            }
            
            input {
                border-radius: 8px;
                margin-bottom: 10px;
            }
            
            button {
                border-radius: 8px;
                padding: 15px;
            }
            
            .result-header {
                flex-direction: column;
                gap: 15px;
                text-align: center;
            }
            
            .sim-cards-container {
                grid-template-columns: 1fr;
            }
            
            .info-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>SIM & CNIC Information Lookup</h1>
            <p class="subtitle">Ghosty Find information by SIM number or CNIC</p>
        </header>
        
        <div class="content">
            <div class="input-section">
                <div class="search-type">
                    <div class="search-option">
                        <input type="radio" id="searchSim" name="searchType" value="sim" checked>
                        <label for="searchSim">QURESHI X ARMY 🗿 Search by SIM Number</label>
                    </div>
                    <div class="search-option">
                        <input type="radio" id="searchCnic" name="searchType" value="cnic">
                        <label for="searchCnic">QURESHI X ARMY 🗿 Search by CNIC</label>
                    </div>
                </div>
                
                <div class="input-group">
                    <input type="text" id="searchInput" placeholder="Enter SIM number or CNIC" maxlength="15">
                    <button id="lookupBtn">Search</button>
                </div>
                
                <div class="examples">
                    <span>Try: </span>
                    <button class="example-btn" data-value="03132737647" data-type="sim">03704309413 (SIM)</button>
                    <button class="example-btn" data-value="3240214025071" data-type="cnic">3240214025071 (CNIC)</button>
                    <button class="example-btn" data-value="03704309413" data-type="sim">03704309413 (SIM)</button>
                </div>
            </div>
            
            <div class="loading" id="loadingIndicator">
                <div class="spinner"></div>
                <p>Searching for information...</p>
            </div>
            
            <div class="result-section" id="resultSection">
                <!-- Results will be displayed here -->
            </div>
        </div>
    </div>
    
    <footer>
        <p>QURESHI X ARMY 🗿 SIM & CNIC Information API &copy; 2023 | All data is for demonstration purposes only</p>

        <a href="https://whatsapp.com/channel/0029Vb6wk97FnSz757IPej32" target="_blank" 
           style="background:#25D366;padding:12px 25px;color:white;border-radius:8px;
                  font-size:1rem;text-decoration:none;display:inline-block;margin-top:10px;">
           Join Our WhatsApp Group
        </a>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const searchInput = document.getElementById('searchInput');
            const lookupBtn = document.getElementById('lookupBtn');
            const loadingIndicator = document.getElementById('loadingIndicator');
            const resultSection = document.getElementById('resultSection');
            const exampleButtons = document.querySelectorAll('.example-btn');
            const searchTypeRadios = document.querySelectorAll('input[name="searchType"]');
            
            // API URL
            const apiUrl = 'https://fam-official.serv00.net/api/famofc_simdatabase.php';
            
            // Update placeholder based on selected search type
            searchTypeRadios.forEach(radio => {
                radio.addEventListener('change', function() {
                    if (this.value === 'sim') {
                        searchInput.placeholder = 'Enter SIM number (e.g., 03338570120)';
                    } else {
                        searchInput.placeholder = 'Enter CNIC number (e.g., 3240214025071)';
                    }
                });
            });
            
            // Example button click handlers
            exampleButtons.forEach(button => {
                button.addEventListener('click', function() {
                    searchInput.value = this.getAttribute('data-value');
                    const type = this.getAttribute('data-type');
                    
                    // Set the radio button based on example type
                    document.getElementById(type === 'sim' ? 'searchSim' : 'searchCnic').checked = true;
                    
                    // Trigger the change event to update placeholder
                    const event = new Event('change');
                    document.getElementById(type === 'sim' ? 'searchSim' : 'searchCnic').dispatchEvent(event);
                    
                    lookupInfo();
                });
            });
            
            // Lookup button click handler
            lookupBtn.addEventListener('click', lookupInfo);
            
            // Enter key handler
            searchInput.addEventListener('keypress', function(e) {
                if (e.key === 'Enter') {
                    lookupInfo();
                }
            });
            
            function lookupInfo() {
                const searchValue = searchInput.value.trim();
                const searchType = document.querySelector('input[name="searchType"]:checked').value;
                
                if (!searchValue) {
                    alert('Please enter a search value');
                    return;
                }
                
                // Validate input based on search type
                if (searchType === 'sim' && !/^\d{10,12}$/.test(searchValue)) {
                    alert('Please enter a valid 10-12 digit SIM number');
                    return;
                }
                
                if (searchType === 'cnic' && !/^\d{13}$/.test(searchValue)) {
                    alert('Please enter a valid 13-digit CNIC number');
                    return;
                }
                
                // Show loading indicator
                loadingIndicator.classList.add('active');
                resultSection.classList.remove('active');
                lookupBtn.disabled = true;
                
                // Make API request with the same parameter for both types
                fetch(`${apiUrl}?number=${encodeURIComponent(searchValue)}`)
                    .then(response => {
                        if (!response.ok) {
                            throw new Error('Network response was not ok');
                        }
                        return response.json();
                    })
                    .then(data => {
                        displayResults(data, searchType, searchValue);
                    })
                    .catch(error => {
                        console.error('Error:', error);
                        displayError('Failed to fetch data. Please try again later.', searchType, searchValue);
                    })
                    .finally(() => {
                        loadingIndicator.classList.remove('active');
                        lookupBtn.disabled = false;
                    });
            }
            
            function displayResults(data, searchType, searchValue) {
                resultSection.innerHTML = '';
                
                if (data.success) {
                    // Success case
                    const resultCard = document.createElement('div');
                    resultCard.className = 'result-card success-result';
                    
                    const searchTypeText = searchType === 'sim' ? 'SIM Number' : 'CNIC';
                    const searchTypeBadge = `<span class="search-type-badge">${searchTypeText}</span>`;
                    
                    let resultHTML = `
                        <div class="result-header">
                            <div>
                                <div class="searched-value">${searchTypeText}: ${searchValue} ${searchTypeBadge}</div>
                                ${searchType === 'cnic' ? `<div class="sim-count">${data.data.length} SIM Card(s) Found</div>` : ''}
                            </div>
                            <span class="result-status status-found">Information Found</span>
                        </div>
                    `;
                    
                    if (data.data && data.data.length > 0) {
                        if (searchType === 'cnic' || data.data.length > 1) {
                            // Display as SIM cards (for CNIC search or multiple results)
                            resultHTML += `<div class="sim-cards-container">`;
                            
                            data.data.forEach((sim, index) => {
                                resultHTML += `
                                    <div class="sim-card">
                                        <div class="sim-number">${sim.number || 'N/A'}</div>
                                        <div class="person-name">${sim.name || 'N/A'}</div>
                                        <div class="sim-details">
                                            <div class="detail-row">
                                                <div class="detail-label">CNIC:</div>
                                                <div class="detail-value">${sim.cnic || 'N/A'}</div>
                                            </div>
                                            <div class="detail-row">
                                                <div class="detail-label">Address:</div>
                                                <div class="detail-value">${sim.address || 'N/A'}</div>
                                            </div>
                                        </div>
                                    </div>
                                `;
                            });
                            
                            resultHTML += `</div>`;
                        } else {
                            // Single result for SIM search
                            const sim = data.data[0];
                            resultHTML += `
                                <div class="single-result">
                                    <div class="info-grid">
                                        <div class="info-card">
                                            <div class="info-label">SIM Number</div>
                                            <div class="info-value">${sim.number || 'N/A'}</div>
                                        </div>
                                        <div class="info-card">
                                            <div class="info-label">Name</div>
                                            <div class="info-value">${sim.name || 'N/A'}</div>
                                        </div>
                                        <div class="info-card">
                                            <div class="info-label">CNIC</div>
                                            <div class="info-value">${sim.cnic || 'N/A'}</div>
                                        </div>
                                        <div class="info-card">
                                            <div class="info-label">Address</div>
                                            <div class="info-value">${sim.address || 'N/A'}</div>
                                        </div>
                                    </div>
                                </div>
                            `;
                        }
                    } else {
                        resultHTML += `
                            <div class="no-data">
                                <svg width="64" height="64" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM13 17H11V15H13V17ZM13 13H11V7H13V13Z" fill="#9e9e9e"/>
                                </svg>
                                <p>No information found for this ${searchType === 'sim' ? 'SIM number' : 'CNIC'}.</p>
                            </div>
                        `;
                    }
                    
                    resultHTML += `<div class="credit">Information provided by: ${data.credit || 'Ghosty'}</div>`;
                    resultCard.innerHTML = resultHTML;
                    resultSection.appendChild(resultCard);
                } else {
                    // Error case
                    const resultCard = document.createElement('div');
                    resultCard.className = 'result-card error-result';
                    
                    const searchTypeText = searchType === 'sim' ? 'SIM Number' : 'CNIC';
                    const searchTypeBadge = `<span class="search-type-badge">${searchTypeText}</span>`;
                    
                    resultCard.innerHTML = `
                        <div class="result-header">
                            <div class="searched-value">${searchTypeText}: ${searchValue} ${searchTypeBadge}</div>
                            <span class="result-status status-error">Error</span>
                        </div>
                        <div style="padding: 30px; text-align: center;">
                            <svg width="48" height="48" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" style="margin-bottom: 15px;">
                                <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM13 17H11V15H13V17ZM13 13H11V7H13V13Z" fill="#dc3545"/>
                            </svg>
                            <h3 style="color: #C62828; margin-bottom: 10px;">Unable to Retrieve Information</h3>
                            <p style="color: #666; font-size: 1.1rem;">${data.error || 'An unknown error occurred'}</p>
                        </div>
                        <div class="credit">Service by: ${data.credit || 'QURESHI'}</div>
                    `;
                    
                    resultSection.appendChild(resultCard);
                }
                
                resultSection.classList.add('active');
            }
            
            function displayError(message, searchType, searchValue) {
                resultSection.innerHTML = '';
                
                const resultCard = document.createElement('div');
                resultCard.className = 'result-card error-result';
                
                const searchTypeText = searchType === 'sim' ? 'SIM Number' : 'CNIC';
                const searchTypeBadge = `<span class="search-type-badge">${searchTypeText}</span>`;
                
                resultCard.innerHTML = `
                    <div class="result-header">
                        <div class="searched-value">${searchTypeText}: ${searchValue} ${searchTypeBadge}</div>
                        <span class="result-status status-error">Network Error</span>
                    </div>
                    <div style="padding: 30px; text-align: center;">
                        <svg width="48" height="48" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" style="margin-bottom: 15px;">
                            <path d="M12 2C6.48 2 2 6.48 2 12C2 17.52 6.48 22 12 22C17.52 22 22 17.52 22 12C22 6.48 17.52 2 12 2ZM13 17H11V15H13V17ZM13 13H11V7H13V13Z" fill="#dc3545"/>
                        </svg>
                        <h3 style="color: #C62828; margin-bottom: 10px;">Connection Problem</h3>
                        <p style="color: #666; font-size: 1.1rem;">${message}</p>
                    </div>
                `;
                
                resultSection.appendChild(resultCard);
                resultSection.classList.add('active');
            }
        });
    </script>
</body>
</html>
