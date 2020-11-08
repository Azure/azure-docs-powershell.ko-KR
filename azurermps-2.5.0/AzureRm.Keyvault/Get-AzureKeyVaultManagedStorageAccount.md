---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 51e7b941e5dbb4d07b48444196f6e3d3aa830452
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881889"
---
# <span data-ttu-id="fc3f9-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc3f9-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fc3f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc3f9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3f9-103">키 보관소 관리 Azure 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc3f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc3f9-104">SYNTAX</span></span>

### <span data-ttu-id="fc3f9-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc3f9-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc3f9-106">ByAccountName</span><span class="sxs-lookup"><span data-stu-id="fc3f9-106">ByAccountName</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc3f9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc3f9-107">DESCRIPTION</span></span>
<span data-ttu-id="fc3f9-108">계정 이름이 지정 되 고 계정 키가 지정 된 자격 증명 모음에 의해 관리 되는 경우 키 보관소 관리 Azure 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-108">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="fc3f9-109">계정 이름을 지정 하지 않으면 해당 키가 지정 된 자격 증명 모음에 의해 관리 되는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-109">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="fc3f9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fc3f9-110">EXAMPLES</span></span>

### <span data-ttu-id="fc3f9-111">예제 1: 모든 키 보관소 관리 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="fc3f9-111">Example 1: List all Key Vault managed Storage Accounts</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'
```

<span data-ttu-id="fc3f9-112">' Myvault ' 자격 증명 모음으로 해당 키를 관리 하는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-112">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="fc3f9-113">예제 2: 키 보관소 관리 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="fc3f9-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'
```

<span data-ttu-id="fc3f9-114">' Mystorageaccount ' 키 저장소 계정이 자격 증명 모음 ' myvault '에 의해 관리 되는 경우 해당 키 자격 증명 모음 관리의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-114">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="fc3f9-115">변수</span><span class="sxs-lookup"><span data-stu-id="fc3f9-115">PARAMETERS</span></span>

### <span data-ttu-id="fc3f9-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc3f9-116">-AccountName</span></span>
<span data-ttu-id="fc3f9-117">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-117">Key Vault managed storage account name.</span></span> <span data-ttu-id="fc3f9-118">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc3f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3f9-119">-DefaultProfile</span></span>
<span data-ttu-id="fc3f9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc3f9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3f9-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fc3f9-121">-VaultName</span></span>
<span data-ttu-id="fc3f9-122">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="fc3f9-122">Vault name.</span></span>
<span data-ttu-id="fc3f9-123">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc3f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3f9-124">CommonParameters</span></span>
<span data-ttu-id="fc3f9-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc3f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3f9-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc3f9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3f9-127">입력</span><span class="sxs-lookup"><span data-stu-id="fc3f9-127">INPUTS</span></span>

### <span data-ttu-id="fc3f9-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc3f9-128">System.String</span></span>

## <span data-ttu-id="fc3f9-129">출력</span><span class="sxs-lookup"><span data-stu-id="fc3f9-129">OUTPUTS</span></span>

### <span data-ttu-id="fc3f9-130">System.webserver. List ' 1 [[Microsoft Azure.]. t e m '을 (를) ' ' [2.5.0.0 Storageaccount. '. KeyVault, Version =, Culture = 중립적인, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fc3f9-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount, Microsoft.Azure.Commands.KeyVault, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fc3f9-131">Microsoft. KeyVault. \* ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc3f9-131">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="fc3f9-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fc3f9-132">NOTES</span></span>

## <span data-ttu-id="fc3f9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc3f9-133">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
