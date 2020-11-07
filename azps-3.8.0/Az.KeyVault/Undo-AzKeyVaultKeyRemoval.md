---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878281"
---
# <span data-ttu-id="4b31f-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="4b31f-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="4b31f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b31f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b31f-103">키 자격 증명 모음에서 삭제 된 키를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="4b31f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b31f-104">SYNTAX</span></span>

### <span data-ttu-id="4b31f-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b31f-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b31f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4b31f-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b31f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4b31f-107">DESCRIPTION</span></span>
<span data-ttu-id="4b31f-108">**AzKeyVaultKeyRemoval** cmdlet은 이전에 삭제 된 키를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="4b31f-109">복구 된 키는 활성화 되며 모든 일반 키 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="4b31f-110">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4b31f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4b31f-111">EXAMPLES</span></span>

### <span data-ttu-id="4b31f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b31f-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

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

<span data-ttu-id="4b31f-113">이 명령을 사용 하면 이전에 삭제 된 ' MyKey ' 키가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4b31f-114">변수</span><span class="sxs-lookup"><span data-stu-id="4b31f-114">PARAMETERS</span></span>

### <span data-ttu-id="4b31f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b31f-115">-DefaultProfile</span></span>
<span data-ttu-id="4b31f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b31f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b31f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b31f-117">-InputObject</span></span>
<span data-ttu-id="4b31f-118">삭제 된 키 개체</span><span class="sxs-lookup"><span data-stu-id="4b31f-118">Deleted key object</span></span>

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

### <span data-ttu-id="4b31f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4b31f-119">-Name</span></span>
<span data-ttu-id="4b31f-120">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-120">Key name.</span></span>
<span data-ttu-id="4b31f-121">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="4b31f-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4b31f-122">-VaultName</span></span>
<span data-ttu-id="4b31f-123">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="4b31f-123">Vault name.</span></span>
<span data-ttu-id="4b31f-124">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4b31f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="4b31f-125">-Confirm</span></span>
<span data-ttu-id="4b31f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b31f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b31f-127">-WhatIf</span></span>
<span data-ttu-id="4b31f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b31f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b31f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b31f-130">CommonParameters</span></span>
<span data-ttu-id="4b31f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b31f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b31f-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b31f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b31f-133">입력</span><span class="sxs-lookup"><span data-stu-id="4b31f-133">INPUTS</span></span>

### <span data-ttu-id="4b31f-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4b31f-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="4b31f-135">출력</span><span class="sxs-lookup"><span data-stu-id="4b31f-135">OUTPUTS</span></span>

### <span data-ttu-id="4b31f-136">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4b31f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="4b31f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4b31f-137">NOTES</span></span>

## <span data-ttu-id="4b31f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b31f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4b31f-139">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4b31f-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="4b31f-140">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4b31f-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="4b31f-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4b31f-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

