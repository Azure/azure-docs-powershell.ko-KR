---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 89452f2a00aea9d3ab42300c2f28bde67fec0905
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323938"
---
# <span data-ttu-id="c757d-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c757d-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c757d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c757d-102">SYNOPSIS</span></span>
<span data-ttu-id="c757d-103">Key Vault 관리 Azure Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="c757d-104">구문</span><span class="sxs-lookup"><span data-stu-id="c757d-104">SYNTAX</span></span>

### <span data-ttu-id="c757d-105">ByAccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c757d-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c757d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c757d-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c757d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c757d-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c757d-108">설명</span><span class="sxs-lookup"><span data-stu-id="c757d-108">DESCRIPTION</span></span>
<span data-ttu-id="c757d-109">계정 이름이 지정되고 계정 키가 지정된 자격 증명 모음에서 관리되는 경우 Key Vault 관리 Azure Storage 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="c757d-110">계정 이름을 지정하지 않으면 지정된 자격 증명 모음에서 키를 관리하는 모든 계정이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="c757d-111">예제</span><span class="sxs-lookup"><span data-stu-id="c757d-111">EXAMPLES</span></span>

### <span data-ttu-id="c757d-112">예제 1: 모든 Key Vault 관리 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="c757d-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="c757d-113">자격 증명 모음 'myvault'에서 키를 관리하는 모든 계정을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="c757d-114">예제 2: Key Vault 관리 저장소 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="c757d-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

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

<span data-ttu-id="c757d-115">키가 자격 증명 모음 'myvault'에서 관리되는 경우 'mystorageaccount'의 Key Vault 관리 스토리지 계정의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="c757d-116">예제 3: 필터링을 사용하여 모든 Key Vault 관리되는 Storage 계정 나열</span><span class="sxs-lookup"><span data-stu-id="c757d-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="c757d-117">"test"로 시작하는 자격 증명 모음 'myvault'에서 키를 관리하는 모든 계정을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="c757d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c757d-118">PARAMETERS</span></span>

### <span data-ttu-id="c757d-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c757d-119">-AccountName</span></span>
<span data-ttu-id="c757d-120">Key Vault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="c757d-121">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c757d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c757d-122">-DefaultProfile</span></span>
<span data-ttu-id="c757d-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c757d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c757d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c757d-124">-InputObject</span></span>
<span data-ttu-id="c757d-125">자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-125">Vault object.</span></span>

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

### <span data-ttu-id="c757d-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c757d-126">-InRemovedState</span></span>
<span data-ttu-id="c757d-127">이전에 삭제된 저장소 계정을 출력에 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="c757d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c757d-128">-ResourceId</span></span>
<span data-ttu-id="c757d-129">자격 증명 모음 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-129">Vault resource id.</span></span>

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

### <span data-ttu-id="c757d-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c757d-130">-VaultName</span></span>
<span data-ttu-id="c757d-131">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-131">Vault name.</span></span>
<span data-ttu-id="c757d-132">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c757d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c757d-133">CommonParameters</span></span>
<span data-ttu-id="c757d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c757d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c757d-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c757d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c757d-136">입력</span><span class="sxs-lookup"><span data-stu-id="c757d-136">INPUTS</span></span>

### <span data-ttu-id="c757d-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="c757d-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c757d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c757d-138">System.String</span></span>

## <span data-ttu-id="c757d-139">출력</span><span class="sxs-lookup"><span data-stu-id="c757d-139">OUTPUTS</span></span>

### <span data-ttu-id="c757d-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c757d-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="c757d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c757d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="c757d-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c757d-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="c757d-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c757d-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c757d-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c757d-144">NOTES</span></span>

## <span data-ttu-id="c757d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c757d-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

