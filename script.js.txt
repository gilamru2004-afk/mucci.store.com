const STORAGE_KEY = 'shop-accounting-data';
const shopNameElement = document.getElementById('shopName');
const shopStickerElement = document.getElementById('shopSticker');
const shopStickerInput = document.getElementById('shopStickerInput');
const settingsButton = document.getElementById('settingsButton');
const settingsPage = document.getElementById('settingsPage');
const dashboardPage = document.getElementById('dashboardPage');
const warehousePage = document.getElementById('warehousePage');
const storePage = document.getElementById('storePage');
const expensesPage = document.getElementById('expensesPage');
const debtsPage = document.getElementById('debtsPage');
const debtForm = document.getElementById('debtForm');
const debtNameInput = document.getElementById('debtNameInput');
const debtPhoneInput = document.getElementById('debtPhoneInput');
const debtAmountInput = document.getElementById('debtAmountInput');
const debtAmountFormatted = document.getElementById('debtAmountFormatted');
const debtPeriodInput = document.getElementById('debtPeriodInput');
const debtPeriodUnit = document.getElementById('debtPeriodUnit');
const debtDueDatePreview = document.getElementById('debtDueDatePreview');
const debtsList = document.getElementById('debtsList');
const debtSearchInput = document.getElementById('debtSearchInput');
const overdueDebtsOnlyInput = document.getElementById('overdueDebtsOnlyInput');
const backupReminder = document.getElementById('backupReminder');
const backupReminderText = document.getElementById('backupReminderText');
const backupReminderButton = document.getElementById('backupReminderButton');
const salePaymentMethod = document.getElementById('salePaymentMethod');
const saleCreditFields = document.getElementById('saleCreditFields');
const saleCustomerName = document.getElementById('saleCustomerName');
const saleCustomerPhone = document.getElementById('saleCustomerPhone');
const saleCreditPeriod = document.getElementById('saleCreditPeriod');
const saleCreditPeriodUnit = document.getElementById('saleCreditPeriodUnit');
const saleDueDatePreview = document.getElementById('saleDueDatePreview');
const expenseForm = document.getElementById('expenseForm');
const expenseReasonInput = document.getElementById('expenseReasonInput');
const expenseAmountInput = document.getElementById('expenseAmountInput');
const expenseAmountFormatted = document.getElementById('expenseAmountFormatted');
const expensePlaceInput = document.getElementById('expensePlaceInput');
const expensesList = document.getElementById('expensesList');
const todayExpensesTotal = document.getElementById('todayExpensesTotal');
const saleForm = document.getElementById('saleForm');
const saleProductSearchInput = document.getElementById('saleProductSearchInput');
const saleProductSuggestions = document.getElementById('saleProductSuggestions');
const saleCategoryInput = document.getElementById('saleCategoryInput');
const saleProductInput = document.getElementById('saleProductInput');
const addToCartButton = document.getElementById('addToCartButton');
const clearCartButton = document.getElementById('clearCartButton');
const checkoutButton = document.getElementById('checkoutButton');
const saleCartList = document.getElementById('saleCartList');
const receiptDialog = document.getElementById('receiptDialog');
const receiptSticker = document.getElementById('receiptSticker');
const receiptShopName = document.getElementById('receiptShopName');
const receiptDate = document.getElementById('receiptDate');
const receiptNumber = document.getElementById('receiptNumber');
const receiptItems = document.getElementById('receiptItems');
const receiptTotal = document.getElementById('receiptTotal');
const receiptPayment = document.getElementById('receiptPayment');
const closeReceiptButton = document.getElementById('closeReceiptButton');
const printReceiptButton = document.getElementById('printReceiptButton');
const saleQuantityInput = document.getElementById('saleQuantityInput');
const salePriceInput = document.getElementById('salePriceInput');
const salePriceFormatted = document.getElementById('salePriceFormatted');
const saleCostHint = document.getElementById('saleCostHint');
const saleTotal = document.getElementById('saleTotal');
const transferForm = document.getElementById('transferForm');
const transferProductInput = document.getElementById('transferProductInput');
const transferQuantityInput = document.getElementById('transferQuantityInput');
const storeProductsList = document.getElementById('storeProductsList');
const storeSearchInput = document.getElementById('storeSearchInput');
const storeSearchSuggestions = document.getElementById('storeSearchSuggestions');
const warehouseSearchInput = document.getElementById('warehouseSearchInput');
const warehouseSearchSuggestions = document.getElementById('warehouseSearchSuggestions');
const salesHistoryList = document.getElementById('salesHistoryList');
const productForm = document.getElementById('productForm');
const productNameInput = document.getElementById('productNameInput');
const productCategoryInput = document.getElementById('productCategoryInput');
const productModelInput = document.getElementById('productModelInput');
const productBarcodeInput = document.getElementById('productBarcodeInput');
const productColorInput = document.getElementById('productColorInput');
const productSizeInput = document.getElementById('productSizeInput');
const productQuantityInput = document.getElementById('productQuantityInput');
const productPriceInput = document.getElementById('productPriceInput');
const productCostPriceInput = document.getElementById('productCostPriceInput');
const warehouseProductsList = document.getElementById('warehouseProductsList');
const warehouseQuantityCount = document.getElementById('warehouseQuantityCount');
const warehouseValueCount = document.getElementById('warehouseValueCount');
const editShopNameButton = document.getElementById('editShopNameButton');
const settingsForm = document.getElementById('settingsForm');
const shopNameInput = document.getElementById('shopNameInput');
const cancelSettings = document.getElementById('cancelSettings');
const lowStockForm = document.getElementById('lowStockForm');
const editLowStockButton = document.getElementById('editLowStockButton');
const cancelLowStock = document.getElementById('cancelLowStock');
const currentStockThreshold = document.getElementById('currentStockThreshold');
const recentProductsList = document.getElementById('recentProductsList');
const productCount = document.getElementById('productCount');
const profitLossValue = document.getElementById('profitLossValue');
const outstandingDebtTotal = document.getElementById('outstandingDebtTotal');
const outstandingDebtCount = document.getElementById('outstandingDebtCount');
const lowStockThresholdInput = document.getElementById('lowStockThresholdInput');
const exportDataButton = document.getElementById('exportDataButton');
const importDataInput = document.getElementById('importDataInput');
const backgroundColorInput = document.getElementById('backgroundColorInput');
const darkModeInput = document.getElementById('darkModeInput');
const backgroundThemes = ['lavender', 'blue', 'mint', 'peach', 'rose'];
const currentTimeElement = document.getElementById('currentTime');
const currentDateElement = document.getElementById('currentDate');
const todaySalesTotal = document.getElementById('todaySalesTotal');
const reportPeriodInput = document.getElementById('reportPeriodInput');
const reportPeriodLabel = document.getElementById('reportPeriodLabel');
const reportSalesTotal = document.getElementById('reportSalesTotal');
const reportCashTotal = document.getElementById('reportCashTotal');
const reportCardTotal = document.getElementById('reportCardTotal');
const reportCreditTotal = document.getElementById('reportCreditTotal');
const reportDebtPaymentsTotal = document.getElementById('reportDebtPaymentsTotal');
const reportExpensesTotal = document.getElementById('reportExpensesTotal');
const reportNetTotal = document.getElementById('reportNetTotal');
const BACKUP_DATE_KEY = 'shop-accounting-last-backup';

function createRecordId(prefix) {
  return `${prefix}-${Date.now()}-${Math.random().toString(36).slice(2, 10)}`;
}

function updateDateTime() {
  const now = new Date();
  currentTimeElement.textContent = new Intl.DateTimeFormat('uz-UZ', {
    hour: '2-digit', minute: '2-digit', second: '2-digit'
  }).format(now);
  currentDateElement.textContent = new Intl.DateTimeFormat('uz-UZ', {
    weekday: 'long', day: 'numeric', month: 'long', year: 'numeric'
  }).format(now);
}

updateDateTime();
setInterval(updateDateTime, 1000);

function loadSavedData() {
  try {
    const saved = JSON.parse(localStorage.getItem(STORAGE_KEY));
    return saved && typeof saved === 'object' ? saved : {};
  } catch (error) {
    return {};
  }
}

let savedData = loadSavedData();
let shopName = typeof savedData.shopName === 'string' && savedData.shopName.trim()
  ? savedData.shopName
  : 'Mening do‘konim';
let shopSticker = typeof savedData.shopSticker === 'string' ? savedData.shopSticker : '';
let products = Array.isArray(savedData.products) ? savedData.products : [];
let saleCart = [];
products.forEach(product => {
  if (!product.id) product.id = createRecordId('product');
  if (!Number.isFinite(Number(product.storeQuantity))) product.storeQuantity = 0;
});
let sales = Array.isArray(savedData.sales) ? savedData.sales : [];
let expenses = Array.isArray(savedData.expenses) ? savedData.expenses : [];
let debts = Array.isArray(savedData.debts) ? savedData.debts : [];
let lowStockThreshold = Number.isInteger(savedData.lowStockThreshold) && savedData.lowStockThreshold >= 0
  ? savedData.lowStockThreshold
  : 5;
