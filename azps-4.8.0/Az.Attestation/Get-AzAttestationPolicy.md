---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 64a74902d1a5b10ed36c635b58910246634e68b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048524"
---
# <span data-ttu-id="adc37-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="adc37-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="adc37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc37-102">SYNOPSIS</span></span>
<span data-ttu-id="adc37-103">Azure 증명의 테 넌 트에서 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="adc37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adc37-104">SYNTAX</span></span>

### <span data-ttu-id="adc37-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc37-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc37-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc37-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc37-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc37-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc37-108">설명은</span><span class="sxs-lookup"><span data-stu-id="adc37-108">DESCRIPTION</span></span>
<span data-ttu-id="adc37-109">Get-AzAttestationPolicy cmdlet은 Azure 증명의 테 넌 트에서 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="adc37-110">예제의</span><span class="sxs-lookup"><span data-stu-id="adc37-110">EXAMPLES</span></span>

### <span data-ttu-id="adc37-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="adc37-111">Example 1</span></span>
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

<span data-ttu-id="adc37-112">티 유형 *SgxEnclave* 에 대 한 증명 공급자 *pshtest* 에 대 한 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="adc37-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="adc37-113">Example 2</span></span>
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

<span data-ttu-id="adc37-114">T e t t e t t e t e t e t e t e *SgxEnclave* 의 증명 기본 공급자 위치 *영국 남아프리카*</span><span class="sxs-lookup"><span data-stu-id="adc37-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="adc37-115">변수</span><span class="sxs-lookup"><span data-stu-id="adc37-115">PARAMETERS</span></span>

### <span data-ttu-id="adc37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc37-116">-DefaultProfile</span></span>
<span data-ttu-id="adc37-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc37-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="adc37-118">-DefaultProvider</span></span>
<span data-ttu-id="adc37-119">기본 증명 공급자에 대 한 요청 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-119">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="adc37-120">-위치</span><span class="sxs-lookup"><span data-stu-id="adc37-120">-Location</span></span>
<span data-ttu-id="adc37-121">기본 증명 공급자의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-121">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="adc37-122">-이름</span><span class="sxs-lookup"><span data-stu-id="adc37-122">-Name</span></span>
<span data-ttu-id="adc37-123">테 넌 트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="adc37-124">이 cmdlet은이 매개 변수에서 지정 하는 테 넌 트에 대 한 증명 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="adc37-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc37-125">-ResourceGroupName</span></span>
<span data-ttu-id="adc37-126">증명 공급자의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="adc37-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adc37-127">-ResourceId</span></span>
<span data-ttu-id="adc37-128">증명 공급자의 ResourceID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="adc37-129">-T e</span><span class="sxs-lookup"><span data-stu-id="adc37-129">-Tee</span></span>
<span data-ttu-id="adc37-130">신뢰할 수 있는 실행 환경의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="adc37-131">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave 등 네 가지 유형의 환경을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="adc37-132">-확인</span><span class="sxs-lookup"><span data-stu-id="adc37-132">-Confirm</span></span>
<span data-ttu-id="adc37-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc37-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc37-134">-WhatIf</span></span>
<span data-ttu-id="adc37-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adc37-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc37-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc37-137">CommonParameters</span></span>
<span data-ttu-id="adc37-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc37-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc37-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adc37-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc37-140">입력</span><span class="sxs-lookup"><span data-stu-id="adc37-140">INPUTS</span></span>

### <span data-ttu-id="adc37-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="adc37-141">System.String</span></span>

## <span data-ttu-id="adc37-142">출력</span><span class="sxs-lookup"><span data-stu-id="adc37-142">OUTPUTS</span></span>

### <span data-ttu-id="adc37-143">Microsoft. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="adc37-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="adc37-144">상속자</span><span class="sxs-lookup"><span data-stu-id="adc37-144">NOTES</span></span>

## <span data-ttu-id="adc37-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc37-145">RELATED LINKS</span></span>
