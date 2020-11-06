---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 6de9fecc4b9576f9d69ddc1f963ae537f4422371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535864"
---
# <span data-ttu-id="d5479-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d5479-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="d5479-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5479-102">SYNOPSIS</span></span>
<span data-ttu-id="d5479-103">키 자격 증명 모음에서 삭제 된 키를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5479-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5479-104">SYNTAX</span></span>

### <span data-ttu-id="d5479-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5479-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5479-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d5479-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5479-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5479-107">DESCRIPTION</span></span>
<span data-ttu-id="d5479-108">**AzureKeyVaultKeyRemoval** cmdlet은 이전에 삭제 된 키를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="d5479-109">복구 된 키는 활성화 되며 모든 일반 키 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="d5479-110">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d5479-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d5479-111">EXAMPLES</span></span>

### <span data-ttu-id="d5479-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5479-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d5479-113">이 명령을 사용 하면 이전에 삭제 된 ' MyKey ' 키가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d5479-114">변수</span><span class="sxs-lookup"><span data-stu-id="d5479-114">PARAMETERS</span></span>

### <span data-ttu-id="d5479-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5479-115">-DefaultProfile</span></span>
<span data-ttu-id="d5479-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5479-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5479-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5479-117">-InputObject</span></span>
<span data-ttu-id="d5479-118">삭제 된 키 개체</span><span class="sxs-lookup"><span data-stu-id="d5479-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5479-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d5479-119">-Name</span></span>
<span data-ttu-id="d5479-120">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-120">Key name.</span></span>
<span data-ttu-id="d5479-121">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5479-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d5479-122">-VaultName</span></span>
<span data-ttu-id="d5479-123">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="d5479-123">Vault name.</span></span>
<span data-ttu-id="d5479-124">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d5479-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d5479-125">-Confirm</span></span>
<span data-ttu-id="d5479-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5479-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5479-127">-WhatIf</span></span>
<span data-ttu-id="d5479-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5479-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5479-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5479-130">CommonParameters</span></span>
<span data-ttu-id="d5479-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5479-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5479-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5479-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5479-133">입력</span><span class="sxs-lookup"><span data-stu-id="d5479-133">INPUTS</span></span>

### <span data-ttu-id="d5479-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d5479-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="d5479-135">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5479-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d5479-136">출력</span><span class="sxs-lookup"><span data-stu-id="d5479-136">OUTPUTS</span></span>

### <span data-ttu-id="d5479-137">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d5479-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="d5479-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d5479-138">NOTES</span></span>

## <span data-ttu-id="d5479-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5479-139">RELATED LINKS</span></span>

[<span data-ttu-id="d5479-140">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d5479-140">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="d5479-141">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d5479-141">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="d5479-142">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d5479-142">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

