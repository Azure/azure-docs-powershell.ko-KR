---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: fdd62a78b9d75ef222dc9f41f2c791afadfad9b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381095"
---
# <span data-ttu-id="2c496-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="2c496-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="2c496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c496-102">SYNOPSIS</span></span>
<span data-ttu-id="2c496-103">Azure Attestation에서 테넌트에 대한 신뢰할 수 있는 정책 서명자 제거</span><span class="sxs-lookup"><span data-stu-id="2c496-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="2c496-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c496-104">SYNTAX</span></span>

### <span data-ttu-id="2c496-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c496-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c496-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c496-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c496-107">설명</span><span class="sxs-lookup"><span data-stu-id="2c496-107">DESCRIPTION</span></span>
<span data-ttu-id="2c496-108">이 Remove-AzAttestationPolicySigner cmdlet은 Azure Attestation에서 테넌트에 대한 신뢰할 수 있는 정책 서명기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="2c496-109">예제</span><span class="sxs-lookup"><span data-stu-id="2c496-109">EXAMPLES</span></span>

### <span data-ttu-id="2c496-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c496-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="2c496-111">*pshtest라는* 명명된 Attest 공급자에 대한 신뢰할 수 있는 서명자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="2c496-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c496-112">PARAMETERS</span></span>

### <span data-ttu-id="2c496-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c496-113">-DefaultProfile</span></span>
<span data-ttu-id="2c496-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c496-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2c496-115">-Name</span></span>
<span data-ttu-id="2c496-116">등록 공급자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="2c496-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c496-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c496-118">등록 공급자의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="2c496-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c496-119">-ResourceId</span></span>
<span data-ttu-id="2c496-120">등록 공급자의 ResourceID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="2c496-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="2c496-121">-Signer</span></span>
<span data-ttu-id="2c496-122">해당 값이 제거할 신뢰할 수 있는 서명 키를 포함하는 RFC7517 JSON 웹 키인 "maa-policyCertificate"라는 클레임이 포함된 RFC7519 JSON 웹 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="2c496-123">RFC7519 JWT는 기존의 신뢰할 수 있는 서명 키 중 하나를 사용하여 서명해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="2c496-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c496-124">-Confirm</span></span>
<span data-ttu-id="2c496-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c496-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c496-126">-WhatIf</span></span>
<span data-ttu-id="2c496-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c496-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c496-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c496-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c496-129">CommonParameters</span></span>
<span data-ttu-id="2c496-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c496-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c496-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c496-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c496-132">입력</span><span class="sxs-lookup"><span data-stu-id="2c496-132">INPUTS</span></span>

### <span data-ttu-id="2c496-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2c496-133">System.String</span></span>

## <span data-ttu-id="2c496-134">출력</span><span class="sxs-lookup"><span data-stu-id="2c496-134">OUTPUTS</span></span>

### <span data-ttu-id="2c496-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="2c496-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="2c496-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c496-136">NOTES</span></span>

## <span data-ttu-id="2c496-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c496-137">RELATED LINKS</span></span>