let backgroundTheme = backgroundThemes.includes(savedData.backgroundTheme) ? savedData.backgroundTheme : 'lavender';
let darkMode = savedData.darkMode === true;
shopNameElement.textContent = shopName;
shopStickerElement.textContent = shopSticker;
lowStockThresholdInput.value = lowStockThreshold;
currentStockThreshold.textContent = `${lowStockThreshold} dona`;
backgroundColorInput.value = backgroundTheme;
darkModeInput.checked = darkMode;
document.body.dataset.theme = backgroundTheme;
document.body.classList.toggle('dark-mode', darkMode);

function saveData() {
  savedData = { ...savedData, shopName, shopSticker, products, sales, expenses, debts, lowStockThreshold, backgroundTheme, darkMode };
  try {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(savedData));
  } catch (error) {
    // Sahifa ishlashda davom etadi, lekin ma’lumotlar saqlanmasligi mumkin.
  }
}

function updateBackupReminder() {
  let lastBackup = '';
  try {
    lastBackup = localStorage.getItem(BACKUP_DATE_KEY) || '';
  } catch (error) {
    backupReminder.hidden = false;
    backupReminderText.textContent = 'Ma’lumotlar brauzerda saqlanadi. Muhim yozuvlarni yo‘qotmaslik uchun zaxira faylini yuklab oling.';
    return;
  }

  const backupTime = Date.parse(lastBackup);
  const reminderNeeded = !Number.isFinite(backupTime) || Date.now() - backupTime > 30 * 24 * 60 * 60 * 1000;
  backupReminder.hidden = !reminderNeeded;
  backupReminderText.textContent = Number.isFinite(backupTime)
    ? 'Oxirgi zaxiradan 30 kundan oshdi. Ma’lumotlar faqat shu brauzerda saqlanadi.'
    : 'Zaxira nusxasi hali yuklab olinmagan. Ma’lumotlar faqat shu brauzerda saqlanadi.';
}

updateBackupReminder();

function renderProductList(list, items, emptyText = 'Hozircha tovar qo‘shilmagan.', allowDelete = false) {
  list.replaceChildren();

  if (items.length === 0) {
    const emptyMessage = document.createElement('li');
    emptyMessage.className = 'product-empty';
    emptyMessage.textContent = emptyText;
    list.append(emptyMessage);
    return;
  }

  items.forEach(product => {
    const item = document.createElement('li');
    item.className = 'product-item';
    const name = document.createElement('strong');
    name.textContent = product.name;
    const details = document.createElement('span');
    const sellingPrice = formatMoney(product.price);
    const costPrice = product.costPrice == null
      ? 'Tannarx kiritilmagan'
      : `${formatMoney(product.costPrice)} so‘m`;
    const category = product.category || 'Kategoriya ko‘rsatilmagan';
    const attributes = [
      product.model && `Rusumi: ${product.model}`,
      product.barcode && `Shtrix-kod: ${product.barcode}`,
      product.color && `Rangi: ${product.color}`,
      product.size && `O‘lchami: ${product.size}`
    ].filter(Boolean);
    details.textContent = [
      category,
      ...attributes,
      `${Number(product.quantity).toLocaleString('uz-UZ')} dona`,
      `Sotiladigan narx: ${sellingPrice} so‘m`,
      `Tannarx: ${costPrice}`
    ].join(' · ');
    item.append(name, details);
    if (Number(product.quantity) <= lowStockThreshold) {
      const warning = document.createElement('span');
      warning.className = 'stock-warning';
      warning.textContent = '⚠️ Kam qolgan tovar';
      item.append(warning);
    }
    if (allowDelete) {
      const deleteButton = document.createElement('button');
      deleteButton.className = 'delete-button product-delete-button';
      deleteButton.type = 'button';
      deleteButton.dataset.deleteProductIndex = String(products.indexOf(product));
      deleteButton.textContent = 'O‘chirish';
      item.append(deleteButton);
    }
    list.append(item);
  });
}

function populateSaleCategories() {
  const previousValue = saleCategoryInput.value;
  const categories = [...new Set(products
    .filter(product => Number(product.storeQuantity || 0) > 0)
    .map(product => (product.category || 'Kategoriya ko‘rsatilmagan').trim()))]
    .sort((first, second) => first.localeCompare(second, 'uz'));

  saleCategoryInput.replaceChildren();
  const allCategories = document.createElement('option');
  allCategories.value = '';
  allCategories.textContent = 'Barcha kategoriyalar';
  saleCategoryInput.append(allCategories);
  categories.forEach(category => {
    const option = document.createElement('option');
    option.value = category;
    option.textContent = category;
    saleCategoryInput.append(option);
  });

  if (categories.includes(previousValue)) saleCategoryInput.value = previousValue;
}

function populateProductSelect(select, stockField, selectedCategory = '', query = '') {
  const previousValue = select.value;
  select.replaceChildren();
  const placeholder = document.createElement('option');
  placeholder.value = '';
  placeholder.textContent = 'Tovarni tanlang';
  select.append(placeholder);

  products.forEach((product, index) => {
    const quantity = Number(product[stockField] || 0);
    const category = (product.category || 'Kategoriya ko‘rsatilmagan').trim();
    if (quantity <= 0 || (selectedCategory && category !== selectedCategory) ||
      (query && !matchesProductSearch(product, query))) return;
    const option = document.createElement('option');
    option.value = String(index);
    option.textContent = `${product.name} — ${quantity} dona`;
    select.append(option);
  });

  if ([...select.options].some(option => option.value === previousValue)) {
    select.value = previousValue;
  }
}

function matchesProductSearch(product, query) {
  const searchableText = [product.name, product.category, product.model, product.barcode, product.color, product.size]
    .filter(Boolean)
    .join(' ')
    .toLocaleLowerCase('uz-UZ');
  return searchableText.includes(query.trim().toLocaleLowerCase('uz-UZ'));
}

function populateSearchSuggestions(datalist, items, stockField) {
  datalist.replaceChildren();
  items.forEach(product => {
    const option = document.createElement('option');
    option.value = product.name;
    option.label = `${product.barcode ? `Shtrix-kod: ${product.barcode}` : (product.category || 'Kategoriya ko‘rsatilmagan')} · ${Number(product[stockField] || 0)} dona`;
    datalist.append(option);
  });
}

function renderInventoryLists() {
  const storeProducts = products.filter(product => Number(product.storeQuantity || 0) > 0);
  const matchingStoreProducts = storeProducts.filter(product => matchesProductSearch(product, storeSearchInput.value));
  const storeEmptyText = storeProducts.length === 0
    ? 'Do‘konga hali tovar o‘tkazilmagan.'
    : 'Qidiruv bo‘yicha tovar topilmadi.';
  renderProductList(storeProductsList, matchingStoreProducts.map(product => ({
    ...product,
    quantity: product.storeQuantity
  })), storeEmptyText);

  const matchingWarehouseProducts = [...products].reverse()
    .filter(product => matchesProductSearch(product, warehouseSearchInput.value));
  const warehouseEmptyText = products.length === 0
    ? 'Hozircha tovar qo‘shilmagan.'
    : 'Qidiruv bo‘yicha tovar topilmadi.';
  renderProductList(warehouseProductsList, matchingWarehouseProducts, warehouseEmptyText, true);
  populateSearchSuggestions(storeSearchSuggestions, storeProducts, 'storeQuantity');
  populateSearchSuggestions(warehouseSearchSuggestions, products, 'quantity');
}

function getSaleCartTotal() {
  return saleCart.reduce((total, item) => total + Number(item.quantity || 0) * Number(item.price || 0), 0);
}

function renderSaleCart() {
  saleCartList.replaceChildren();
  if (saleCart.length === 0) {
    const empty = document.createElement('li');
    empty.className = 'product-empty';
    empty.textContent = 'Savat hozircha bo‘sh.';
    saleCartList.append(empty);
  } else {
    saleCart.forEach((cartItem, index) => {
      const row = document.createElement('li');
      row.className = 'product-item cart-item';
      const copy = document.createElement('div');
      copy.className = 'cart-item-copy';
      const name = document.createElement('strong');
      name.textContent = cartItem.name;
      const details = document.createElement('span');
      details.textContent = `${cartItem.quantity} dona × ${formatMoney(cartItem.price)} so‘m = ${formatMoney(cartItem.quantity * cartItem.price)} so‘m`;
      copy.append(name, details);
      const remove = document.createElement('button');
      remove.className = 'delete-button';
      remove.type = 'button';
      remove.dataset.removeCartIndex = String(index);
      remove.textContent = 'Olib tashlash';
      row.append(copy, remove);
      saleCartList.append(row);
    });
  }
  saleTotal.textContent = `Savat jami: ${formatMoney(getSaleCartTotal())} so‘m`;
  checkoutButton.disabled = saleCart.length === 0;
  clearCartButton.disabled = saleCart.length === 0;
}

