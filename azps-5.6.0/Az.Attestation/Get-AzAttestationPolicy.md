---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 498777c6413cf4f80d32b50b4fb40da6216e43a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985413"
---
# <span data-ttu-id="cb3cf-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3cf-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="cb3cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cb3cf-103">Azure Attestation의 테넌트에서 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="cb3cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb3cf-104">SYNTAX</span></span>

### <span data-ttu-id="cb3cf-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3cf-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3cf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3cf-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb3cf-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb3cf-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb3cf-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb3cf-108">DESCRIPTION</span></span>
<span data-ttu-id="cb3cf-109">Get-AzAttestationPolicy cmdlet은 Azure Attestation의 테넌트에서 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="cb3cf-110">예제</span><span class="sxs-lookup"><span data-stu-id="cb3cf-110">EXAMPLES</span></span>

### <span data-ttu-id="cb3cf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb3cf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="cb3cf-112">Tee 형식 *SgxEnclave에* 대한 Attestation Provider *pshtest에* 대한 정책을 을 을 를 를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="cb3cf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cb3cf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

<span data-ttu-id="cb3cf-114">Tee 형식 *SgxEnclave에* 대한 *영국* 남부 위치에서 Attestation 기본 공급자에 대한 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="cb3cf-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb3cf-115">PARAMETERS</span></span>

### <span data-ttu-id="cb3cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb3cf-116">-DefaultProfile</span></span>
<span data-ttu-id="cb3cf-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb3cf-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="cb3cf-118">-DefaultProvider</span></span>
<span data-ttu-id="cb3cf-119">이 요청은 기본 데이터 등록 공급자에 대한 요청입니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-119">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3cf-120">-Location</span><span class="sxs-lookup"><span data-stu-id="cb3cf-120">-Location</span></span>
<span data-ttu-id="cb3cf-121">기본 토픽 공급자의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-121">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb3cf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cb3cf-122">-Name</span></span>
<span data-ttu-id="cb3cf-123">테넌트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="cb3cf-124">이 cmdlet은 이 매개 변수가 지정하는 테넌트에 대한 설명 정책을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb3cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb3cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb3cf-126">토의 공급자의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="cb3cf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb3cf-127">-ResourceId</span></span>
<span data-ttu-id="cb3cf-128">토의 공급자의 ResourceID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="cb3cf-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="cb3cf-129">-Tee</span></span>
<span data-ttu-id="cb3cf-130">신뢰할 수 있는 실행 환경 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="cb3cf-131">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave의 네 가지 유형의 환경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="cb3cf-132">-확인</span><span class="sxs-lookup"><span data-stu-id="cb3cf-132">-Confirm</span></span>
<span data-ttu-id="cb3cf-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb3cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb3cf-134">-WhatIf</span></span>
<span data-ttu-id="cb3cf-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb3cf-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb3cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb3cf-137">CommonParameters</span></span>
<span data-ttu-id="cb3cf-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb3cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb3cf-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb3cf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb3cf-140">입력</span><span class="sxs-lookup"><span data-stu-id="cb3cf-140">INPUTS</span></span>

### <span data-ttu-id="cb3cf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cb3cf-141">System.String</span></span>

## <span data-ttu-id="cb3cf-142">출력</span><span class="sxs-lookup"><span data-stu-id="cb3cf-142">OUTPUTS</span></span>

### <span data-ttu-id="cb3cf-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3cf-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="cb3cf-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb3cf-144">NOTES</span></span>

## <span data-ttu-id="cb3cf-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb3cf-145">RELATED LINKS</span></span>
