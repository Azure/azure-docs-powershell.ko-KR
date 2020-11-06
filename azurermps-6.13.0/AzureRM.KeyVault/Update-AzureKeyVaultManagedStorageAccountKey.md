---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 2e096b04830d50840d6298e7aa8085b0090a347e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534315"
---
# <span data-ttu-id="94047-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="94047-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="94047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94047-102">SYNOPSIS</span></span>
<span data-ttu-id="94047-103">키 자격 증명 모음 관리 Azure 저장소 계정의 지정 된 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94047-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94047-104">SYNTAX</span></span>

### <span data-ttu-id="94047-105">ByDefinitionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="94047-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94047-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="94047-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94047-107">설명은</span><span class="sxs-lookup"><span data-stu-id="94047-107">DESCRIPTION</span></span>
<span data-ttu-id="94047-108">키 보관소의 지정 된 키를 관리 하는 Azure Storage 계정을 다시 생성 하 고 키를 활성 키로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="94047-109">키 보관소는 키를 다시 생성 하기 위해 Azure Resource Manager에 대 한 통화를 프록시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="94047-110">호출자는 지정 된 Azure Storage 계정에서 키를 다시 생성 하는 권한을 플랫폼이 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="94047-111">예제의</span><span class="sxs-lookup"><span data-stu-id="94047-111">EXAMPLES</span></span>

### <span data-ttu-id="94047-112">예제 1: 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="94047-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

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

<span data-ttu-id="94047-113">계정 ' mystorageaccount '의 ' key1 '을 다시 생성 하 고 ' key1 '을 키 보관소 관리 Azure 저장소 계정의 활성으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="94047-114">변수</span><span class="sxs-lookup"><span data-stu-id="94047-114">PARAMETERS</span></span>

### <span data-ttu-id="94047-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="94047-115">-AccountName</span></span>
<span data-ttu-id="94047-116">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94047-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="94047-117">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="94047-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94047-118">-DefaultProfile</span></span>
<span data-ttu-id="94047-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="94047-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94047-120">-Force</span><span class="sxs-lookup"><span data-stu-id="94047-120">-Force</span></span>
<span data-ttu-id="94047-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94047-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94047-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94047-122">-InputObject</span></span>
<span data-ttu-id="94047-123">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94047-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="94047-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="94047-124">-KeyName</span></span>
<span data-ttu-id="94047-125">다시 생성 하 고 활성 상태로 만들 저장소 계정 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94047-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="94047-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94047-126">-PassThru</span></span>
<span data-ttu-id="94047-127">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94047-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="94047-128">이 스위치가 지정 된 경우 cmdlet은 삭제 된 관리 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="94047-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="94047-129">-VaultName</span></span>
<span data-ttu-id="94047-130">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="94047-130">Vault name.</span></span>
<span data-ttu-id="94047-131">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="94047-132">-확인</span><span class="sxs-lookup"><span data-stu-id="94047-132">-Confirm</span></span>
<span data-ttu-id="94047-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94047-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94047-134">-WhatIf</span></span>
<span data-ttu-id="94047-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="94047-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94047-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94047-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94047-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94047-137">CommonParameters</span></span>
<span data-ttu-id="94047-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94047-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94047-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94047-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94047-140">입력</span><span class="sxs-lookup"><span data-stu-id="94047-140">INPUTS</span></span>

### <span data-ttu-id="94047-141">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="94047-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="94047-142">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94047-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="94047-143">출력</span><span class="sxs-lookup"><span data-stu-id="94047-143">OUTPUTS</span></span>

### <span data-ttu-id="94047-144">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94047-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="94047-145">상속자</span><span class="sxs-lookup"><span data-stu-id="94047-145">NOTES</span></span>

## <span data-ttu-id="94047-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94047-146">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

