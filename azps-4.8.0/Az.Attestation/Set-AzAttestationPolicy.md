---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204104"
---
# <span data-ttu-id="7c67c-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="7c67c-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="7c67c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c67c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c67c-103">Azure Attestationn의 테 넌 트에서 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="7c67c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c67c-104">SYNTAX</span></span>

### <span data-ttu-id="7c67c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c67c-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c67c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c67c-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c67c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c67c-107">DESCRIPTION</span></span>
<span data-ttu-id="7c67c-108">Set-AzAttestationPolicy cmdlet은 Azure 증명의 테 넌 트에서 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="7c67c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7c67c-109">EXAMPLES</span></span>

### <span data-ttu-id="7c67c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c67c-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="7c67c-111">텍스트 정책 형식 (기본값)을 사용 하 여 증명 공급자 *pshtest* 의 티 형식 *SgxEnclave* 에 대 한 사용자 정의 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="7c67c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c67c-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="7c67c-113">JWT 정책 형식을 사용 하 여 증명 공급자 *pshtest* 의 티 형식 *SgxEnclave* 에 대 한 사용자 정의 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="7c67c-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c67c-114">PARAMETERS</span></span>

### <span data-ttu-id="7c67c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c67c-115">-DefaultProfile</span></span>
<span data-ttu-id="7c67c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c67c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7c67c-117">-Name</span></span>
<span data-ttu-id="7c67c-118">테 넌 트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="7c67c-119">이 cmdlet은이 매개 변수에서 지정 하는 테 넌 트에 대 한 증명 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c67c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c67c-120">-PassThru</span></span>
<span data-ttu-id="7c67c-121">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7c67c-122">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7c67c-123">-정책</span><span class="sxs-lookup"><span data-stu-id="7c67c-123">-Policy</span></span>
<span data-ttu-id="7c67c-124">설정할 정책 문서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="7c67c-125">정책 형식은 Text 또는 JWT (JSON Web Token) 중 하나일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="7c67c-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="7c67c-126">-PolicyFormat</span></span>
<span data-ttu-id="7c67c-127">정책에 대 한 형식 (Text 또는 JWT (JSON 웹 토큰))을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="7c67c-128">기본 정책 형식은 텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="7c67c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c67c-129">-ResourceGroupName</span></span>
<span data-ttu-id="7c67c-130">증명 공급자의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="7c67c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c67c-131">-ResourceId</span></span>
<span data-ttu-id="7c67c-132">증명 공급자의 ResourceID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="7c67c-133">-T e</span><span class="sxs-lookup"><span data-stu-id="7c67c-133">-Tee</span></span>
<span data-ttu-id="7c67c-134">신뢰할 수 있는 실행 환경의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="7c67c-135">SgxEnclave, OpenEnclave, CyResComponent 및 VBSEnclave 등 네 가지 유형의 환경이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="7c67c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="7c67c-136">-Confirm</span></span>
<span data-ttu-id="7c67c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c67c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c67c-138">-WhatIf</span></span>
<span data-ttu-id="7c67c-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c67c-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c67c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c67c-141">CommonParameters</span></span>
<span data-ttu-id="7c67c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c67c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c67c-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c67c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c67c-144">입력</span><span class="sxs-lookup"><span data-stu-id="7c67c-144">INPUTS</span></span>

### <span data-ttu-id="7c67c-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c67c-145">System.String</span></span>

## <span data-ttu-id="7c67c-146">출력</span><span class="sxs-lookup"><span data-stu-id="7c67c-146">OUTPUTS</span></span>

### <span data-ttu-id="7c67c-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c67c-147">System.String</span></span>

## <span data-ttu-id="7c67c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="7c67c-148">NOTES</span></span>

## <span data-ttu-id="7c67c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c67c-149">RELATED LINKS</span></span>