function renderStore() {
  renderInventoryLists();

  salesHistoryList.replaceChildren();
  if (sales.length === 0) {
    const emptyMessage = document.createElement('li');
    emptyMessage.className = 'product-empty';
    emptyMessage.textContent = 'Hozircha sotuv yo‘q.';
    salesHistoryList.append(emptyMessage);
  } else {
    sales.slice(-10).reverse().forEach((sale, reversedIndex) => {
      const saleIndex = sales.length - 1 - reversedIndex;
      const item = document.createElement('li');
      item.className = 'product-item';
      const name = document.createElement('strong');
      name.textContent = sale.name;
      const details = document.createElement('span');
      const paymentLabel = { cash: 'Naqd', card: 'Karta', credit: 'Nasiya' }[sale.paymentMethod] || 'Naqd';
      const customerDetails = sale.paymentMethod === 'credit'
        ? ` · Mijoz: ${sale.customerName || '—'} · Tel: ${sale.customerPhone || '—'} · Muddat: ${sale.dueDate || '—'}`
        : '';
      const saleDate = new Date(sale.date);
      const saleDateText = Number.isNaN(saleDate.getTime()) ? (sale.date || '') : saleDate.toLocaleString('uz-UZ');
      details.textContent = `${sale.quantity} dona · ${formatMoney(sale.price)} so‘m/dona · Jami: ${formatMoney(sale.total)} so‘m · To‘lov: ${paymentLabel}${customerDetails} · ${saleDateText}`;
      const cancelButton = document.createElement('button');
      cancelButton.className = 'delete-button';
      cancelButton.type = 'button';
      cancelButton.dataset.cancelSaleIndex = String(saleIndex);
      cancelButton.textContent = 'Bekor qilish / qaytarish';
      item.append(name, details, cancelButton);
      salesHistoryList.append(item);
    });
  }

  populateSaleCategories();
  populateProductSelect(saleProductInput, 'storeQuantity', saleCategoryInput.value, saleProductSearchInput.value);
  populateSearchSuggestions(saleProductSuggestions, products.filter(product => Number(product.storeQuantity || 0) > 0), 'storeQuantity');
  populateProductSelect(transferProductInput, 'quantity');
  renderSaleCart();
}

salesHistoryList.addEventListener('click', event => {
  const button = event.target.closest('[data-cancel-sale-index]');
  if (!button) return;
  const saleIndex = Number(button.dataset.cancelSaleIndex);
  const sale = sales[saleIndex];
  if (!sale) return;

  let product = sale.productId
    ? products.find(item => item.id === sale.productId)
    : null;
  if (!product) {
    const matchingProducts = products.filter(item => item.name === sale.name);
    if (matchingProducts.length === 1) product = matchingProducts[0];
  }
  if (!product) {
    window.alert('Sotuvga tegishli tovar omborda topilmadi. Qoldiqni xavfsiz tiklab bo‘lmadi.');
    return;
  }

  let debtIndex = debts.findIndex(debt => sale.saleId && debt.saleId === sale.saleId);
  if (sale.paymentMethod === 'credit' && debtIndex < 0) {
    const saleAmount = Number(sale.total ?? Number(sale.quantity || 0) * Number(sale.price || 0));
    const possibleDebts = debts.map((debt, index) => ({ debt, index })).filter(({ debt }) =>
      debt.saleName === sale.name && debt.name === sale.customerName && debt.phone === sale.customerPhone &&
      Number(debt.amount) === saleAmount && debt.dueDate === sale.dueDate
    );
    if (possibleDebts.length === 1) debtIndex = possibleDebts[0].index;
    else {
      window.alert('Bu nasiya sotuviga mos qarz aniq topilmadi. Avval qarz yozuvini tekshiring.');
      return;
    }
  }

  if (debtIndex >= 0 && getDebtPaidAmount(debts[debtIndex]) > 0) {
    window.alert('Bu nasiya qarziga to‘lov qilingan. Avval to‘lovlarni hisobga olib, qarzni alohida to‘g‘rilang.');
    return;
  }

  if (!window.confirm(`“${sale.name}” (${sale.quantity} dona) sotuvini bekor qilib, tovarni do‘kon qoldig‘iga qaytarasizmi? Hisobotdan ham chiqariladi.`)) return;
  product.storeQuantity = Number(product.storeQuantity || 0) + Number(sale.quantity || 0);
  sales.splice(saleIndex, 1);
  if (debtIndex >= 0) debts.splice(debtIndex, 1);
  renderProducts();
  saveData();
});

function updateProfitLoss() {
  const netProfit = sales.reduce((total, sale) => {
    const quantity = Number(sale.quantity);
    const price = Number(sale.price);
    const savedCost = Number(sale.costPrice);
    const oldProduct = products.find(product => product.name === sale.name);
    const costPrice = Number.isFinite(savedCost)
      ? savedCost
      : Number(oldProduct && oldProduct.costPrice);

    if (!Number.isFinite(quantity) || !Number.isFinite(price) || !Number.isFinite(costPrice)) return total;
    return total + quantity * (price - costPrice);
  }, 0);

  profitLossValue.textContent = `${netProfit < 0 ? 'Zarar' : 'Foyda'}: ${formatMoney(Math.abs(netProfit))} so‘m`;
  profitLossValue.classList.toggle('profit-negative', netProfit < 0);
  profitLossValue.classList.toggle('profit-positive', netProfit >= 0);
}

function localDateKey(date) {
  const year = date.getFullYear();
  const month = String(date.getMonth() + 1).padStart(2, '0');
  const day = String(date.getDate()).padStart(2, '0');
  return `${year}-${month}-${day}`;
}

function getSaleDateKey(sale) {
  if (typeof sale.dateKey === 'string' && /^\d{4}-\d{2}-\d{2}$/.test(sale.dateKey)) {
    return sale.dateKey;
  }
  if (typeof sale.date === 'string') {
    const localizedDate = sale.date.match(/^(\d{1,2})[./](\d{1,2})[./](\d{4})/);
    if (localizedDate) {
      return `${localizedDate[3]}-${localizedDate[2].padStart(2, '0')}-${localizedDate[1].padStart(2, '0')}`;
    }
    const parsedDate = new Date(sale.date);
    if (!Number.isNaN(parsedDate.getTime())) return localDateKey(parsedDate);
  }
  return '';
}

function getDebtPaidAmount(debt) {
  if (Array.isArray(debt.payments)) {
    return debt.payments.reduce((total, payment) => total + (Number(payment.amount) || 0), 0);
  }
  if (Number.isFinite(Number(debt.paidAmount))) return Number(debt.paidAmount);
  return debt.paid ? Number(debt.amount) || 0 : 0;
}

function getDebtRemaining(debt) {
  return Math.max(0, (Number(debt.amount) || 0) - getDebtPaidAmount(debt));
}

function isDebtOverdue(debt) {
  return getDebtRemaining(debt) > 0 && typeof debt.dueDate === 'string' &&
    /^\d{4}-\d{2}-\d{2}$/.test(debt.dueDate) && debt.dueDate < localDateKey(new Date());
}

function getRecordDateKey(value) {
  if (typeof value !== 'string' || !value) return '';
  const parsed = new Date(value);
  return Number.isNaN(parsed.getTime()) ? '' : localDateKey(parsed);
}

function renderStatisticsReport() {
  const now = new Date();
  const todayKey = localDateKey(now);
  const monthKey = todayKey.slice(0, 7);
  const isMonthly = reportPeriodInput.value === 'month';
  const includesDate = key => key && (isMonthly ? key.startsWith(monthKey) : key === todayKey);
  const periodSales = sales.filter(sale => includesDate(getSaleDateKey(sale)));
  const totals = periodSales.reduce((result, sale) => {
    const amount = Number(sale.total ?? Number(sale.quantity || 0) * Number(sale.price || 0));
    if (Number.isFinite(amount)) {
      result.sales += amount;
      if (sale.paymentMethod === 'card') result.card += amount;
      else if (sale.paymentMethod === 'credit') result.credit += amount;
      else result.cash += amount;
    }
    return result;
  }, { sales: 0, cash: 0, card: 0, credit: 0 });
  const expenseTotal = expenses.reduce((total, expense) =>
    includesDate(getRecordDateKey(expense.date)) ? total + (Number(expense.amount) || 0) : total, 0);
  const debtPaymentsTotal = debts.reduce((total, debt) => {
    const payments = Array.isArray(debt.payments) ? debt.payments : [];
    return total + payments.reduce((sum, payment) =>
      includesDate(getRecordDateKey(payment.date)) ? sum + (Number(payment.amount) || 0) : sum, 0);
  }, 0);

  reportPeriodLabel.textContent = isMonthly
    ? `Hisobot davri: ${now.toLocaleDateString('uz-UZ', { month: 'long', year: 'numeric' })}`
    : `Hisobot sanasi: ${now.toLocaleDateString('uz-UZ')}`;
  reportSalesTotal.textContent = `${formatMoney(totals.sales)} so‘m`;
  reportCashTotal.textContent = `${formatMoney(totals.cash)} so‘m`;
  reportCardTotal.textContent = `${formatMoney(totals.card)} so‘m`;
  reportCreditTotal.textContent = `${formatMoney(totals.credit)} so‘m`;
  reportDebtPaymentsTotal.textContent = `${formatMoney(debtPaymentsTotal)} so‘m`;
  reportExpensesTotal.textContent = `${formatMoney(expenseTotal)} so‘m`;
  reportNetTotal.textContent = `${formatMoney(totals.sales - expenseTotal)} so‘m`;
}

reportPeriodInput.addEventListener('change', renderStatisticsReport);

