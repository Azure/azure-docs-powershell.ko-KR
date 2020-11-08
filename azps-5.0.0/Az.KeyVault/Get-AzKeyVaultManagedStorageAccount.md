---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 6e7cbaf9ed6e9f0d9751e8e16004891a7fcbb056
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215314"
---
# <span data-ttu-id="0cca4-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cca4-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0cca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cca4-102">SYNOPSIS</span></span>
<span data-ttu-id="0cca4-103">키 보관소 관리 Azure 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="0cca4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0cca4-104">SYNTAX</span></span>

### <span data-ttu-id="0cca4-105">ByAccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0cca4-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cca4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0cca4-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cca4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0cca4-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cca4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0cca4-108">DESCRIPTION</span></span>
<span data-ttu-id="0cca4-109">계정 이름이 지정 되 고 계정 키가 지정 된 자격 증명 모음에 의해 관리 되는 경우 키 보관소 관리 Azure 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="0cca4-110">계정 이름을 지정 하지 않으면 해당 키가 지정 된 자격 증명 모음에 의해 관리 되는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="0cca4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0cca4-111">EXAMPLES</span></span>

### <span data-ttu-id="0cca4-112">예제 1: 모든 키 보관소 관리 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="0cca4-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="0cca4-113">' Myvault ' 자격 증명 모음으로 해당 키를 관리 하는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="0cca4-114">예제 2: 키 보관소 관리 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="0cca4-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="0cca4-115">' Mystorageaccount ' 키 저장소 계정이 자격 증명 모음 ' myvault '에 의해 관리 되는 경우 해당 키 자격 증명 모음 관리의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="0cca4-116">예제 3: 필터링을 사용 하 여 모든 키 보관소 관리 저장소 계정 나열</span><span class="sxs-lookup"><span data-stu-id="0cca4-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="0cca4-117">"Test"로 시작 하는 자격 증명 모음 ' myvault '에 의해 해당 키가 관리 되는 모든 계정이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="0cca4-118">변수</span><span class="sxs-lookup"><span data-stu-id="0cca4-118">PARAMETERS</span></span>

### <span data-ttu-id="0cca4-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0cca4-119">-AccountName</span></span>
<span data-ttu-id="0cca4-120">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="0cca4-121">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="0cca4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cca4-122">-DefaultProfile</span></span>
<span data-ttu-id="0cca4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0cca4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cca4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cca4-124">-InputObject</span></span>
<span data-ttu-id="0cca4-125">자격 증명 모음 개체.</span><span class="sxs-lookup"><span data-stu-id="0cca4-125">Vault object.</span></span>

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

### <span data-ttu-id="0cca4-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0cca4-126">-InRemovedState</span></span>
<span data-ttu-id="0cca4-127">이전에 삭제 된 저장소 계정을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="0cca4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cca4-128">-ResourceId</span></span>
<span data-ttu-id="0cca4-129">자격 증명 모음 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-129">Vault resource id.</span></span>

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

### <span data-ttu-id="0cca4-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0cca4-130">-VaultName</span></span>
<span data-ttu-id="0cca4-131">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="0cca4-131">Vault name.</span></span>
<span data-ttu-id="0cca4-132">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0cca4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cca4-133">CommonParameters</span></span>
<span data-ttu-id="0cca4-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cca4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cca4-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0cca4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cca4-136">입력</span><span class="sxs-lookup"><span data-stu-id="0cca4-136">INPUTS</span></span>

### <span data-ttu-id="0cca4-137">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0cca4-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0cca4-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0cca4-138">System.String</span></span>

## <span data-ttu-id="0cca4-139">출력</span><span class="sxs-lookup"><span data-stu-id="0cca4-139">OUTPUTS</span></span>

### <span data-ttu-id="0cca4-140">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0cca4-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="0cca4-141">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cca4-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="0cca4-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0cca4-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="0cca4-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cca4-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0cca4-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0cca4-144">NOTES</span></span>

## <span data-ttu-id="0cca4-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cca4-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

