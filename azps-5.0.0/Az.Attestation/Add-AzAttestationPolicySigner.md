---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308588"
---
# <span data-ttu-id="c42b1-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="c42b1-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="c42b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c42b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c42b1-103">Azure 증명에 테 넌 트에 대해 신뢰할 수 있는 정책 서명자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="c42b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c42b1-104">SYNTAX</span></span>

### <span data-ttu-id="c42b1-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c42b1-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c42b1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c42b1-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c42b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c42b1-107">DESCRIPTION</span></span>
<span data-ttu-id="c42b1-108">Add-AzAttestationPolicySigner cmdlet은 Azure 증명에 테 넌 트에 대해 신뢰할 수 있는 정책 서명자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="c42b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c42b1-109">EXAMPLES</span></span>

### <span data-ttu-id="c42b1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c42b1-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="c42b1-111">*Pshtest* 라는 Atteestation 공급자에 대해 신뢰할 수 있는 서명자를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="c42b1-112">변수</span><span class="sxs-lookup"><span data-stu-id="c42b1-112">PARAMETERS</span></span>

### <span data-ttu-id="c42b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42b1-113">-DefaultProfile</span></span>
<span data-ttu-id="c42b1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42b1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c42b1-115">-Name</span></span>
<span data-ttu-id="c42b1-116">증명 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="c42b1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42b1-117">-ResourceGroupName</span></span>
<span data-ttu-id="c42b1-118">증명 공급자의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="c42b1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c42b1-119">-ResourceId</span></span>
<span data-ttu-id="c42b1-120">증명 공급자의 ResourceID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="c42b1-121">-서명자</span><span class="sxs-lookup"><span data-stu-id="c42b1-121">-Signer</span></span>
<span data-ttu-id="c42b1-122">해당 값이 추가할 새 신뢰할 수 있는 서명 키를 포함 하는 RFC7517 JSON 웹 키인 "maa-policyCertificate" 라는 클레임을 포함 하는 RFC7519 JSON 웹 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="c42b1-123">RFC7519 JWT는 기존 신뢰할 수 있는 서명 키 중 하나를 사용 하 여 서명 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="c42b1-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c42b1-124">-Confirm</span></span>
<span data-ttu-id="c42b1-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c42b1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42b1-126">-WhatIf</span></span>
<span data-ttu-id="c42b1-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c42b1-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c42b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42b1-129">CommonParameters</span></span>
<span data-ttu-id="c42b1-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42b1-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c42b1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42b1-132">입력</span><span class="sxs-lookup"><span data-stu-id="c42b1-132">INPUTS</span></span>

### <span data-ttu-id="c42b1-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c42b1-133">System.String</span></span>

## <span data-ttu-id="c42b1-134">출력</span><span class="sxs-lookup"><span data-stu-id="c42b1-134">OUTPUTS</span></span>

### <span data-ttu-id="c42b1-135">PSPolicySigners/. i m m</span><span class="sxs-lookup"><span data-stu-id="c42b1-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="c42b1-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c42b1-136">NOTES</span></span>

## <span data-ttu-id="c42b1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c42b1-137">RELATED LINKS</span></span>