function calculateDueDate(period, unit, startDate = new Date()) {
  const dueDate = new Date(startDate);
  const amount = Number(period);
  if (unit === 'months') {
    const originalDay = dueDate.getDate();
    dueDate.setDate(1);
    dueDate.setMonth(dueDate.getMonth() + amount);
    const lastDay = new Date(dueDate.getFullYear(), dueDate.getMonth() + 1, 0).getDate();
    dueDate.setDate(Math.min(originalDay, lastDay));
  } else {
    dueDate.setDate(dueDate.getDate() + amount);
  }
  return localDateKey(dueDate);
}

function updateDueDatePreview(element, period, unit) {
  const amount = Number(period.value);
  if (!Number.isInteger(amount) || amount < 1) {
    element.textContent = 'Qaytarish sanasi: —';
    return;
  }
  const dueDate = new Date(`${calculateDueDate(amount, unit.value)}T00:00:00`);
  element.textContent = `Qaytarish sanasi: ${dueDate.toLocaleDateString('uz-UZ')}`;
}

debtPeriodInput.addEventListener('input', () => updateDueDatePreview(debtDueDatePreview, debtPeriodInput, debtPeriodUnit));
debtPeriodUnit.addEventListener('change', () => updateDueDatePreview(debtDueDatePreview, debtPeriodInput, debtPeriodUnit));
saleCreditPeriod.addEventListener('input', () => updateDueDatePreview(saleDueDatePreview, saleCreditPeriod, saleCreditPeriodUnit));
saleCreditPeriodUnit.addEventListener('change', () => updateDueDatePreview(saleDueDatePreview, saleCreditPeriod, saleCreditPeriodUnit));
updateDueDatePreview(debtDueDatePreview, debtPeriodInput, debtPeriodUnit);
updateDueDatePreview(saleDueDatePreview, saleCreditPeriod, saleCreditPeriodUnit);

function renderExpenses() {
  const todayKey = localDateKey(new Date());
  const todayTotal = expenses.reduce((total, expense) => {
    const date = new Date(expense.date);
    return !Number.isNaN(date.getTime()) && localDateKey(date) === todayKey
      ? total + Number(expense.amount || 0)
      : total;
  }, 0);
  todayExpensesTotal.textContent = `${formatMoney(todayTotal)} so‘m`;
  renderStatisticsReport();

  expensesList.replaceChildren();
  if (expenses.length === 0) {
    const emptyMessage = document.createElement('li');
    emptyMessage.className = 'product-empty';
    emptyMessage.textContent = 'Hozircha xarajat yo‘q.';
    expensesList.append(emptyMessage);
    return;
  }

  [...expenses].reverse().forEach(expense => {
    const item = document.createElement('li');
    item.className = 'product-item';
    const reason = document.createElement('strong');
    reason.textContent = expense.reason;
    const details = document.createElement('span');
    const date = new Date(expense.date);
    const dateText = Number.isNaN(date.getTime()) ? '' : date.toLocaleString('uz-UZ');
    details.textContent = `Qayerga: ${expense.place} · Miqdori: ${formatMoney(expense.amount)} so‘m${dateText ? ` · ${dateText}` : ''}`;
    item.append(reason, details);
    expensesList.append(item);
  });
}

function renderDebts() {
  const unpaidDebts = debts.filter(debt => getDebtRemaining(debt) > 0);
  const unpaidTotal = unpaidDebts.reduce((total, debt) => total + getDebtRemaining(debt), 0);
  outstandingDebtTotal.textContent = `${formatMoney(unpaidTotal)} so‘m`;
  outstandingDebtCount.textContent = `${unpaidDebts.length} ta qarz`;

  debtsList.replaceChildren();
  const query = debtSearchInput.value.trim().toLocaleLowerCase('uz-UZ');
  const overdueOnly = overdueDebtsOnlyInput.checked;
  const filteredDebts = debts.map((debt, index) => ({ debt, index })).filter(({ debt }) => {
    const searchable = `${debt.name || ''} ${debt.phone || ''}`.toLocaleLowerCase('uz-UZ');
    return searchable.includes(query) && (!overdueOnly || isDebtOverdue(debt));
  });
  if (filteredDebts.length === 0) {
    const emptyMessage = document.createElement('li');
    emptyMessage.className = 'product-empty';
    emptyMessage.textContent = debts.length === 0 ? 'Hozircha qarz yo‘q.' : 'Tanlangan qidiruv bo‘yicha qarz topilmadi.';
    debtsList.append(emptyMessage);
    return;
  }

  filteredDebts.reverse().forEach(({ debt, index: debtIndex }) => {
    const item = document.createElement('li');
    item.className = 'product-item debt-item';
    const copy = document.createElement('div');
    copy.className = 'debt-copy';
    const name = document.createElement('strong');
    name.textContent = debt.name || 'Ism ko‘rsatilmagan';
    const details = document.createElement('span');
    const dueDate = debt.dueDate || '';
    const remaining = getDebtRemaining(debt);
    const paidAmount = Math.max(0, (Number(debt.amount) || 0) - remaining);
    const isPaid = remaining <= 0;
    const overdue = isDebtOverdue(debt);
    const sourceText = debt.saleName ? ` · Tovar: ${debt.saleName}` : '';
    const periodText = Number.isInteger(Number(debt.period))
      ? ` (${debt.period} ${debt.periodUnit === 'months' ? 'oy' : 'kun'})`
      : '';
    details.textContent = `Telefon: ${debt.phone || 'Ko‘rsatilmagan'} · Jami: ${formatMoney(debt.amount)} so‘m · To‘langan: ${formatMoney(paidAmount)} so‘m · Qoldiq: ${formatMoney(remaining)} so‘m · Muddat: ${dueDate || 'Ko‘rsatilmagan'}${periodText}${sourceText}`;
    copy.append(name, details);
    const status = document.createElement('span');
    status.className = isPaid ? 'debt-status debt-paid' : overdue ? 'debt-status stock-warning' : 'debt-status';
    status.textContent = isPaid ? 'To‘langan' : overdue ? 'Muddati o‘tgan' : paidAmount > 0 ? 'Qisman to‘langan' : 'To‘lanmagan';
    item.append(copy, status);
    if (!isPaid) {
      const paymentButton = document.createElement('button');
      paymentButton.className = 'secondary-button debt-paid-button';
      paymentButton.type = 'button';
      paymentButton.dataset.debtPaymentIndex = String(debtIndex);
      paymentButton.textContent = 'To‘lov kiritish';
      item.append(paymentButton);
    }
    debtsList.append(item);
  });
}

debtSearchInput.addEventListener('input', renderDebts);
overdueDebtsOnlyInput.addEventListener('change', renderDebts);

debtsList.addEventListener('click', event => {
  const button = event.target.closest('[data-debt-payment-index]');
  if (!button) return;
  const debt = debts[Number(button.dataset.debtPaymentIndex)];
  if (!debt) return;
  const remaining = getDebtRemaining(debt);
  const enteredAmount = window.prompt(`To‘lov miqdorini kiriting. Qolgan qarz: ${formatMoney(remaining)} so‘m`);
  if (enteredAmount === null) return;
  const amount = Number(enteredAmount.replace(/\D/g, ''));
  if (!Number.isInteger(amount) || amount < 1 || amount > remaining) {
    window.alert(`To‘lov 1 so‘mdan kam va qolgan qarzdan ko‘p bo‘lmasligi kerak (${formatMoney(remaining)} so‘m).`);
    return;
  }
  debt.payments = Array.isArray(debt.payments) ? debt.payments : [];
  debt.payments.push({ amount, date: new Date().toISOString() });
  debt.paidAmount = getDebtPaidAmount(debt);
  debt.paid = debt.paidAmount >= Number(debt.amount);
  renderDebts();
  renderStatisticsReport();
  saveData();
});

function renderProducts() {
  productCount.textContent = `${products.length} ta`;
  const todayKey = localDateKey(new Date());
  const todaySales = sales.reduce((total, sale) => {
    if (getSaleDateKey(sale) !== todayKey) return total;
    const saleTotal = Number(sale.total ?? (Number(sale.quantity || 0) * Number(sale.price || 0)));
    return total + (Number.isFinite(saleTotal) ? saleTotal : 0);
  }, 0);
  todaySalesTotal.textContent = `${formatMoney(todaySales)} so‘m`;
  updateProfitLoss();
  renderExpenses();
  const totalQuantity = products.reduce((total, product) => total + Number(product.quantity || 0), 0);
  const totalCostValue = products.reduce(
    (total, product) => total + Number(product.quantity || 0) * Number(product.costPrice || 0),
    0
  );
  warehouseQuantityCount.textContent = `${totalQuantity.toLocaleString('uz-UZ')} dona`;
  warehouseValueCount.textContent = `${totalCostValue.toLocaleString('uz-UZ')} so‘m`;
  renderProductList(recentProductsList, products.slice(-5).reverse());
  renderStore();
  renderDebts();
}

renderProducts();

storeSearchInput.addEventListener('input', renderInventoryLists);
warehouseSearchInput.addEventListener('input', renderInventoryLists);

