---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399093"
---
# <span data-ttu-id="813a4-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="813a4-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="813a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="813a4-102">SYNOPSIS</span></span>
<span data-ttu-id="813a4-103">키 자격 증명 모음에서 삭제된 비밀을 활성 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="813a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="813a4-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="813a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="813a4-105">DESCRIPTION</span></span>
<span data-ttu-id="813a4-106">**Undo-AzKeyVaultSecretRemoval** cmdlet은 이전에 삭제된 비밀을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="813a4-107">복구된 비밀은 활성화됩니다. 모든 일반 비밀 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="813a4-108">이 작업을 수행하려면 호출자에 '복구' 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="813a4-109">예제</span><span class="sxs-lookup"><span data-stu-id="813a4-109">EXAMPLES</span></span>

### <span data-ttu-id="813a4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="813a4-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="813a4-111">이 명령은 이전에 삭제된 'MySecret' 비밀을 활성 및 사용 가능한 상태로 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="813a4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="813a4-112">PARAMETERS</span></span>

### <span data-ttu-id="813a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813a4-113">-DefaultProfile</span></span>
<span data-ttu-id="813a4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="813a4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813a4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="813a4-115">-Name</span></span>
<span data-ttu-id="813a4-116">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-116">Secret name.</span></span>
<span data-ttu-id="813a4-117">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름에서 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813a4-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="813a4-118">-VaultName</span></span>
<span data-ttu-id="813a4-119">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-119">Vault name.</span></span>
<span data-ttu-id="813a4-120">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813a4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="813a4-121">-Confirm</span></span>
<span data-ttu-id="813a4-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="813a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813a4-123">-WhatIf</span></span>
<span data-ttu-id="813a4-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="813a4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="813a4-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="813a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813a4-126">CommonParameters</span></span>
<span data-ttu-id="813a4-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="813a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813a4-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="813a4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813a4-129">입력</span><span class="sxs-lookup"><span data-stu-id="813a4-129">INPUTS</span></span>

### <span data-ttu-id="813a4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="813a4-130">System.String</span></span>

## <span data-ttu-id="813a4-131">출력</span><span class="sxs-lookup"><span data-stu-id="813a4-131">OUTPUTS</span></span>

### <span data-ttu-id="813a4-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="813a4-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="813a4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="813a4-133">NOTES</span></span>

## <span data-ttu-id="813a4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="813a4-134">RELATED LINKS</span></span>

[<span data-ttu-id="813a4-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="813a4-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="813a4-136">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="813a4-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
