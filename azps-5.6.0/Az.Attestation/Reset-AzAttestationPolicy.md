---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: b628d93d44b863b4af05f09dd4d132ec986702e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966795"
---
# <span data-ttu-id="9b0da-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="9b0da-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="9b0da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b0da-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0da-103">Azure Attestationn.} 테넌트에서 정책을 재설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="9b0da-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b0da-104">SYNTAX</span></span>

### <span data-ttu-id="9b0da-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b0da-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b0da-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b0da-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b0da-107">설명</span><span class="sxs-lookup"><span data-stu-id="9b0da-107">DESCRIPTION</span></span>
<span data-ttu-id="9b0da-108">Reset-AzAttestationPolicy cmdlet은 Azure Attestation의 테넌트에서 정의된 사용자 평가 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="9b0da-109">예제</span><span class="sxs-lookup"><span data-stu-id="9b0da-109">EXAMPLES</span></span>

### <span data-ttu-id="9b0da-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b0da-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="9b0da-111">Tee 형식 *SgxEnclave에* 대한 Attestation 공급자 *pshtest의* 기본값으로 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="9b0da-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9b0da-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="9b0da-113">격리된 트러스트 모델을 사용하도록 Attest 공급자 *pshtest가* 구성된 경우 서명된 정책을 포함하여 Tee 형식 *SgxEnclave의* 기본값으로 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="9b0da-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b0da-114">PARAMETERS</span></span>

### <span data-ttu-id="9b0da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0da-115">-DefaultProfile</span></span>
<span data-ttu-id="9b0da-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b0da-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9b0da-117">-Name</span></span>
<span data-ttu-id="9b0da-118">테넌트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="9b0da-119">이 cmdlet은 이 매개 변수가 지정하는 테넌트에 대한 설명 정책을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b0da-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b0da-120">-PassThru</span></span>
<span data-ttu-id="9b0da-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9b0da-122">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9b0da-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="9b0da-123">-Policy</span></span>
<span data-ttu-id="9b0da-124">다시 설정할 정책 문서를 설명하는 JSON 웹 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="9b0da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b0da-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b0da-126">토의 공급자의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="9b0da-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b0da-127">-ResourceId</span></span>
<span data-ttu-id="9b0da-128">토의 공급자의 ResourceID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="9b0da-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="9b0da-129">-Tee</span></span>
<span data-ttu-id="9b0da-130">신뢰할 수 있는 실행 환경 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="9b0da-131">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave의 네 가지 유형의 환경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="9b0da-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9b0da-132">-Confirm</span></span>
<span data-ttu-id="9b0da-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b0da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b0da-134">-WhatIf</span></span>
<span data-ttu-id="9b0da-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b0da-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b0da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0da-137">CommonParameters</span></span>
<span data-ttu-id="9b0da-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b0da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0da-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b0da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0da-140">입력</span><span class="sxs-lookup"><span data-stu-id="9b0da-140">INPUTS</span></span>

### <span data-ttu-id="9b0da-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b0da-141">System.String</span></span>

## <span data-ttu-id="9b0da-142">출력</span><span class="sxs-lookup"><span data-stu-id="9b0da-142">OUTPUTS</span></span>

### <span data-ttu-id="9b0da-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b0da-143">System.Boolean</span></span>

## <span data-ttu-id="9b0da-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b0da-144">NOTES</span></span>

## <span data-ttu-id="9b0da-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b0da-145">RELATED LINKS</span></span>
