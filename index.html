<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Free AI-Powered Invoice Generator. Create professional invoices in 30 seconds. Download PDF instantly. No signup required.">
    <meta name="keywords" content="free invoice generator, invoice pdf download, online invoice maker, freelancers invoice">
    <title>InvoiceBuddy - Free Invoice Generator & PDF Download</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#4f46e5',
                        secondary: '#818cf8',
                        accent: '#fbbf24',
                        dark: '#1e293b'
                    }
                }
            }
        }
    </script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        body { font-family: 'Inter', sans-serif; scroll-behavior: smooth; }
        .item-row:hover { background-color: #f8fafc; }
    </style>
</head>
<body class="bg-gray-50 text-gray-800">
    <!-- Navigation - same as yours -->
    <nav class="bg-white shadow-sm sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <i class="fas fa-file-invoice-dollar text-primary text-2xl mr-2"></i>
                    <span class="font-bold text-xl text-dark">Invoice<span class="text-primary">Buddy</span></span>
                </div>
                <div class="flex items-center space-x-4">
                    <button id="downloadPdfBtn" class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg text-sm font-medium">
                        <i class="fas fa-download mr-2"></i>Download PDF
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Invoice Creator Form -->
    <section id="invoiceForm" class="py-16 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-dark mb-4">Create New Invoice</h2>
            </div>
            
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <div class="lg:col-span-2">
                    <form id="invoiceFormElement" class="space-y-8">
                        <!-- From Section -->
                        <div class="bg-gray-50 p-6 rounded-xl shadow-sm">
                            <h3 class="text-lg font-semibold text-dark mb-4">From</h3>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <input id="fromName" type="text" placeholder="Your Name" class="w-full px-4 py-2 border rounded-lg">
                                <input id="fromEmail" type="email" placeholder="Your Email" class="w-full px-4 py-2 border rounded-lg">
                                <textarea id="fromAddress" class="md:col-span-2 w-full px-4 py-2 border rounded-lg" rows="2" placeholder="Your Address"></textarea>
                            </div>
                        </div>

                        <!-- To Section -->
                        <div class="bg-gray-50 p-6 rounded-xl shadow-sm">
                            <h3 class="text-lg font-semibold text-dark mb-4">To</h3>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <input id="toName" type="text" placeholder="Client Name" class="w-full px-4 py-2 border rounded-lg">
                                <input id="toEmail" type="email" placeholder="Client Email" class="w-full px-4 py-2 border rounded-lg">
                                <textarea id="toAddress" class="md:col-span-2 w-full px-4 py-2 border rounded-lg" rows="2" placeholder="Client Address"></textarea>
                            </div>
                        </div>

                        <!-- Line Items -->
                        <div class="bg-gray-50 p-6 rounded-xl shadow-sm">
                            <div class="flex justify-between items-center mb-4">
                                <h3 class="text-lg font-semibold text-dark">Line Items</h3>
                                <button type="button" id="addItemBtn" class="text-primary font-medium"><i class="fas fa-plus mr-1"></i> Add Item</button>
                            </div>
                            <div class="overflow-x-auto">
                                <table class="min-w-full">
                                    <thead class="bg-gray-100">
                                        <tr>
                                            <th class="px-4 py-3 text-left text-xs">Description</th>
                                            <th class="px-4 py-3 text-left text-xs">Qty</th>
                                            <th class="px-4 py-3 text-left text-xs">Rate</th>
                                            <th class="px-4 py-3 text-left text-xs">Amount</th>
                                            <th class="px-4 py-3 text-left text-xs">Actions</th>
                                        </tr>
                                    </thead>
                                    <tbody id="itemsTableBody">
                                        <!-- Items will be added here by JS -->
                                    </tbody>
                                </table>
                            </div>
                            <!-- Totals -->
                            <div class="mt-6 text-right space-y-2">
                                <p>Subtotal: <span id="subtotal">$0.00</span></p>
                                <p>Tax 10%: <span id="tax">$0.00</span></p>
                                <p class="text-xl font-bold">Total: <span id="total">$0.00</span></p>
                            </div>
                        </div>
                    </form>
                </div>

                <!-- Preview -->
                <div class="lg:col-span-1">
                    <div class="bg-white p-6 rounded-xl shadow-lg sticky top-24">
                        <h3 class="font-bold text-lg mb-4">Preview</h3>
                        <div id="invoicePreview" class="text-sm">
                            Invoice will appear here
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

<script>
const { jsPDF } = window.jspdf;
let itemCount = 0;

// Add first item on load
document.addEventListener('DOMContentLoaded', () => {
    addItem();
    updateTotals();
});

document.getElementById('addItemBtn').addEventListener('click', addItem);
document.getElementById('downloadPdfBtn').addEventListener('click', downloadPDF);

function addItem() {
    itemCount++;
    const tbody = document.getElementById('itemsTableBody');
    const row = `
    <tr class="item-row" data-id="${itemCount}">
        <td class="px-4 py-3"><input type="text" class="desc w-full px-2 py-1 border rounded" placeholder="Service"></td>
        <td class="px-4 py-3"><input type="number" class="qty w-16 px-2 py-1 border rounded text-center" value="1"></td>
        <td class="px-4 py-3"><input type="number" class="rate w-24 px-2 py-1 border rounded text-right" value="0"></td>
        <td class="px-4 py-3 text-right font-medium"><span class="amount">$0.00</span></td>
        <td class="px-4 py-3 text-center"><button type="button" class="removeBtn text-red-500"><i class="fas fa-trash"></i></button></td>
    </tr>`;
    tbody.insertAdjacentHTML('beforeend', row);
    
    // Add listeners
    tbody.lastElementChild.querySelectorAll('input').forEach(input => {
        input.addEventListener('input', updateTotals);
    });
    tbody.lastElementChild.querySelector('.removeBtn').addEventListener('click', (e) => {
        e.target.closest('tr').remove();
        updateTotals();
    });
}

function updateTotals() {
    let subtotal = 0;
    document.querySelectorAll('#itemsTableBody tr').forEach(row => {
        const qty = parseFloat(row.querySelector('.qty').value) || 0;
        const rate = parseFloat(row.querySelector('.rate').value) || 0;
        const amount = qty * rate;
        row.querySelector('.amount').innerText = `$${amount.toFixed(2)}`;
        subtotal += amount;
    });
    const tax = subtotal * 0.10;
    const total = subtotal + tax;
    
    document.getElementById('subtotal').innerText = `$${subtotal.toFixed(2)}`;
    document.getElementById('tax').innerText = `$${tax.toFixed(2)}`;
    document.getElementById('total').innerText = `$${total.toFixed(2)}`;
}

function downloadPDF() {
    const doc = new jsPDF();
    doc.setFontSize(20);
    doc.text("INVOICE", 105, 20, {align: "center"});
    doc.setFontSize(12);
    doc.text(`From: ${document.getElementById('fromName').value}`, 20, 40);
    doc.text(`To: ${document.getElementById('toName').value}`, 20, 50);
    doc.text(`Total: ${document.getElementById('total').innerText}`, 20, 70);
    doc.save("invoice.pdf");
}
</script>
</body>
</html>
