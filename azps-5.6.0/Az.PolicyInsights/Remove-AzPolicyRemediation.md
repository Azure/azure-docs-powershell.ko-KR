---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 44e6be7e7f112d0c6e4e657aca5670211aff6006
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989081"
---
# <span data-ttu-id="6f467-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6f467-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="6f467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f467-102">SYNOPSIS</span></span>
<span data-ttu-id="6f467-103">정책 수정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="6f467-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f467-104">SYNTAX</span></span>

### <span data-ttu-id="6f467-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6f467-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f467-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f467-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f467-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f467-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f467-108">설명</span><span class="sxs-lookup"><span data-stu-id="6f467-108">DESCRIPTION</span></span>
<span data-ttu-id="6f467-109">**Remove-AzPolicyRemediation** cmdlet은 정책 수정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="6f467-110">예제</span><span class="sxs-lookup"><span data-stu-id="6f467-110">EXAMPLES</span></span>

### <span data-ttu-id="6f467-111">예제 1: 리소스 그룹 범위에서 정책 수정 삭제</span><span class="sxs-lookup"><span data-stu-id="6f467-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="6f467-112">이 명령은 리소스 그룹 'myRG'에서 'remediation1'이라는 수정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="6f467-113">예제 2: 배관을 통해 관리 그룹 수정 삭제</span><span class="sxs-lookup"><span data-stu-id="6f467-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="6f467-114">이 명령은 관리 그룹 'mg1'에서 'remediation1'이라는 수정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="6f467-115">리소스를 삭제하기 전에 확인 프롬프트가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="6f467-116">예제 3: 정책 수정 취소 및 삭제</span><span class="sxs-lookup"><span data-stu-id="6f467-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="6f467-117">이 명령은 리소스 그룹 'myRG'에서 'remediation1'이라는 수정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="6f467-118">수정이 진행 중이면 삭제되기 전에 취소됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="6f467-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f467-119">PARAMETERS</span></span>

### <span data-ttu-id="6f467-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="6f467-120">-AllowStop</span></span>
<span data-ttu-id="6f467-121">진행 중일 경우 수정을 취소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="6f467-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f467-122">-AsJob</span></span>
<span data-ttu-id="6f467-123">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6f467-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f467-124">-DefaultProfile</span></span>
<span data-ttu-id="6f467-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f467-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f467-126">-InputObject</span></span>
<span data-ttu-id="6f467-127">수정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-127">The Remediation object.</span></span>

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

### <span data-ttu-id="6f467-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6f467-128">-ManagementGroupName</span></span>
<span data-ttu-id="6f467-129">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-129">Management group ID.</span></span>

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

### <span data-ttu-id="6f467-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6f467-130">-Name</span></span>
<span data-ttu-id="6f467-131">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-131">Resource name.</span></span>

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

### <span data-ttu-id="6f467-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f467-132">-PassThru</span></span>
<span data-ttu-id="6f467-133">명령이 성공적으로 완료되면 True를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="6f467-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f467-134">-ResourceGroupName</span></span>
<span data-ttu-id="6f467-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-135">Resource group name.</span></span>

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

### <span data-ttu-id="6f467-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f467-136">-ResourceId</span></span>
<span data-ttu-id="6f467-137">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-137">Resource ID.</span></span>

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

### <span data-ttu-id="6f467-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="6f467-138">-Scope</span></span>
<span data-ttu-id="6f467-139">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-139">Scope of the resource.</span></span>
<span data-ttu-id="6f467-140">예:</span><span class="sxs-lookup"><span data-stu-id="6f467-140">E.g.</span></span>
<span data-ttu-id="6f467-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="6f467-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="6f467-142">-확인</span><span class="sxs-lookup"><span data-stu-id="6f467-142">-Confirm</span></span>
<span data-ttu-id="6f467-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f467-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f467-144">-WhatIf</span></span>
<span data-ttu-id="6f467-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f467-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f467-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f467-147">CommonParameters</span></span>
<span data-ttu-id="6f467-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f467-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f467-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f467-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f467-150">입력</span><span class="sxs-lookup"><span data-stu-id="6f467-150">INPUTS</span></span>

### <span data-ttu-id="6f467-151">System.String</span><span class="sxs-lookup"><span data-stu-id="6f467-151">System.String</span></span>

### <span data-ttu-id="6f467-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="6f467-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="6f467-153">출력</span><span class="sxs-lookup"><span data-stu-id="6f467-153">OUTPUTS</span></span>

### <span data-ttu-id="6f467-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f467-154">System.Boolean</span></span>

## <span data-ttu-id="6f467-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f467-155">NOTES</span></span>

## <span data-ttu-id="6f467-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f467-156">RELATED LINKS</span></span>
