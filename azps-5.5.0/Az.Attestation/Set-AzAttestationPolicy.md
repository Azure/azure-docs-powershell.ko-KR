---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182196"
---
# <span data-ttu-id="f4bda-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="f4bda-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="f4bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4bda-102">SYNOPSIS</span></span>
<span data-ttu-id="f4bda-103">Azure Attestationn의 테넌트에서 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="f4bda-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4bda-104">SYNTAX</span></span>

### <span data-ttu-id="f4bda-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4bda-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4bda-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4bda-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4bda-107">설명</span><span class="sxs-lookup"><span data-stu-id="f4bda-107">DESCRIPTION</span></span>
<span data-ttu-id="f4bda-108">이 Set-AzAttestationPolicy cmdlet은 Azure Attestation의 테넌트에서 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f4bda-109">예제</span><span class="sxs-lookup"><span data-stu-id="f4bda-109">EXAMPLES</span></span>

### <span data-ttu-id="f4bda-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4bda-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="f4bda-111">텍스트 정책 형식(기본값)을 사용하여 TEE 형식 *SgxEnclave* for Attest Provider *pshtest에* 대해 사용자 정의 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="f4bda-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4bda-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="f4bda-113">JWT 정책 형식을 사용하여 TEE 형식 *SgxEnclave* for Attest Provider *pshtest에* 대해 사용자 정의 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="f4bda-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4bda-114">PARAMETERS</span></span>

### <span data-ttu-id="f4bda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4bda-115">-DefaultProfile</span></span>
<span data-ttu-id="f4bda-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4bda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f4bda-117">-Name</span></span>
<span data-ttu-id="f4bda-118">테넌트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="f4bda-119">이 cmdlet은 이 매개 변수가 지정하는 테넌트에 대한 설명 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4bda-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4bda-120">-PassThru</span></span>
<span data-ttu-id="f4bda-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f4bda-122">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f4bda-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="f4bda-123">-Policy</span></span>
<span data-ttu-id="f4bda-124">설정할 정책 문서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="f4bda-125">정책 형식은 텍스트 또는 JWT(JSON 웹 토큰)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="f4bda-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="f4bda-126">-PolicyFormat</span></span>
<span data-ttu-id="f4bda-127">정책의 형식(텍스트 또는 JWT(JSON 웹 토큰)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="f4bda-128">기본 정책 형식은 Text입니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="f4bda-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4bda-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4bda-130">등록 공급자의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="f4bda-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4bda-131">-ResourceId</span></span>
<span data-ttu-id="f4bda-132">등록 공급자의 ResourceID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="f4bda-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="f4bda-133">-Tee</span></span>
<span data-ttu-id="f4bda-134">신뢰할 수 있는 실행 환경의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="f4bda-135">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave의 네 가지 유형의 환경이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="f4bda-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4bda-136">-Confirm</span></span>
<span data-ttu-id="f4bda-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4bda-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4bda-138">-WhatIf</span></span>
<span data-ttu-id="f4bda-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f4bda-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4bda-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4bda-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4bda-141">CommonParameters</span></span>
<span data-ttu-id="f4bda-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4bda-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4bda-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4bda-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4bda-144">입력</span><span class="sxs-lookup"><span data-stu-id="f4bda-144">INPUTS</span></span>

### <span data-ttu-id="f4bda-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f4bda-145">System.String</span></span>

## <span data-ttu-id="f4bda-146">출력</span><span class="sxs-lookup"><span data-stu-id="f4bda-146">OUTPUTS</span></span>

### <span data-ttu-id="f4bda-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f4bda-147">System.String</span></span>

## <span data-ttu-id="f4bda-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4bda-148">NOTES</span></span>

## <span data-ttu-id="f4bda-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4bda-149">RELATED LINKS</span></span>
