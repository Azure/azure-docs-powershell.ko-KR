---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: 07c62b1b106453cf9b19610867be39458943bcab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531707"
---
# <span data-ttu-id="52a67-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="52a67-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="52a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a67-102">SYNOPSIS</span></span>
<span data-ttu-id="52a67-103">키 자격 증명 모음에서 삭제 된 비밀을 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52a67-104">SYNTAX</span></span>

### <span data-ttu-id="52a67-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="52a67-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a67-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="52a67-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a67-107">설명은</span><span class="sxs-lookup"><span data-stu-id="52a67-107">DESCRIPTION</span></span>
<span data-ttu-id="52a67-108">**AzureKeyVaultSecretRemoval** cmdlet은 이전에 삭제 된 비밀을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="52a67-109">복구 된 비밀은 활성 상태가 되며, 모든 일반 비밀 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="52a67-110">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="52a67-111">예제의</span><span class="sxs-lookup"><span data-stu-id="52a67-111">EXAMPLES</span></span>

### <span data-ttu-id="52a67-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="52a67-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="52a67-113">이 명령을 사용 하면 이전에 삭제 된 비밀 ' MySecret '가 활성 및 사용 가능한 상태로 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="52a67-114">변수</span><span class="sxs-lookup"><span data-stu-id="52a67-114">PARAMETERS</span></span>

### <span data-ttu-id="52a67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a67-115">-DefaultProfile</span></span>
<span data-ttu-id="52a67-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="52a67-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52a67-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a67-117">-InputObject</span></span>
<span data-ttu-id="52a67-118">비밀 개체 삭제 됨</span><span class="sxs-lookup"><span data-stu-id="52a67-118">Deleted secret object</span></span>

```yaml
Type: PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a67-119">-이름</span><span class="sxs-lookup"><span data-stu-id="52a67-119">-Name</span></span>
<span data-ttu-id="52a67-120">비밀 이름.</span><span class="sxs-lookup"><span data-stu-id="52a67-120">Secret name.</span></span>
<span data-ttu-id="52a67-121">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a67-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="52a67-122">-VaultName</span></span>
<span data-ttu-id="52a67-123">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="52a67-123">Vault name.</span></span>
<span data-ttu-id="52a67-124">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a67-125">-확인</span><span class="sxs-lookup"><span data-stu-id="52a67-125">-Confirm</span></span>
<span data-ttu-id="52a67-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a67-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a67-127">-WhatIf</span></span>
<span data-ttu-id="52a67-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a67-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a67-130">CommonParameters</span></span>
<span data-ttu-id="52a67-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a67-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a67-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a67-133">입력</span><span class="sxs-lookup"><span data-stu-id="52a67-133">INPUTS</span></span>

### <span data-ttu-id="52a67-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52a67-134">System.String</span></span>

## <span data-ttu-id="52a67-135">출력</span><span class="sxs-lookup"><span data-stu-id="52a67-135">OUTPUTS</span></span>

### <span data-ttu-id="52a67-136">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="52a67-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="52a67-137">상속자</span><span class="sxs-lookup"><span data-stu-id="52a67-137">NOTES</span></span>

## <span data-ttu-id="52a67-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52a67-138">RELATED LINKS</span></span>

[<span data-ttu-id="52a67-139">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="52a67-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="52a67-140">추가-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="52a67-140">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="52a67-141">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="52a67-141">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
