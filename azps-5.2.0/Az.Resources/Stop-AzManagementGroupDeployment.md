---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354801"
---
# <span data-ttu-id="d2df7-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d2df7-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d2df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2df7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2df7-103">관리 그룹에서 실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="d2df7-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="d2df7-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2df7-104">SYNTAX</span></span>

### <span data-ttu-id="d2df7-105">StopByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d2df7-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2df7-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d2df7-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2df7-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2df7-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2df7-108">설명</span><span class="sxs-lookup"><span data-stu-id="d2df7-108">DESCRIPTION</span></span>
<span data-ttu-id="d2df7-109">**Stop-AzManagementGroupDeployment** cmdlet은 관리 그룹에서 시작했지만 완료되지 않은 배포를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="d2df7-110">배포를 중지하려면 배포에 프로비전 또는 실패와 같은 완료된 상태가 아닌 프로비전과 같은 불완전한 프로비전 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="d2df7-111">관리 그룹에서 배포를 만들 경우 New-AzManagementGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="d2df7-112">예제</span><span class="sxs-lookup"><span data-stu-id="d2df7-112">EXAMPLES</span></span>

### <span data-ttu-id="d2df7-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2df7-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="d2df7-114">이 명령은 관리 그룹 "myMG"에서 실행 중인 배포 "deployment01"을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="d2df7-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="d2df7-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="d2df7-116">이 명령은 관리 그룹 "myMG"에서 배포 "deployment01"을 얻게 하여 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="d2df7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2df7-117">PARAMETERS</span></span>

### <span data-ttu-id="d2df7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2df7-118">-DefaultProfile</span></span>
<span data-ttu-id="d2df7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2df7-120">-Id</span><span class="sxs-lookup"><span data-stu-id="d2df7-120">-Id</span></span>
<span data-ttu-id="d2df7-121">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d2df7-122">예: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d2df7-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2df7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2df7-123">-InputObject</span></span>
<span data-ttu-id="d2df7-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2df7-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d2df7-125">-ManagementGroupId</span></span>
<span data-ttu-id="d2df7-126">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2df7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d2df7-127">-Name</span></span>
<span data-ttu-id="d2df7-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2df7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2df7-129">-PassThru</span></span>
<span data-ttu-id="d2df7-130">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="d2df7-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d2df7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d2df7-131">-Pre</span></span>
<span data-ttu-id="d2df7-132">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d2df7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2df7-133">-Confirm</span></span>
<span data-ttu-id="d2df7-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2df7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2df7-135">-WhatIf</span></span>
<span data-ttu-id="d2df7-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d2df7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2df7-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2df7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2df7-138">CommonParameters</span></span>
<span data-ttu-id="d2df7-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2df7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2df7-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2df7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2df7-141">입력</span><span class="sxs-lookup"><span data-stu-id="d2df7-141">INPUTS</span></span>

### <span data-ttu-id="d2df7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="d2df7-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d2df7-143">출력</span><span class="sxs-lookup"><span data-stu-id="d2df7-143">OUTPUTS</span></span>

### <span data-ttu-id="d2df7-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2df7-144">System.Boolean</span></span>

## <span data-ttu-id="d2df7-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2df7-145">NOTES</span></span>

## <span data-ttu-id="d2df7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2df7-146">RELATED LINKS</span></span>
