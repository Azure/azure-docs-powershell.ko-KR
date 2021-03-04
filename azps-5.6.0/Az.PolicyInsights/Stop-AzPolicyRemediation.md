---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2eb9d5a11b160a1061bbd769f337cf053b6ad805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989058"
---
# <span data-ttu-id="f1d3d-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f1d3d-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="f1d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d3d-103">진행 중 정책 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="f1d3d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1d3d-104">SYNTAX</span></span>

### <span data-ttu-id="f1d3d-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1d3d-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d3d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1d3d-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1d3d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f1d3d-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1d3d-108">설명</span><span class="sxs-lookup"><span data-stu-id="f1d3d-108">DESCRIPTION</span></span>
<span data-ttu-id="f1d3d-109">**Stop-AzPolicyRemediation** cmdlet은 진행 중 정책 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="f1d3d-110">활성 배포가 취소되고 새 배포가 생성되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="f1d3d-111">예제</span><span class="sxs-lookup"><span data-stu-id="f1d3d-111">EXAMPLES</span></span>

### <span data-ttu-id="f1d3d-112">예제 1: 리소스 그룹 범위에서 정책 수정 취소</span><span class="sxs-lookup"><span data-stu-id="f1d3d-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="f1d3d-113">이 명령은 리소스 그룹 'myRG'에서 'remediation1'이라는 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="f1d3d-114">예제 2: 배관을 통해 관리 그룹 수정 취소</span><span class="sxs-lookup"><span data-stu-id="f1d3d-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="f1d3d-115">이 명령은 관리 그룹 'mg1'에서 'remediation1'이라는 수정을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="f1d3d-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1d3d-116">PARAMETERS</span></span>

### <span data-ttu-id="f1d3d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1d3d-117">-AsJob</span></span>
<span data-ttu-id="f1d3d-118">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f1d3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d3d-119">-DefaultProfile</span></span>
<span data-ttu-id="f1d3d-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1d3d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1d3d-121">-InputObject</span></span>
<span data-ttu-id="f1d3d-122">수정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-122">The Remediation object.</span></span>

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

### <span data-ttu-id="f1d3d-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d3d-123">-ManagementGroupName</span></span>
<span data-ttu-id="f1d3d-124">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-124">Management group ID.</span></span>

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

### <span data-ttu-id="f1d3d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f1d3d-125">-Name</span></span>
<span data-ttu-id="f1d3d-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-126">Resource name.</span></span>

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

### <span data-ttu-id="f1d3d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1d3d-127">-PassThru</span></span>
<span data-ttu-id="f1d3d-128">명령이 성공적으로 완료되면 True를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="f1d3d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d3d-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1d3d-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-130">Resource group name.</span></span>

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

### <span data-ttu-id="f1d3d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1d3d-131">-ResourceId</span></span>
<span data-ttu-id="f1d3d-132">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-132">Resource ID.</span></span>

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

### <span data-ttu-id="f1d3d-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="f1d3d-133">-Scope</span></span>
<span data-ttu-id="f1d3d-134">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-134">Scope of the resource.</span></span>
<span data-ttu-id="f1d3d-135">예:</span><span class="sxs-lookup"><span data-stu-id="f1d3d-135">E.g.</span></span>
<span data-ttu-id="f1d3d-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="f1d3d-137">-확인</span><span class="sxs-lookup"><span data-stu-id="f1d3d-137">-Confirm</span></span>
<span data-ttu-id="f1d3d-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1d3d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1d3d-139">-WhatIf</span></span>
<span data-ttu-id="f1d3d-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1d3d-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1d3d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d3d-142">CommonParameters</span></span>
<span data-ttu-id="f1d3d-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d3d-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1d3d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d3d-145">입력</span><span class="sxs-lookup"><span data-stu-id="f1d3d-145">INPUTS</span></span>

### <span data-ttu-id="f1d3d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f1d3d-146">System.String</span></span>

### <span data-ttu-id="f1d3d-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="f1d3d-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="f1d3d-148">출력</span><span class="sxs-lookup"><span data-stu-id="f1d3d-148">OUTPUTS</span></span>

### <span data-ttu-id="f1d3d-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1d3d-149">System.Boolean</span></span>

## <span data-ttu-id="f1d3d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1d3d-150">NOTES</span></span>

## <span data-ttu-id="f1d3d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1d3d-151">RELATED LINKS</span></span>
