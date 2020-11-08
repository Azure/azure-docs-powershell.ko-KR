---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204105"
---
# <span data-ttu-id="796d5-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="796d5-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="796d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="796d5-102">SYNOPSIS</span></span>
<span data-ttu-id="796d5-103">Azure Attestationn의 테 넌 트에서 정책을 다시 설정 합니다.}</span><span class="sxs-lookup"><span data-stu-id="796d5-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="796d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="796d5-104">SYNTAX</span></span>

### <span data-ttu-id="796d5-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="796d5-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="796d5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="796d5-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="796d5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="796d5-107">DESCRIPTION</span></span>
<span data-ttu-id="796d5-108">Reset-AzAttestationPolicy cmdlet은 Azure 증명의 테 넌 트에서 사용자가 정의한 증명 정책을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="796d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="796d5-109">EXAMPLES</span></span>

### <span data-ttu-id="796d5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="796d5-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="796d5-111">T e t type *SgxEnclave* 에 대 한 증명 공급자 *pshtest* 의 기본값으로 정책을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="796d5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="796d5-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="796d5-113">증명 공급자 *pshtest* 가 격리 된 신뢰 모델을 사용 하도록 구성 된 경우에는 서명 된 정책을 포함 하 여 *SgxEnclave* 에서 정책을 t e 티 형식에 대 한 기본값으로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="796d5-114">변수</span><span class="sxs-lookup"><span data-stu-id="796d5-114">PARAMETERS</span></span>

### <span data-ttu-id="796d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="796d5-115">-DefaultProfile</span></span>
<span data-ttu-id="796d5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="796d5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="796d5-117">-Name</span></span>
<span data-ttu-id="796d5-118">테 넌 트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="796d5-119">이 cmdlet은이 매개 변수에서 지정 하는 테 넌 트에 대 한 증명 정책을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="796d5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="796d5-120">-PassThru</span></span>
<span data-ttu-id="796d5-121">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="796d5-122">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="796d5-123">-정책</span><span class="sxs-lookup"><span data-stu-id="796d5-123">-Policy</span></span>
<span data-ttu-id="796d5-124">다시 설정할 정책 문서를 설명 하는 JSON 웹 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="796d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="796d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="796d5-126">증명 공급자의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="796d5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="796d5-127">-ResourceId</span></span>
<span data-ttu-id="796d5-128">증명 공급자의 ResourceID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="796d5-129">-T e</span><span class="sxs-lookup"><span data-stu-id="796d5-129">-Tee</span></span>
<span data-ttu-id="796d5-130">신뢰할 수 있는 실행 환경의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="796d5-131">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave 등 네 가지 유형의 환경을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="796d5-132">-확인</span><span class="sxs-lookup"><span data-stu-id="796d5-132">-Confirm</span></span>
<span data-ttu-id="796d5-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="796d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="796d5-134">-WhatIf</span></span>
<span data-ttu-id="796d5-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="796d5-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="796d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="796d5-137">CommonParameters</span></span>
<span data-ttu-id="796d5-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="796d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="796d5-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="796d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="796d5-140">입력</span><span class="sxs-lookup"><span data-stu-id="796d5-140">INPUTS</span></span>

### <span data-ttu-id="796d5-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="796d5-141">System.String</span></span>

## <span data-ttu-id="796d5-142">출력</span><span class="sxs-lookup"><span data-stu-id="796d5-142">OUTPUTS</span></span>

### <span data-ttu-id="796d5-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="796d5-143">System.Boolean</span></span>

## <span data-ttu-id="796d5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="796d5-144">NOTES</span></span>

## <span data-ttu-id="796d5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="796d5-145">RELATED LINKS</span></span>