warehouseProductsList.addEventListener('click', event => {
  const button = event.target.closest('[data-delete-product-index]');
  if (!button) return;
  const index = Number(button.dataset.deleteProductIndex);
  const product = products[index];
  if (!product || !window.confirm(`“${product.name}” tovarini ombor va do‘kon qoldig‘idan o‘chirasizmi? Sotuv tarixi va qarzlar saqlanib qoladi.`)) return;
  products.splice(index, 1);
  renderProducts();
  saveData();
});

document.querySelectorAll('[data-clear-section]').forEach(button => {
  button.addEventListener('click', () => {
    const section = button.dataset.clearSection;
    const confirmMessages = {
      products: 'Barcha tovarlarni ombor va do‘kon qoldig‘idan o‘chirasizmi? Sotuv tarixi va qarzlar saqlanib qoladi.',
      'store-stock': 'Do‘kondagi barcha qoldiqni tozalaysizmi? Ombordagi tovarlar va sotuv tarixi saqlanadi.',
      sales: 'Sotuvlar tarixini butunlay o‘chirasizmi? Qarzlar alohida saqlanadi.',
      expenses: 'Barcha xarajat yozuvlarini o‘chirasizmi?',
      debts: 'Qarzlar ro‘yxati o‘chiriladi. Nasiya sotuvlari sotuvlar tarixida saqlanib qoladi. Davom etasizmi?'
    };
    if (!confirmMessages[section] || !window.confirm(confirmMessages[section])) return;

    if (section === 'products') {
      products = [];
      storeSearchInput.value = '';
      warehouseSearchInput.value = '';
    } else if (section === 'store-stock') {
      products.forEach(product => { product.storeQuantity = 0; });
    } else if (section === 'sales') {
      sales = [];
    } else if (section === 'expenses') {
      expenses = [];
    } else if (section === 'debts') {
      debts = [];
    }

    renderProducts();
    saveData();
  });
});

debtAmountInput.addEventListener('input', () => {
  const digits = debtAmountInput.value.replace(/\D/g, '');
  const amount = Number(digits);
  debtAmountInput.value = digits ? formatMoney(amount) : '';
  debtAmountFormatted.textContent = `Ko‘rinishi: ${digits ? formatMoney(amount) : '0'} so‘m`;
});

debtForm.addEventListener('submit', event => {
  event.preventDefault();
  const name = debtNameInput.value.trim();
  const phone = debtPhoneInput.value.trim();
  const amount = Number(debtAmountInput.value.replace(/\D/g, ''));
  const period = Number(debtPeriodInput.value);
  const periodUnit = debtPeriodUnit.value;
  if (!name || !phone || !Number.isInteger(amount) || amount < 1 || !Number.isInteger(period) || period < 1) return;
  const dueDate = calculateDueDate(period, periodUnit);

  debts.push({ name, phone, amount, dueDate, period, periodUnit, createdAt: new Date().toISOString(), paid: false });
  renderDebts();
  saveData();
  debtForm.reset();
  updateDueDatePreview(debtDueDatePreview, debtPeriodInput, debtPeriodUnit);
  debtAmountFormatted.textContent = 'Ko‘rinishi: 0 so‘m';
  debtNameInput.focus();
});

expenseAmountInput.addEventListener('input', () => {
  const digits = expenseAmountInput.value.replace(/\D/g, '');
  const amount = Number(digits);
  expenseAmountInput.value = digits ? formatMoney(amount) : '';
  expenseAmountFormatted.textContent = `Ko‘rinishi: ${digits ? formatMoney(amount) : '0'} so‘m`;
});

expenseForm.addEventListener('submit', event => {
  event.preventDefault();
  const reason = expenseReasonInput.value.trim();
  const amount = Number(expenseAmountInput.value.replace(/\D/g, ''));
  const place = expensePlaceInput.value.trim();
  if (!reason || !place || !Number.isInteger(amount) || amount < 1) return;

  expenses.push({ reason, amount, place, date: new Date().toISOString() });
  renderExpenses();
  saveData();
  expenseForm.reset();
  expenseAmountFormatted.textContent = 'Ko‘rinishi: 0 so‘m';
  expenseReasonInput.focus();
});

settingsButton.addEventListener('click', () => {
  dashboardPage.hidden = true;
  warehousePage.hidden = true;
  storePage.hidden = true;
  expensesPage.hidden = true;
  debtsPage.hidden = true;
  settingsPage.hidden = false;
  settingsForm.hidden = true;
  lowStockForm.hidden = true;
  document.querySelectorAll('.nav-button').forEach(link => link.classList.remove('active'));
});

