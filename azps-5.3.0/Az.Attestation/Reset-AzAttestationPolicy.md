---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381088"
---
# <span data-ttu-id="36af4-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="36af4-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="36af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36af4-102">SYNOPSIS</span></span>
<span data-ttu-id="36af4-103">Azure Attestationn의 테넌트에서 정책을 다시 설정합니다.}</span><span class="sxs-lookup"><span data-stu-id="36af4-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="36af4-104">구문</span><span class="sxs-lookup"><span data-stu-id="36af4-104">SYNTAX</span></span>

### <span data-ttu-id="36af4-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36af4-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36af4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36af4-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36af4-107">설명</span><span class="sxs-lookup"><span data-stu-id="36af4-107">DESCRIPTION</span></span>
<span data-ttu-id="36af4-108">이 Reset-AzAttestationPolicy cmdlet은 Azure Attestation의 테넌트에서 사용자 정의 평가 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="36af4-109">예제</span><span class="sxs-lookup"><span data-stu-id="36af4-109">EXAMPLES</span></span>

### <span data-ttu-id="36af4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="36af4-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="36af4-111">Tee 형식 *SgxEnclave에* 대한 Attestation Provider *pshtest의* 기본값으로 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="36af4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="36af4-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="36af4-113">Attestation Provider *pshtest가* 격리된 트러스트 모델을 사용하도록 구성된 경우 서명된 정책을 포함하여 Tee 형식 *SgxEnclave에* 대한 기본값으로 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="36af4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36af4-114">PARAMETERS</span></span>

### <span data-ttu-id="36af4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36af4-115">-DefaultProfile</span></span>
<span data-ttu-id="36af4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36af4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="36af4-117">-Name</span></span>
<span data-ttu-id="36af4-118">테넌트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="36af4-119">이 cmdlet은 이 매개 변수가 지정하는 테넌트에 대한 설명 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="36af4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36af4-120">-PassThru</span></span>
<span data-ttu-id="36af4-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="36af4-122">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36af4-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="36af4-123">-Policy</span></span>
<span data-ttu-id="36af4-124">재설정할 정책 문서를 설명하는 JSON 웹 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36af4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36af4-125">-ResourceGroupName</span></span>
<span data-ttu-id="36af4-126">등록 공급자의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="36af4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36af4-127">-ResourceId</span></span>
<span data-ttu-id="36af4-128">등록 공급자의 ResourceID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="36af4-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="36af4-129">-Tee</span></span>
<span data-ttu-id="36af4-130">신뢰할 수 있는 실행 환경의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="36af4-131">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave의 네 가지 유형의 환경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="36af4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36af4-132">-Confirm</span></span>
<span data-ttu-id="36af4-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36af4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36af4-134">-WhatIf</span></span>
<span data-ttu-id="36af4-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="36af4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36af4-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36af4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36af4-137">CommonParameters</span></span>
<span data-ttu-id="36af4-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36af4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36af4-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36af4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36af4-140">입력</span><span class="sxs-lookup"><span data-stu-id="36af4-140">INPUTS</span></span>

### <span data-ttu-id="36af4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="36af4-141">System.String</span></span>

## <span data-ttu-id="36af4-142">출력</span><span class="sxs-lookup"><span data-stu-id="36af4-142">OUTPUTS</span></span>

### <span data-ttu-id="36af4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36af4-143">System.Boolean</span></span>

## <span data-ttu-id="36af4-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36af4-144">NOTES</span></span>

## <span data-ttu-id="36af4-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36af4-145">RELATED LINKS</span></span>
