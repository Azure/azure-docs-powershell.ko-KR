---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334929"
---
# <span data-ttu-id="dc832-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dc832-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="dc832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc832-102">SYNOPSIS</span></span>
<span data-ttu-id="dc832-103">Key Vault 관리 Azure Storage 계정의 지정된 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="dc832-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc832-104">SYNTAX</span></span>

### <span data-ttu-id="dc832-105">ByDefinitionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc832-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc832-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc832-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc832-107">설명</span><span class="sxs-lookup"><span data-stu-id="dc832-107">DESCRIPTION</span></span>
<span data-ttu-id="dc832-108">Key Vault 관리 Azure Storage 계정의 지정된 키를 다시 생성하고 키를 활성 키로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="dc832-109">Key Vault는 Azure Resource Manager에 대한 호출을 프로시저하여 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="dc832-110">호출자는 주어진 Azure Storage 계정에서 키를 다시 생성하는 권한을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="dc832-111">예제</span><span class="sxs-lookup"><span data-stu-id="dc832-111">EXAMPLES</span></span>

### <span data-ttu-id="dc832-112">예제 1: 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="dc832-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="dc832-113">'mystorageaccount' 계정의 'key1'을 다시 생성하고 'key1'을 Key Vault 관리 Azure Storage 계정의 활성으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="dc832-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc832-114">PARAMETERS</span></span>

### <span data-ttu-id="dc832-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc832-115">-AccountName</span></span>
<span data-ttu-id="dc832-116">Key Vault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="dc832-117">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc832-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc832-118">-DefaultProfile</span></span>
<span data-ttu-id="dc832-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dc832-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc832-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dc832-120">-Force</span></span>
<span data-ttu-id="dc832-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dc832-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc832-122">-InputObject</span></span>
<span data-ttu-id="dc832-123">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc832-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dc832-124">-KeyName</span></span>
<span data-ttu-id="dc832-125">다시 생성하고 활성화할 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc832-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc832-126">-PassThru</span></span>
<span data-ttu-id="dc832-127">Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dc832-128">이 스위치를 지정하면 cmdlet은 삭제된 관리되는 저장소 계정을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="dc832-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dc832-129">-VaultName</span></span>
<span data-ttu-id="dc832-130">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-130">Vault name.</span></span>
<span data-ttu-id="dc832-131">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc832-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc832-132">-Confirm</span></span>
<span data-ttu-id="dc832-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc832-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc832-134">-WhatIf</span></span>
<span data-ttu-id="dc832-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc832-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc832-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc832-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc832-137">CommonParameters</span></span>
<span data-ttu-id="dc832-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc832-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc832-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc832-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc832-140">입력</span><span class="sxs-lookup"><span data-stu-id="dc832-140">INPUTS</span></span>

### <span data-ttu-id="dc832-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="dc832-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="dc832-142">출력</span><span class="sxs-lookup"><span data-stu-id="dc832-142">OUTPUTS</span></span>

### <span data-ttu-id="dc832-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc832-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="dc832-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc832-144">NOTES</span></span>

## <span data-ttu-id="dc832-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc832-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

