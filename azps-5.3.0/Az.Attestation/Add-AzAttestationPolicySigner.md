---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381200"
---
# <span data-ttu-id="14650-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="14650-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="14650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14650-102">SYNOPSIS</span></span>
<span data-ttu-id="14650-103">Azure Attestation에서 테넌트에 대한 신뢰할 수 있는 정책 서명자 추가</span><span class="sxs-lookup"><span data-stu-id="14650-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="14650-104">구문</span><span class="sxs-lookup"><span data-stu-id="14650-104">SYNTAX</span></span>

### <span data-ttu-id="14650-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14650-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14650-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14650-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14650-107">설명</span><span class="sxs-lookup"><span data-stu-id="14650-107">DESCRIPTION</span></span>
<span data-ttu-id="14650-108">Add-AzAttestationPolicySigner cmdlet은 Azure Attestation에서 테넌트에 대한 신뢰할 수 있는 정책 서명자 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="14650-109">예제</span><span class="sxs-lookup"><span data-stu-id="14650-109">EXAMPLES</span></span>

### <span data-ttu-id="14650-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="14650-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="14650-111">*pshtest라는* Atteestation Provider에 신뢰할 수 있는 서명자를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="14650-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14650-112">PARAMETERS</span></span>

### <span data-ttu-id="14650-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14650-113">-DefaultProfile</span></span>
<span data-ttu-id="14650-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14650-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14650-115">-Name</span><span class="sxs-lookup"><span data-stu-id="14650-115">-Name</span></span>
<span data-ttu-id="14650-116">등록 공급자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14650-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14650-117">-ResourceGroupName</span></span>
<span data-ttu-id="14650-118">등록 공급자의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14650-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14650-119">-ResourceId</span></span>
<span data-ttu-id="14650-120">등록 공급자의 ResourceID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14650-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="14650-121">-Signer</span></span>
<span data-ttu-id="14650-122">추가할 신뢰할 수 있는 새 서명 키가 포함된 RFC7517 JSON 웹 키 값인 "maa-policyCertificate"라는 클레임이 포함된 RFC7519 JSON 웹 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="14650-123">RFC7519 JWT는 기존의 신뢰할 수 있는 서명 키 중 하나를 사용하여 서명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14650-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14650-124">-Confirm</span></span>
<span data-ttu-id="14650-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="14650-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14650-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14650-126">-WhatIf</span></span>
<span data-ttu-id="14650-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="14650-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14650-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14650-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14650-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14650-129">CommonParameters</span></span>
<span data-ttu-id="14650-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14650-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14650-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14650-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14650-132">입력</span><span class="sxs-lookup"><span data-stu-id="14650-132">INPUTS</span></span>

### <span data-ttu-id="14650-133">System.String</span><span class="sxs-lookup"><span data-stu-id="14650-133">System.String</span></span>

## <span data-ttu-id="14650-134">출력</span><span class="sxs-lookup"><span data-stu-id="14650-134">OUTPUTS</span></span>

### <span data-ttu-id="14650-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="14650-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="14650-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14650-136">NOTES</span></span>

## <span data-ttu-id="14650-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14650-137">RELATED LINKS</span></span>