document.querySelectorAll('.nav-button').forEach(link => {
  link.addEventListener('click', () => {
    const destination = link.getAttribute('href');
    document.querySelectorAll('.nav-button').forEach(item => item.classList.remove('active'));
    link.classList.add('active');
    [dashboardPage, warehousePage, storePage, expensesPage, debtsPage, settingsPage].forEach(page => {
      page.hidden = true;
    });

    if (destination === '#warehouse') {
      warehousePage.hidden = false;
    } else if (destination === '#store') {
      storePage.hidden = false;
    } else if (destination === '#expenses') {
      expensesPage.hidden = false;
      renderExpenses();
    } else if (destination === '#debts') {
      debtsPage.hidden = false;
      renderDebts();
    } else {
      dashboardPage.hidden = false;
      if (destination === '#summary') {
        document.getElementById('statisticsReport').scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    }
  });
});

productForm.addEventListener('submit', event => {
  event.preventDefault();
  const product = {
    id: createRecordId('product'),
    name: productNameInput.value.trim(),
    category: productCategoryInput.value.trim() || 'Boshqa',
    model: productModelInput.value.trim(),
    barcode: productBarcodeInput.value.trim(),
    color: productColorInput.value.trim(),
    size: productSizeInput.value.trim(),
    quantity: Number(productQuantityInput.value),
    price: Number(productPriceInput.value),
    costPrice: Number(productCostPriceInput.value)
  };
  if (!product.name || !product.category || !Number.isFinite(product.quantity) || product.quantity < 1 || !Number.isFinite(product.price) || product.price < 0 || !Number.isFinite(product.costPrice) || product.costPrice < 0) return;
  if (product.barcode && products.some(item => String(item.barcode || '').trim() === product.barcode)) {
    window.alert('Bu shtrix-kod boshqa tovarga biriktirilgan. Kodni tekshiring.');
    return;
  }

  products.push(product);
  renderProducts();
  saveData();
  productForm.reset();
  productNameInput.focus();
});

function formatMoney(value) {
  return new Intl.NumberFormat('uz-UZ', { maximumFractionDigits: 0 }).format(Number(value) || 0);
}

function getExportTables(section) {
  if (section === 'dashboard') {
    return {
      title: 'Dashboard',
      tables: [
        {
          title: 'Do‘kon ko‘rsatkichlari',
          headers: ['Ko‘rsatkich', 'Qiymat'],
          rows: [
            ['Do‘kon nomi', shopName],
            ['Jami tovar turi', `${products.length} ta`],
            ['Bugungi savdo', todaySalesTotal.textContent],
            ['Bugungi xarajat', todayExpensesTotal.textContent],
            ['To‘lanmagan nasiya', `${formatMoney(debts.reduce((total, debt) => total + getDebtRemaining(debt), 0))} so‘m`],
            ['Sotuvlardan foyda / zarar', profitLossValue.textContent]
          ]
        },
        {
          title: 'Oxirgi qo‘shilgan tovarlar',
          headers: ['Tovar', 'Kategoriya', 'Miqdor', 'Tannarx', 'Sotuv narxi'],
          rows: products.slice(-5).reverse().map(product => [
            product.name,
            product.category || 'Kategoriya ko‘rsatilmagan',
            `${Number(product.quantity || 0)} dona`,
            `${formatMoney(product.costPrice)} so‘m`,
            `${formatMoney(product.price)} so‘m`
          ])
        }
      ]
    };
  }

  if (section === 'recent-products') {
    return {
      title: 'Oxirgi qo‘shilgan tovarlar',
      tables: [{
        title: 'Tovarlar jadvali',
        headers: ['Tovar', 'Kategoriya', 'Rusumi', 'Rangi', 'O‘lchami', 'Ombor qoldig‘i', 'Do‘kon qoldig‘i', 'Tannarx/dona', 'Sotuv narxi'],
        rows: products.slice(-5).reverse().map(product => [
          product.name,
          product.category || 'Ko‘rsatilmagan',
          product.model || '—',
          product.color || '—',
          product.size || '—',
          `${Number(product.quantity || 0)} dona`,
          `${Number(product.storeQuantity || 0)} dona`,
          `${formatMoney(product.costPrice)} so‘m`,
          `${formatMoney(product.price)} so‘m`
        ])
      }]
    };
  }

  if (section === 'store-stock') {
    return {
      title: 'Do‘kon qoldig‘i',
      tables: [{
        title: 'Do‘kondagi tovarlar',
        headers: ['№', 'Tovar', 'Kategoriya', 'Rusumi', 'Rangi', 'O‘lchami', 'Qoldiq', 'Sotuv narxi', 'Jami qiymat'],
        rows: products.filter(product => Number(product.storeQuantity || 0) > 0).map((product, index) => [
          index + 1,
          product.name,
          product.category || 'Ko‘rsatilmagan',
          product.model || '—',
          product.color || '—',
          product.size || '—',
          `${Number(product.storeQuantity || 0)} dona`,
          `${formatMoney(product.price)} so‘m`,
          `${formatMoney(Number(product.storeQuantity || 0) * Number(product.price || 0))} so‘m`
        ])
      }]
    };
  }

  if (section === 'sales-history') {
    return {
      title: 'Sotuvlar tarixi',
      tables: [{
        title: 'Sotuvlar jadvali',
        headers: ['№', 'Tovar', 'Miqdor', 'Sotuv narxi/dona', 'Tannarx/dona', 'Jami savdo', 'To‘lov turi', 'Mijoz', 'Telefon', 'Qaytarish muddati', 'Foyda/zarar', 'Sana'],
        rows: sales.map((sale, index) => {
          const quantity = Number(sale.quantity || 0);
          const price = Number(sale.price || 0);
          const cost = Number(sale.costPrice || 0);
          const paymentLabel = { cash: 'Naqd', card: 'Karta', credit: 'Nasiya' }[sale.paymentMethod] || 'Naqd';
          return [index + 1, sale.name || '', `${quantity} dona`, `${formatMoney(price)} so‘m`, `${formatMoney(cost)} so‘m`, `${formatMoney(sale.total ?? quantity * price)} so‘m`, paymentLabel, sale.customerName || '', sale.customerPhone || '', sale.dueDate || '', `${formatMoney(quantity * (price - cost))} so‘m`, sale.date || ''];
        })
      }]
    };
  }

  if (section === 'expense-history') {
    return {
      title: 'Xarajatlar ro‘yxati',
      tables: [{
        title: 'Xarajatlar jadvali',
        headers: ['№', 'Nima uchun sarflandi', 'Qayerga sarflandi', 'Miqdori', 'Sana'],
        rows: expenses.map((expense, index) => {
          const date = new Date(expense.date);
          return [index + 1, expense.reason || '', expense.place || '', `${formatMoney(expense.amount)} so‘m`, Number.isNaN(date.getTime()) ? '' : date.toLocaleString('uz-UZ')];
        })
      }]
    };
  }

  if (section === 'debts') {
    return {
      title: 'Qarzlar va nasiyalar',
      tables: [{
        title: 'Mijozlar qarzlari',
        headers: ['№', 'Mijoz ismi', 'Telefon raqami', 'Jami qarz', 'To‘langan', 'Qoldiq', 'Qaytarish muddati', 'Qaytarish sanasi', 'Tovar', 'Holati'],
        rows: debts.map((debt, index) => [
          index + 1,
          debt.name || '',
          debt.phone || '',
          `${formatMoney(debt.amount)} so‘m`,
          `${formatMoney(Math.max(0, (Number(debt.amount) || 0) - getDebtRemaining(debt)))} so‘m`,
          `${formatMoney(getDebtRemaining(debt))} so‘m`,
          Number.isInteger(Number(debt.period)) ? `${debt.period} ${debt.periodUnit === 'months' ? 'oy' : 'kun'}` : '',
          debt.dueDate || '',
          debt.saleName || 'Qo‘lda kiritilgan qarz',
          getDebtRemaining(debt) <= 0 ? 'To‘langan' : Number(debt.amount) > getDebtRemaining(debt) ? 'Qisman to‘langan' : 'To‘lanmagan'
        ])
      }]
    };
  }

  if (section === 'warehouse-stock') {
    return {
      title: 'Ombor qoldig‘i',
      tables: [{
        title: 'Ombordagi tovarlar',
        headers: ['№', 'Tovar', 'Kategoriya', 'Rusumi', 'Rangi', 'O‘lchami', 'Miqdor', 'Tannarx/dona', 'Jami tannarx', 'Sotuv narxi'],
        rows: products.map((product, index) => [
          index + 1,
          product.name,
          product.category || 'Ko‘rsatilmagan',
          product.model || '—',
          product.color || '—',
          product.size || '—',
          `${Number(product.quantity || 0)} dona`,
          `${formatMoney(product.costPrice)} so‘m`,
          `${formatMoney(Number(product.quantity || 0) * Number(product.costPrice || 0))} so‘m`,
          `${formatMoney(product.price)} so‘m`
        ])
      }]
    };
  }

  if (section === 'store') {
    return {
      title: 'Do‘kon',
      tables: [
        {
          title: 'Do‘kondagi tovarlar',
          headers: ['Tovar', 'Kategoriya', 'Qoldiq', 'Sotuv narxi'],
          rows: products.filter(product => Number(product.storeQuantity || 0) > 0).map(product => [
            product.name,
            product.category || 'Kategoriya ko‘rsatilmagan',
            `${Number(product.storeQuantity || 0)} dona`,
            `${formatMoney(product.price)} so‘m`
          ])
        },
        {
          title: 'Sotuvlar tarixi',
          headers: ['Tovar', 'Miqdor', 'Narx/dona', 'Jami', 'To‘lov turi', 'Mijoz', 'Telefon', 'Muddat', 'Sana'],
          rows: sales.map(sale => [
            sale.name,
            `${Number(sale.quantity || 0)} dona`,
            `${formatMoney(sale.price)} so‘m`,
            `${formatMoney(sale.total ?? Number(sale.quantity || 0) * Number(sale.price || 0))} so‘m`,
            ({ cash: 'Naqd', card: 'Karta', credit: 'Nasiya' }[sale.paymentMethod] || 'Naqd'),
            sale.customerName || '',
            sale.customerPhone || '',
            sale.dueDate || '',
            sale.date || ''
          ])
        }
      ]
    };
  }

  if (section === 'expenses') {
    return {
      title: 'Xarajatlar',
      tables: [{
        title: 'Xarajatlar ro‘yxati',
        headers: ['Nima uchun', 'Qayerga', 'Miqdori', 'Sana'],
        rows: expenses.map(expense => {
          const date = new Date(expense.date);
          return [
            expense.reason || '',
            expense.place || '',
            `${formatMoney(expense.amount)} so‘m`,
            Number.isNaN(date.getTime()) ? '' : date.toLocaleString('uz-UZ')
          ];
        })
      }]
    };
  }

  if (section === 'warehouse') {
    return {
      title: 'Ombor',
      tables: [{
        title: 'Ombordagi tovarlar',
        headers: ['Tovar', 'Kategoriya', 'Rusumi', 'Rangi', 'O‘lchami', 'Miqdor', 'Tannarx/dona', 'Sotuv narxi'],
        rows: products.map(product => [
          product.name,
          product.category || '',
          product.model || '',
          product.color || '',
          product.size || '',
          `${Number(product.quantity || 0)} dona`,
          `${formatMoney(product.costPrice)} so‘m`,
          `${formatMoney(product.price)} so‘m`
        ])
      }]
    };
  }

  return {
    title: 'Sozlamalar',
    tables: [{
      title: 'Do‘kon sozlamalari',
      headers: ['Sozlama', 'Qiymat'],
      rows: [
        ['Do‘kon nomi', shopName],
        ['Stiker', shopSticker || 'Stikersiz'],
        ['Kam qolgan tovar chegarasi', `${lowStockThreshold} dona`],
        ['Fon rangi', backgroundTheme],
        ['Qorong‘i rejim', darkMode ? 'Yoqilgan' : 'O‘chirilgan']
      ]
    }]
  };
}

function escapeExportHTML(value) {
  return String(value ?? '').replace(/[&<>"']/g, character => ({
    '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;'
  })[character]);
}

function downloadSectionExport(section, format) {
  const report = getExportTables(section);
  const tablesHTML = report.tables.map(table => {
    const headings = table.headers.map(header => `<th>${escapeExportHTML(header)}</th>`).join('');
    const rows = table.rows.length
      ? table.rows.map(row => `<tr>${row.map(value => `<td>${escapeExportHTML(value)}</td>`).join('')}</tr>`).join('')
      : `<tr><td colspan="${table.headers.length}">Ma’lumot yo‘q</td></tr>`;
    return `<h2>${escapeExportHTML(table.title)}</h2><table><thead><tr>${headings}</tr></thead><tbody>${rows}</tbody></table>`;
  }).join('');
  const documentHTML = `<!DOCTYPE html><html><head><meta charset="UTF-8"><style>body{font-family:Arial,sans-serif;color:#20243a;margin:28px}h1{font-size:22px;color:#334a9e;border-bottom:2px solid #6879e5;padding-bottom:10px}h2{font-size:16px;margin:24px 0 8px;color:#334a9e}p{color:#666;font-size:12px}table{width:100%;border-collapse:collapse;margin:10px 0 24px}th,td{border:1px solid #cbd2e3;padding:8px;text-align:left;vertical-align:top}th{background:#e9edf8;color:#283c79}tbody tr:nth-child(even){background:#f5f7fc}td{font-size:12px}</style></head><body><h1>${escapeExportHTML(shopName)} — ${escapeExportHTML(report.title)}</h1><p>Sana: ${escapeExportHTML(new Date().toLocaleString('uz-UZ'))}</p>${tablesHTML}</body></html>`;
  const isExcel = format === 'excel';
  const blob = new Blob([isExcel ? `\uFEFF${documentHTML}` : documentHTML], {
    type: isExcel ? 'application/vnd.ms-excel;charset=utf-8' : 'application/msword;charset=utf-8'
  });
  const url = URL.createObjectURL(blob);
  const link = document.createElement('a');
  const safeShopName = shopName.replace(/[^a-z0-9_-]+/gi, '-').replace(/^-|-$/g, '') || 'dokon';
  link.href = url;
  link.download = `${safeShopName}-${section}.${isExcel ? 'xls' : 'doc'}`;
  link.click();
  setTimeout(() => URL.revokeObjectURL(url), 1000);
}

