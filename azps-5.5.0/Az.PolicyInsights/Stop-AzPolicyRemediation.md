---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202209"
---
# <span data-ttu-id="fd344-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="fd344-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="fd344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd344-102">SYNOPSIS</span></span>
<span data-ttu-id="fd344-103">진행 중 정책 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="fd344-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd344-104">SYNTAX</span></span>

### <span data-ttu-id="fd344-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd344-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd344-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd344-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd344-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd344-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd344-108">설명</span><span class="sxs-lookup"><span data-stu-id="fd344-108">DESCRIPTION</span></span>
<span data-ttu-id="fd344-109">**Stop-AzPolicyRemediation** cmdlet은 진행 중 정책 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="fd344-110">활성 배포가 취소되고 새 배포가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="fd344-111">예제</span><span class="sxs-lookup"><span data-stu-id="fd344-111">EXAMPLES</span></span>

### <span data-ttu-id="fd344-112">예제 1: 리소스 그룹 범위에서 정책 수정 취소</span><span class="sxs-lookup"><span data-stu-id="fd344-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="fd344-113">이 명령은 리소스 그룹 'myRG'에서 'remediation1'이라는 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="fd344-114">예제 2: 파이핑을 통해 관리 그룹 수정 취소</span><span class="sxs-lookup"><span data-stu-id="fd344-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="fd344-115">이 명령은 관리 그룹 'mg1'에서 'remediation1'이라는 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="fd344-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd344-116">PARAMETERS</span></span>

### <span data-ttu-id="fd344-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd344-117">-AsJob</span></span>
<span data-ttu-id="fd344-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fd344-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd344-119">-DefaultProfile</span></span>
<span data-ttu-id="fd344-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd344-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd344-121">-InputObject</span></span>
<span data-ttu-id="fd344-122">수정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd344-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fd344-123">-ManagementGroupName</span></span>
<span data-ttu-id="fd344-124">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd344-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fd344-125">-Name</span></span>
<span data-ttu-id="fd344-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd344-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd344-127">-PassThru</span></span>
<span data-ttu-id="fd344-128">명령이 성공적으로 완료되면 True를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="fd344-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd344-129">-ResourceGroupName</span></span>
<span data-ttu-id="fd344-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd344-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd344-131">-ResourceId</span></span>
<span data-ttu-id="fd344-132">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd344-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="fd344-133">-Scope</span></span>
<span data-ttu-id="fd344-134">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-134">Scope of the resource.</span></span>
<span data-ttu-id="fd344-135">예:</span><span class="sxs-lookup"><span data-stu-id="fd344-135">E.g.</span></span>
<span data-ttu-id="fd344-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="fd344-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd344-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd344-137">-Confirm</span></span>
<span data-ttu-id="fd344-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd344-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd344-139">-WhatIf</span></span>
<span data-ttu-id="fd344-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fd344-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd344-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd344-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd344-142">CommonParameters</span></span>
<span data-ttu-id="fd344-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd344-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd344-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd344-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd344-145">입력</span><span class="sxs-lookup"><span data-stu-id="fd344-145">INPUTS</span></span>

### <span data-ttu-id="fd344-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fd344-146">System.String</span></span>

### <span data-ttu-id="fd344-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="fd344-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="fd344-148">출력</span><span class="sxs-lookup"><span data-stu-id="fd344-148">OUTPUTS</span></span>

### <span data-ttu-id="fd344-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd344-149">System.Boolean</span></span>

## <span data-ttu-id="fd344-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd344-150">NOTES</span></span>

## <span data-ttu-id="fd344-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd344-151">RELATED LINKS</span></span>
