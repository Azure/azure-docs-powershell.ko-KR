---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultmanagedstorageaccountremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultManagedStorageAccountRemoval.md
ms.openlocfilehash: a8e8bb9a4a006c30275f1de959181ad640a04f88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711367"
---
# <span data-ttu-id="ae8d0-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="ae8d0-101">Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

## <span data-ttu-id="ae8d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae8d0-103">이전에 삭제 된 KeyVault 관리 저장소 계정을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-103">Recovers a previously deleted KeyVault-managed storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae8d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae8d0-104">SYNTAX</span></span>

### <span data-ttu-id="ae8d0-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae8d0-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae8d0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae8d0-106">InputObject</span></span>
```
Undo-AzureKeyVaultManagedStorageAccountRemoval
 [-InputObject] <PSDeletedKeyVaultManagedStorageAccountIdentityItem> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae8d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ae8d0-107">DESCRIPTION</span></span>
<span data-ttu-id="ae8d0-108">**AzureKeyVaultManagedStorageAccountRemoval** 명령은이 자격 증명 모음에 대 한 소프트 삭제를 사용 하도록 설정 된 경우 이전에 삭제 된 관리 저장소 계정을 복구 하 고 복구 간격 중에 복구 시도가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-108">The **Undo-AzureKeyVaultManagedStorageAccountRemoval** command recovers a previously deleted managed storage account, provided that soft delete is enabled for this vault, and that the attempt to recover occurs during the recovery interval.</span></span>

## <span data-ttu-id="ae8d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ae8d0-109">EXAMPLES</span></span>

### <span data-ttu-id="ae8d0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae8d0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName myVault -Name myAccount -InRemovedState
PS C:\> Undo-AzureKeyVaultManagedStorageAccountRemoval -VaultName myVault -Name myAccount

Id                  : https://myvault.vault.azure.net:443/storage/myaccount
Vault Name          : myVault
AccountName         : myAccount
Account Resource Id : /subscriptions/8bc48661-1801-4b7a-8ca1-6a3cadfb4870/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/myaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="ae8d0-111">이 명령 순서는 지정 된 저장소 계정이 자격 증명 모음에 삭제 됨 상태 인지 여부를 결정 합니다. 후속 명령은 삭제 된 저장소 계정을 복구 하 여 활성 상태로 다시 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-111">This sequence of commands determines whether the specified storage account exists in the vault in a deleted state; the subsequent command recovers the deleted storage account, bringing it back into an active state.</span></span>

## <span data-ttu-id="ae8d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="ae8d0-112">PARAMETERS</span></span>

### <span data-ttu-id="ae8d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae8d0-113">-DefaultProfile</span></span>
<span data-ttu-id="ae8d0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae8d0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae8d0-115">-InputObject</span></span>
<span data-ttu-id="ae8d0-116">관리 되는 저장소 계정 개체 삭제 됨</span><span class="sxs-lookup"><span data-stu-id="ae8d0-116">Deleted Managed Storage Account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ae8d0-117">-Name</span></span>
<span data-ttu-id="ae8d0-118">KeyVault 관리 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-118">Name of the KeyVault managed storage account.</span></span>
<span data-ttu-id="ae8d0-119">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리 되는 저장소 계정의 이름에 대 한 대상의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-119">Cmdlet constructs the FQDN of the target from vault name, currently selected environment and the name of the managed storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d0-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae8d0-120">-VaultName</span></span>
<span data-ttu-id="ae8d0-121">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="ae8d0-121">Vault name.</span></span>
<span data-ttu-id="ae8d0-122">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-122">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae8d0-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ae8d0-123">-Confirm</span></span>
<span data-ttu-id="ae8d0-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae8d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae8d0-125">-WhatIf</span></span>
<span data-ttu-id="ae8d0-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae8d0-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae8d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae8d0-128">CommonParameters</span></span>
<span data-ttu-id="ae8d0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae8d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae8d0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae8d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae8d0-131">입력</span><span class="sxs-lookup"><span data-stu-id="ae8d0-131">INPUTS</span></span>

### <span data-ttu-id="ae8d0-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ae8d0-132">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="ae8d0-133">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae8d0-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ae8d0-134">출력</span><span class="sxs-lookup"><span data-stu-id="ae8d0-134">OUTPUTS</span></span>

### <span data-ttu-id="ae8d0-135">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae8d0-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ae8d0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ae8d0-136">NOTES</span></span>

## <span data-ttu-id="ae8d0-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae8d0-137">RELATED LINKS</span></span>