document.querySelectorAll('[data-export-section][data-export-format]').forEach(button => {
  button.addEventListener('click', () => {
    downloadSectionExport(button.dataset.exportSection, button.dataset.exportFormat);
  });
});

function updateCreditFields() {
  const isCredit = salePaymentMethod.value === 'credit';
  saleCreditFields.hidden = !isCredit;
  saleCustomerName.required = isCredit;
  saleCustomerPhone.required = isCredit;
  saleCreditPeriod.required = isCredit;
  saleCreditPeriodUnit.required = isCredit;
  if (isCredit) updateDueDatePreview(saleDueDatePreview, saleCreditPeriod, saleCreditPeriodUnit);
}

salePaymentMethod.addEventListener('change', updateCreditFields);
updateCreditFields();

function updateSalePreview() {
  const product = products[Number(saleProductInput.value)];
  const quantity = Number(saleQuantityInput.value);
  const price = Number(salePriceInput.value);
  const hasQuantity = saleQuantityInput.value !== '' && Number.isFinite(quantity);
  const hasPrice = salePriceInput.value !== '' && Number.isFinite(price);

  salePriceFormatted.textContent = `Ko‘rinishi: ${hasPrice ? formatMoney(price) : '0'} so‘m`;
  saleCostHint.classList.toggle(
    'stock-warning',
    Boolean(product && hasPrice && price < Number(product.costPrice || 0))
  );
  const reservedQuantity = product
    ? saleCart.filter(item => item.productId === product.id).reduce((total, item) => total + item.quantity, 0)
    : 0;
  saleQuantityInput.classList.toggle(
    'input-warning',
    Boolean(product && hasQuantity && quantity > Number(product.storeQuantity || 0) - reservedQuantity)
  );
  salePriceInput.classList.toggle(
    'input-warning',
    Boolean(product && hasPrice && price < Number(product.costPrice || 0))
  );
}

saleProductSearchInput.addEventListener('input', () => {
  saleProductInput.value = '';
  populateProductSelect(saleProductInput, 'storeQuantity', saleCategoryInput.value, saleProductSearchInput.value);
  const matching = products.filter(product => Number(product.storeQuantity || 0) > 0 &&
    (!saleCategoryInput.value || (product.category || 'Kategoriya ko‘rsatilmagan').trim() === saleCategoryInput.value) &&
    matchesProductSearch(product, saleProductSearchInput.value));
  if (saleProductSearchInput.value.trim() && matching.length === 1) {
    const index = products.indexOf(matching[0]);
    if ([...saleProductInput.options].some(option => option.value === String(index))) {
      saleProductInput.value = String(index);
      saleProductInput.dispatchEvent(new Event('change'));
    }
  } else {
    saleCostHint.textContent = 'Mos tovarni ro‘yxatdan tanlang.';
    updateSalePreview();
  }
});

saleCategoryInput.addEventListener('change', () => {
  saleProductInput.value = '';
  saleQuantityInput.value = '';
  salePriceInput.value = '';
  populateProductSelect(saleProductInput, 'storeQuantity', saleCategoryInput.value, saleProductSearchInput.value);
  saleCostHint.textContent = 'Tovar tanlang — tannarxi va do‘kondagi qoldiq shu yerda ko‘rinadi.';
  updateSalePreview();
});

saleProductInput.addEventListener('change', () => {
  const product = products[Number(saleProductInput.value)];
  if (!product) {
    saleCostHint.textContent = 'Tovar tanlang — tannarxi va do‘kondagi qoldiq shu yerda ko‘rinadi.';
    salePriceInput.value = '';
    updateSalePreview();
    return;
  }
  salePriceInput.value = Number(product.price || 0);
  saleCostHint.textContent = `Tannarx: ${formatMoney(product.costPrice)} so‘m/dona · Do‘konda: ${Number(product.storeQuantity || 0)} dona`;
  updateSalePreview();
});

saleQuantityInput.addEventListener('input', updateSalePreview);
salePriceInput.addEventListener('input', updateSalePreview);

addToCartButton.addEventListener('click', () => {
  const product = products[Number(saleProductInput.value)];
  const quantity = Number(saleQuantityInput.value);
  const price = Number(salePriceInput.value);
  if (!product || !Number.isInteger(quantity) || quantity < 1 || !Number.isFinite(price) || price < 0) {
    window.alert('Tovar, miqdor va sotuv narxini to‘g‘ri kiriting.');
    return;
  }
  const alreadyInCart = saleCart.filter(item => item.productId === product.id)
    .reduce((total, item) => total + item.quantity, 0);
  const available = Number(product.storeQuantity || 0) - alreadyInCart;
  if (quantity > available) {
    window.alert(`Do‘konda savatdagi miqdorni hisobga olganda faqat ${Math.max(0, available)} dona qoldi.`);
    return;
  }
  if (price < Number(product.costPrice || 0) && !window.confirm('Sotuv narxi tannarxdan arzon. Zararga sotishni davom ettirasizmi?')) return;

  const sameItem = saleCart.find(item => item.productId === product.id && item.price === price);
  if (sameItem) sameItem.quantity += quantity;
  else saleCart.push({
    productId: product.id,
    name: product.name,
    quantity,
    price,
    costPrice: Number(product.costPrice || 0)
  });
  saleQuantityInput.value = '';
  updateSalePreview();
  renderSaleCart();
  saleQuantityInput.focus();
});

saleCartList.addEventListener('click', event => {
  const button = event.target.closest('[data-remove-cart-index]');
  if (!button) return;
  saleCart.splice(Number(button.dataset.removeCartIndex), 1);
  renderSaleCart();
});

clearCartButton.addEventListener('click', () => {
  if (!saleCart.length || !window.confirm('Savatdagi barcha tovarlarni olib tashlaysizmi?')) return;
  saleCart = [];
  renderSaleCart();
});

function showReceipt(items, paymentMethod, total, details = {}) {
  receiptSticker.textContent = shopSticker;
  receiptShopName.textContent = shopName;
  receiptDate.textContent = new Date().toLocaleString('uz-UZ');
  receiptNumber.textContent = `Chek № ${Date.now().toString().slice(-8)}`;
  receiptItems.replaceChildren();
  items.forEach(item => {
    const row = document.createElement('tr');
    [item.name, `${item.quantity} dona`, `${formatMoney(item.quantity * item.price)} so‘m`].forEach(value => {
      const cell = document.createElement('td');
      cell.textContent = value;
      row.append(cell);
    });
    receiptItems.append(row);
  });
  receiptTotal.textContent = `Jami: ${formatMoney(total)} so‘m`;
  const paymentLabel = { cash: 'Naqd', card: 'Karta', credit: 'Nasiya' }[paymentMethod] || 'Naqd';
  const customerText = paymentMethod === 'credit'
    ? ` · Mijoz: ${details.customerName} · Muddat: ${new Date(`${details.dueDate}T00:00:00`).toLocaleDateString('uz-UZ')}`
    : '';
  receiptPayment.textContent = `To‘lov: ${paymentLabel}${customerText}`;
  receiptDialog.showModal();
}

saleForm.addEventListener('submit', event => {
  event.preventDefault();
  if (saleCart.length === 0) {
    window.alert('Avval tovarlarni savatga qo‘shing.');
    return;
  }
  const isCredit = salePaymentMethod.value === 'credit';
  const customerName = saleCustomerName.value.trim();
  const customerPhone = saleCustomerPhone.value.trim();
  const creditPeriod = Number(saleCreditPeriod.value);
  const creditPeriodUnit = saleCreditPeriodUnit.value;
  if (isCredit && (!customerName || !customerPhone || !Number.isInteger(creditPeriod) || creditPeriod < 1)) {
    window.alert('Nasiya uchun mijoz ma’lumoti va qaytarish muddatini kiriting.');
    return;
  }
  const stockNeeded = new Map();
  saleCart.forEach(item => stockNeeded.set(item.productId, (stockNeeded.get(item.productId) || 0) + item.quantity));
  for (const [productId, quantity] of stockNeeded) {
    const product = products.find(item => item.id === productId);
    if (!product || quantity > Number(product.storeQuantity || 0)) {
      window.alert(`“${product ? product.name : 'Tovar'}” uchun qoldiq yetarli emas. Savatni tekshiring.`);
      return;
    }
  }

  const soldItems = saleCart.map(item => ({ ...item }));
  const paymentMethod = salePaymentMethod.value;
  const dueDate = isCredit ? calculateDueDate(creditPeriod, creditPeriodUnit) : '';
  const saleDate = new Date();
  soldItems.forEach(item => {
    const product = products.find(entry => entry.id === item.productId);
    product.storeQuantity = Number(product.storeQuantity || 0) - item.quantity;
    const amount = item.quantity * item.price;
    const saleId = createRecordId('sale');
    sales.push({
      saleId, productId: product.id, name: item.name, quantity: item.quantity,
      price: item.price, costPrice: item.costPrice, total: amount, paymentMethod,
      customerName: isCredit ? customerName : '', customerPhone: isCredit ? customerPhone : '',
      dueDate: isCredit ? dueDate : '', creditPeriod: isCredit ? creditPeriod : null,
      creditPeriodUnit: isCredit ? creditPeriodUnit : '', date: saleDate.toISOString(),
      dateKey: localDateKey(saleDate)
    });
    if (isCredit) debts.push({
      saleId, name: customerName, phone: customerPhone, amount, dueDate,
      period: creditPeriod, periodUnit: creditPeriodUnit, saleName: item.name,
      createdAt: saleDate.toISOString(), paid: false
    });
  });

  const total = soldItems.reduce((sum, item) => sum + item.quantity * item.price, 0);
  saleCart = [];
  renderProducts();
  saveData();
  saleForm.reset();
  populateSaleCategories();
  populateProductSelect(saleProductInput, 'storeQuantity', saleCategoryInput.value, saleProductSearchInput.value);
  updateCreditFields();
  updateDueDatePreview(saleDueDatePreview, saleCreditPeriod, saleCreditPeriodUnit);
  saleCostHint.textContent = 'Tovar tanlang — tannarxi va do‘kondagi qoldiq shu yerda ko‘rinadi.';
  saleCostHint.classList.remove('stock-warning');
  updateSalePreview();
  renderSaleCart();
  showReceipt(soldItems, paymentMethod, total, { customerName, dueDate });
});

