---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: d85a6170505563daf1033df60474fd94011d928f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974379"
---
# <span data-ttu-id="647ee-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="647ee-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="647ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="647ee-102">SYNOPSIS</span></span>
<span data-ttu-id="647ee-103">리소스 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-103">Removes a resource group.</span></span>

## <span data-ttu-id="647ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="647ee-104">SYNTAX</span></span>

### <span data-ttu-id="647ee-105">RemoveByResourceGroupName(기본값)</span><span class="sxs-lookup"><span data-stu-id="647ee-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="647ee-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="647ee-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="647ee-107">설명</span><span class="sxs-lookup"><span data-stu-id="647ee-107">DESCRIPTION</span></span>
<span data-ttu-id="647ee-108">**Remove-AzResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹 및 해당 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="647ee-109">리소스를 삭제하지만 리소스 그룹을 떠날 경우 Remove-AzResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="647ee-110">예제</span><span class="sxs-lookup"><span data-stu-id="647ee-110">EXAMPLES</span></span>

### <span data-ttu-id="647ee-111">예제 1: 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="647ee-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="647ee-112">이 명령은 구독에서 ContosoRG01 리소스 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="647ee-113">cmdlet은 확인을 묻는 메시지를 표시하고 출력을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="647ee-114">예제 2: 확인 없이 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="647ee-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="647ee-115">이 명령은 Get-AzResourceGroup cmdlet을 사용하여 리소스 그룹 ContosoRG01을 얻은 다음 파이프라인 연산자를 사용하여 **Remove-AzResourceGroup에** 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="647ee-116">Force *매개* 변수는 확인 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="647ee-117">예제 3: 모든 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="647ee-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="647ee-118">이 명령은 **Get-AzResourceGroup** cmdlet을 사용하여 모든 리소스 그룹을 얻은 다음 파이프라인 연산자를 사용하여 **Remove-AzResourceGroup에** 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="647ee-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="647ee-119">PARAMETERS</span></span>

### <span data-ttu-id="647ee-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="647ee-120">-ApiVersion</span></span>
<span data-ttu-id="647ee-121">리소스 공급자에서 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="647ee-122">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="647ee-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="647ee-123">-AsJob</span></span>
<span data-ttu-id="647ee-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="647ee-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="647ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647ee-125">-DefaultProfile</span></span>
<span data-ttu-id="647ee-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="647ee-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="647ee-127">-Force</span><span class="sxs-lookup"><span data-stu-id="647ee-127">-Force</span></span>
<span data-ttu-id="647ee-128">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="647ee-129">-Id</span><span class="sxs-lookup"><span data-stu-id="647ee-129">-Id</span></span>
<span data-ttu-id="647ee-130">제거할 리소스 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="647ee-131">와일드카드 문자는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647ee-132">-Name</span><span class="sxs-lookup"><span data-stu-id="647ee-132">-Name</span></span>
<span data-ttu-id="647ee-133">제거할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="647ee-134">와일드카드 문자는 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="647ee-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="647ee-135">-Pre</span></span>
<span data-ttu-id="647ee-136">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="647ee-137">-확인</span><span class="sxs-lookup"><span data-stu-id="647ee-137">-Confirm</span></span>
<span data-ttu-id="647ee-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="647ee-139">-WhatIf</span></span>
<span data-ttu-id="647ee-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="647ee-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="647ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647ee-142">CommonParameters</span></span>
<span data-ttu-id="647ee-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="647ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647ee-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="647ee-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647ee-145">입력</span><span class="sxs-lookup"><span data-stu-id="647ee-145">INPUTS</span></span>

### <span data-ttu-id="647ee-146">System.String</span><span class="sxs-lookup"><span data-stu-id="647ee-146">System.String</span></span>

## <span data-ttu-id="647ee-147">출력</span><span class="sxs-lookup"><span data-stu-id="647ee-147">OUTPUTS</span></span>

### <span data-ttu-id="647ee-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="647ee-148">System.Boolean</span></span>

## <span data-ttu-id="647ee-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="647ee-149">NOTES</span></span>

## <span data-ttu-id="647ee-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="647ee-150">RELATED LINKS</span></span>

[<span data-ttu-id="647ee-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="647ee-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="647ee-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="647ee-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="647ee-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="647ee-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


