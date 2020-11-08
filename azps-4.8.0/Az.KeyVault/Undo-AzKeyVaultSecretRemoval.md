---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056306"
---
# <span data-ttu-id="54a98-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="54a98-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="54a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a98-102">SYNOPSIS</span></span>
<span data-ttu-id="54a98-103">키 자격 증명 모음에서 삭제 된 비밀을 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="54a98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54a98-104">SYNTAX</span></span>

### <span data-ttu-id="54a98-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="54a98-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54a98-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="54a98-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54a98-107">설명은</span><span class="sxs-lookup"><span data-stu-id="54a98-107">DESCRIPTION</span></span>
<span data-ttu-id="54a98-108">**AzKeyVaultSecretRemoval** cmdlet은 이전에 삭제 된 비밀을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="54a98-109">복구 된 비밀은 활성 상태가 되며, 모든 일반 비밀 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="54a98-110">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="54a98-111">예제의</span><span class="sxs-lookup"><span data-stu-id="54a98-111">EXAMPLES</span></span>

### <span data-ttu-id="54a98-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="54a98-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="54a98-113">이 명령을 사용 하면 이전에 삭제 된 비밀 ' MySecret '가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="54a98-114">변수</span><span class="sxs-lookup"><span data-stu-id="54a98-114">PARAMETERS</span></span>

### <span data-ttu-id="54a98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a98-115">-DefaultProfile</span></span>
<span data-ttu-id="54a98-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54a98-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54a98-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54a98-117">-InputObject</span></span>
<span data-ttu-id="54a98-118">비밀 개체 삭제 됨</span><span class="sxs-lookup"><span data-stu-id="54a98-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54a98-119">-이름</span><span class="sxs-lookup"><span data-stu-id="54a98-119">-Name</span></span>
<span data-ttu-id="54a98-120">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="54a98-120">Secret name.</span></span>
<span data-ttu-id="54a98-121">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54a98-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54a98-122">-VaultName</span></span>
<span data-ttu-id="54a98-123">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="54a98-123">Vault name.</span></span>
<span data-ttu-id="54a98-124">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="54a98-125">-확인</span><span class="sxs-lookup"><span data-stu-id="54a98-125">-Confirm</span></span>
<span data-ttu-id="54a98-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54a98-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a98-127">-WhatIf</span></span>
<span data-ttu-id="54a98-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54a98-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54a98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a98-130">CommonParameters</span></span>
<span data-ttu-id="54a98-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54a98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a98-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54a98-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a98-133">입력</span><span class="sxs-lookup"><span data-stu-id="54a98-133">INPUTS</span></span>

### <span data-ttu-id="54a98-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="54a98-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="54a98-135">출력</span><span class="sxs-lookup"><span data-stu-id="54a98-135">OUTPUTS</span></span>

### <span data-ttu-id="54a98-136">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54a98-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="54a98-137">상속자</span><span class="sxs-lookup"><span data-stu-id="54a98-137">NOTES</span></span>

## <span data-ttu-id="54a98-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54a98-138">RELATED LINKS</span></span>

[<span data-ttu-id="54a98-139">제거-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54a98-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="54a98-140">추가-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54a98-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="54a98-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54a98-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