closeReceiptButton.addEventListener('click', () => receiptDialog.close());
printReceiptButton.addEventListener('click', () => window.print());
receiptDialog.addEventListener('click', event => {
  if (event.target === receiptDialog) receiptDialog.close();
});

transferForm.addEventListener('submit', event => {
  event.preventDefault();
  const product = products[Number(transferProductInput.value)];
  const quantity = Number(transferQuantityInput.value);
  if (!product || !Number.isInteger(quantity) || quantity < 1) return;
  if (quantity > Number(product.quantity || 0)) {
    window.alert('Omborda bu miqdorda tovar yo‘q.');
    return;
  }

  product.quantity = Number(product.quantity || 0) - quantity;
  product.storeQuantity = Number(product.storeQuantity || 0) + quantity;
  renderProducts();
  saveData();
  transferForm.reset();
});

editShopNameButton.addEventListener('click', () => {
  lowStockForm.hidden = true;
  shopNameInput.value = shopName;
  shopStickerInput.value = shopSticker;
  lowStockThresholdInput.value = lowStockThreshold;
  settingsForm.hidden = false;
  shopNameInput.focus();
});

settingsForm.addEventListener('submit', event => {
  event.preventDefault();
  const newName = shopNameInput.value.trim();
  if (!newName) return;

  shopName = newName;
  shopSticker = shopStickerInput.value;
  shopNameElement.textContent = shopName;
  shopStickerElement.textContent = shopSticker;
  saveData();
  settingsForm.hidden = true;
});

cancelSettings.addEventListener('click', () => {
  settingsForm.hidden = true;
});

editLowStockButton.addEventListener('click', () => {
  settingsForm.hidden = true;
  lowStockThresholdInput.value = lowStockThreshold;
  lowStockForm.hidden = false;
  lowStockThresholdInput.focus();
});

lowStockForm.addEventListener('submit', event => {
  event.preventDefault();
  const newThreshold = Number(lowStockThresholdInput.value);
  if (!Number.isInteger(newThreshold) || newThreshold < 0) return;

  lowStockThreshold = newThreshold;
  currentStockThreshold.textContent = `${lowStockThreshold} dona`;
  renderProducts();
  saveData();
  lowStockForm.hidden = true;
});

cancelLowStock.addEventListener('click', () => {
  lowStockForm.hidden = true;
});

backgroundColorInput.addEventListener('change', () => {
  backgroundTheme = backgroundThemes.includes(backgroundColorInput.value) ? backgroundColorInput.value : 'lavender';
  document.body.dataset.theme = backgroundTheme;
  saveData();
});

darkModeInput.addEventListener('change', () => {
  darkMode = darkModeInput.checked;
  document.body.classList.toggle('dark-mode', darkMode);
  saveData();
});

function downloadBackup() {
  saveData();
  const file = new Blob([JSON.stringify(savedData, null, 2)], { type: 'application/json' });
  const url = URL.createObjectURL(file);
  const link = document.createElement('a');
  link.href = url;
  link.download = 'dokon-zaxira.json';
  link.click();
  setTimeout(() => URL.revokeObjectURL(url), 1000);
  try {
    localStorage.setItem(BACKUP_DATE_KEY, new Date().toISOString());
  } catch (error) {
    // Zaxira fayli yuklanadi, faqat eslatma holatini saqlab bo‘lmasligi mumkin.
  }
  updateBackupReminder();
}

exportDataButton.addEventListener('click', downloadBackup);
backupReminderButton.addEventListener('click', downloadBackup);

importDataInput.addEventListener('change', async () => {
  const file = importDataInput.files[0];
  if (!file) return;

  try {
    const imported = JSON.parse(await file.text());
    const isObject = value => value && typeof value === 'object' && !Array.isArray(value);
    const validProducts = isObject(imported) && Array.isArray(imported.products) && imported.products.every(product =>
      isObject(product) && typeof product.name === 'string' && Number.isFinite(Number(product.quantity)) &&
      (product.price === undefined || Number.isFinite(Number(product.price))) &&
      (product.costPrice === undefined || Number.isFinite(Number(product.costPrice)))
    );
    const validCollection = (key, validateItem) => imported[key] === undefined ||
      (Array.isArray(imported[key]) && imported[key].every(validateItem));
    const validSales = validCollection('sales', sale =>
      isObject(sale) && typeof sale.name === 'string' && Number.isFinite(Number(sale.quantity)) &&
      Number(sale.quantity) >= 1 && Number.isFinite(Number(sale.price)) && Number(sale.price) >= 0 &&
      (sale.total === undefined || Number.isFinite(Number(sale.total)))
    );
    const validExpenses = validCollection('expenses', expense =>
      isObject(expense) && typeof expense.reason === 'string' && typeof expense.place === 'string' &&
      Number.isFinite(Number(expense.amount)) && Number(expense.amount) >= 0 &&
      (expense.date === undefined || typeof expense.date === 'string')
    );
    const validDebts = validCollection('debts', debt =>
      isObject(debt) && typeof debt.name === 'string' && typeof debt.phone === 'string' &&
      Number.isFinite(Number(debt.amount)) && Number(debt.amount) >= 0 &&
      (debt.dueDate === undefined || typeof debt.dueDate === 'string') &&
      (debt.paid === undefined || typeof debt.paid === 'boolean') &&
      (debt.paidAmount === undefined || (Number.isFinite(Number(debt.paidAmount)) && Number(debt.paidAmount) >= 0)) &&
      (debt.payments === undefined || (Array.isArray(debt.payments) && debt.payments.every(payment =>
        isObject(payment) && Number.isFinite(Number(payment.amount)) && Number(payment.amount) >= 0 &&
        (payment.date === undefined || typeof payment.date === 'string')
      )))
    );
    if (!validProducts || !validSales || !validExpenses || !validDebts) {
      throw new Error('Noto‘g‘ri zaxira fayli');
    }

    if (!window.confirm('Joriy ma’lumotlar zaxira faylidagi ma’lumotlar bilan almashtirilsinmi?')) return;

    savedData = imported;
    shopName = typeof imported.shopName === 'string' && imported.shopName.trim()
      ? imported.shopName
      : 'Mening do‘konim';
    shopSticker = typeof imported.shopSticker === 'string' ? imported.shopSticker : '';
    products = imported.products;
    products.forEach(product => {
      if (!product.id) product.id = createRecordId('product');
      if (!Number.isFinite(Number(product.storeQuantity))) product.storeQuantity = 0;
    });
    sales = Array.isArray(imported.sales) ? imported.sales : [];
    expenses = Array.isArray(imported.expenses) ? imported.expenses : [];
    debts = Array.isArray(imported.debts) ? imported.debts : [];
    lowStockThreshold = Number.isInteger(imported.lowStockThreshold) && imported.lowStockThreshold >= 0
      ? imported.lowStockThreshold
      : 5;
    backgroundTheme = backgroundThemes.includes(imported.backgroundTheme) ? imported.backgroundTheme : 'lavender';
    darkMode = imported.darkMode === true;
    backgroundColorInput.value = backgroundTheme;
    darkModeInput.checked = darkMode;
    document.body.dataset.theme = backgroundTheme;
    document.body.classList.toggle('dark-mode', darkMode);
    shopNameElement.textContent = shopName;
    shopStickerElement.textContent = shopSticker;
    lowStockThresholdInput.value = lowStockThreshold;
    currentStockThreshold.textContent = `${lowStockThreshold} dona`;
    renderProducts();
    saveData();
    window.alert('Zaxira nusxasi muvaffaqiyatli tiklandi.');
  } catch (error) {
    window.alert('Faylni o‘qib bo‘lmadi. To‘g‘ri zaxira JSON faylini tanlang.');
  } finally {
    importDataInput.value = '';
  }
});

