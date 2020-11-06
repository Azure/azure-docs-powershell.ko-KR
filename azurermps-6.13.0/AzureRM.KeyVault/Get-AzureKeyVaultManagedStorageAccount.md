---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: f3a1e4d1e938b84a434c07451f3d2294e203f440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534328"
---
# <span data-ttu-id="663a0-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663a0-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="663a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="663a0-102">SYNOPSIS</span></span>
<span data-ttu-id="663a0-103">키 보관소 관리 Azure 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="663a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="663a0-104">SYNTAX</span></span>

### <span data-ttu-id="663a0-105">ByAccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="663a0-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="663a0-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663a0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="663a0-107">ByResourceId</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="663a0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="663a0-108">DESCRIPTION</span></span>
<span data-ttu-id="663a0-109">계정 이름이 지정 되 고 계정 키가 지정 된 자격 증명 모음에 의해 관리 되는 경우 키 보관소 관리 Azure 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="663a0-110">계정 이름을 지정 하지 않으면 해당 키가 지정 된 자격 증명 모음에 의해 관리 되는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="663a0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="663a0-111">EXAMPLES</span></span>

### <span data-ttu-id="663a0-112">예제 1: 모든 키 보관소 관리 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="663a0-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="663a0-113">' Myvault ' 자격 증명 모음으로 해당 키를 관리 하는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="663a0-114">예제 2: 키 보관소 관리 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="663a0-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="663a0-115">' Mystorageaccount ' 키 저장소 계정이 자격 증명 모음 ' myvault '에 의해 관리 되는 경우 해당 키 자격 증명 모음 관리의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="663a0-116">변수</span><span class="sxs-lookup"><span data-stu-id="663a0-116">PARAMETERS</span></span>

### <span data-ttu-id="663a0-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="663a0-117">-AccountName</span></span>
<span data-ttu-id="663a0-118">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="663a0-119">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663a0-120">-DefaultProfile</span></span>
<span data-ttu-id="663a0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="663a0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663a0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="663a0-122">-InputObject</span></span>
<span data-ttu-id="663a0-123">자격 증명 모음 개체.</span><span class="sxs-lookup"><span data-stu-id="663a0-123">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="663a0-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="663a0-124">-InRemovedState</span></span>
<span data-ttu-id="663a0-125">이전에 삭제 된 저장소 계정을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-125">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663a0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="663a0-126">-ResourceId</span></span>
<span data-ttu-id="663a0-127">자격 증명 모음 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-127">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663a0-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="663a0-128">-VaultName</span></span>
<span data-ttu-id="663a0-129">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="663a0-129">Vault name.</span></span>
<span data-ttu-id="663a0-130">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="663a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663a0-131">CommonParameters</span></span>
<span data-ttu-id="663a0-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="663a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663a0-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="663a0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663a0-134">입력</span><span class="sxs-lookup"><span data-stu-id="663a0-134">INPUTS</span></span>

### <span data-ttu-id="663a0-135">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="663a0-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="663a0-136">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="663a0-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="663a0-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="663a0-137">System.String</span></span>

## <span data-ttu-id="663a0-138">출력</span><span class="sxs-lookup"><span data-stu-id="663a0-138">OUTPUTS</span></span>

### <span data-ttu-id="663a0-139">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="663a0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="663a0-140">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663a0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="663a0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="663a0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="663a0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="663a0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="663a0-143">상속자</span><span class="sxs-lookup"><span data-stu-id="663a0-143">NOTES</span></span>

## <span data-ttu-id="663a0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="663a0-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

