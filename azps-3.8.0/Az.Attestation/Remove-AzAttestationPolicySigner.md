---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: 8f06713ab61ca423fee031f8dca9df90b941ed32
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042736"
---
# <span data-ttu-id="84cf3-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="84cf3-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="84cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="84cf3-103">Azure 증명에서 테 넌 트에 대해 신뢰할 수 있는 정책 서명자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="84cf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84cf3-104">SYNTAX</span></span>

### <span data-ttu-id="84cf3-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84cf3-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84cf3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84cf3-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84cf3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="84cf3-107">DESCRIPTION</span></span>
<span data-ttu-id="84cf3-108">Remove-AzAttestationPolicySigner cmdlet은 Azure 증명의 테 넌 트에 대해 신뢰할 수 있는 정책 서명자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="84cf3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="84cf3-109">EXAMPLES</span></span>

### <span data-ttu-id="84cf3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="84cf3-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="84cf3-111">*Pshtest* 라는 증명 공급자에 대해 신뢰할 수 있는 서명자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="84cf3-112">변수</span><span class="sxs-lookup"><span data-stu-id="84cf3-112">PARAMETERS</span></span>

### <span data-ttu-id="84cf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cf3-113">-DefaultProfile</span></span>
<span data-ttu-id="84cf3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84cf3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="84cf3-115">-Name</span></span>
<span data-ttu-id="84cf3-116">증명 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="84cf3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84cf3-117">-ResourceGroupName</span></span>
<span data-ttu-id="84cf3-118">증명 공급자의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="84cf3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84cf3-119">-ResourceId</span></span>
<span data-ttu-id="84cf3-120">증명 공급자의 ResourceID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="84cf3-121">-서명자</span><span class="sxs-lookup"><span data-stu-id="84cf3-121">-Signer</span></span>
<span data-ttu-id="84cf3-122">해당 값이 제거할 신뢰할 수 있는 서명 키를 포함 하는 RFC7517 JSON 웹 키인 ".aas-policyCertificate" 라는 클레임을 포함 하는 RFC7519 JSON 웹 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-122">Specifies the RFC7519 JSON Web Token containing a claim named "aas-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="84cf3-123">RFC7519 JWT는 기존 신뢰할 수 있는 서명 키 중 하나를 사용 하 여 서명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="84cf3-124">-확인</span><span class="sxs-lookup"><span data-stu-id="84cf3-124">-Confirm</span></span>
<span data-ttu-id="84cf3-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84cf3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84cf3-126">-WhatIf</span></span>
<span data-ttu-id="84cf3-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84cf3-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84cf3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cf3-129">CommonParameters</span></span>
<span data-ttu-id="84cf3-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84cf3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cf3-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="84cf3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cf3-132">입력</span><span class="sxs-lookup"><span data-stu-id="84cf3-132">INPUTS</span></span>

### <span data-ttu-id="84cf3-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84cf3-133">System.String</span></span>

## <span data-ttu-id="84cf3-134">출력</span><span class="sxs-lookup"><span data-stu-id="84cf3-134">OUTPUTS</span></span>

### <span data-ttu-id="84cf3-135">PSPolicySigners/. i m m</span><span class="sxs-lookup"><span data-stu-id="84cf3-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="84cf3-136">상속자</span><span class="sxs-lookup"><span data-stu-id="84cf3-136">NOTES</span></span>

## <span data-ttu-id="84cf3-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84cf3-137">RELATED LINKS</span></span>
