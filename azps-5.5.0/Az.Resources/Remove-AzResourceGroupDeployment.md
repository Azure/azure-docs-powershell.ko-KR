---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197969"
---
# <span data-ttu-id="a0b23-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0b23-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="a0b23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b23-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b23-103">리소스 그룹 배포 및 관련된 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="a0b23-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0b23-104">SYNTAX</span></span>

### <span data-ttu-id="a0b23-105">RemoveByResourceGroupName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a0b23-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0b23-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a0b23-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0b23-107">설명</span><span class="sxs-lookup"><span data-stu-id="a0b23-107">DESCRIPTION</span></span>

<span data-ttu-id="a0b23-108">**Remove-AzResourceGroupDeployment** cmdlet은 Azure 리소스 그룹 배포 및 연결된 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="a0b23-109">예제</span><span class="sxs-lookup"><span data-stu-id="a0b23-109">EXAMPLES</span></span>

### <span data-ttu-id="a0b23-110">예제 1: ResourceId를 사용하여 리소스 그룹 배포 제거</span><span class="sxs-lookup"><span data-stu-id="a0b23-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="a0b23-111">이 명령은 배포의 정식 리소스 ID를 사용하여 리소스 그룹 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a0b23-112">성공적으로 제거하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-112">Successful removal returns true.</span></span>

### <span data-ttu-id="a0b23-113">예제 2: ResourceGroupName 및 ResourceName을 사용하여 리소스 그룹 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="a0b23-114">이 명령은 제공된 ResourceGroupName 및 ResourceName을 사용하여 리소스 그룹 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="a0b23-115">성공적으로 제거하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-115">Successful removal returns true.</span></span>

## <span data-ttu-id="a0b23-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0b23-116">PARAMETERS</span></span>

### <span data-ttu-id="a0b23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b23-117">-DefaultProfile</span></span>
<span data-ttu-id="a0b23-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0b23-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b23-119">-Id</span><span class="sxs-lookup"><span data-stu-id="a0b23-119">-Id</span></span>
<span data-ttu-id="a0b23-120">제거할 리소스 그룹 배포의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b23-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0b23-121">-Name</span></span>
<span data-ttu-id="a0b23-122">제거할 리소스 그룹 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b23-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="a0b23-123">-Pre</span></span>
<span data-ttu-id="a0b23-124">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a0b23-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0b23-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0b23-126">제거할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0b23-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0b23-127">-Confirm</span></span>
<span data-ttu-id="a0b23-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0b23-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b23-129">-WhatIf</span></span>
<span data-ttu-id="a0b23-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a0b23-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0b23-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0b23-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b23-132">CommonParameters</span></span>
<span data-ttu-id="a0b23-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b23-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b23-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0b23-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b23-135">입력</span><span class="sxs-lookup"><span data-stu-id="a0b23-135">INPUTS</span></span>

### <span data-ttu-id="a0b23-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a0b23-136">System.String</span></span>

## <span data-ttu-id="a0b23-137">출력</span><span class="sxs-lookup"><span data-stu-id="a0b23-137">OUTPUTS</span></span>

### <span data-ttu-id="a0b23-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0b23-138">System.Boolean</span></span>

## <span data-ttu-id="a0b23-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0b23-139">NOTES</span></span>

## <span data-ttu-id="a0b23-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0b23-140">RELATED LINKS</span></span>

[<span data-ttu-id="a0b23-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0b23-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="a0b23-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0b23-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="a0b23-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0b23-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="a0b23-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a0b23-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


