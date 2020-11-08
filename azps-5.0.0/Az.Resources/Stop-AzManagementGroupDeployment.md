---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217028"
---
# <span data-ttu-id="d6199-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d6199-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d6199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6199-102">SYNOPSIS</span></span>
<span data-ttu-id="d6199-103">관리 그룹에서 실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="d6199-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="d6199-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6199-104">SYNTAX</span></span>

### <span data-ttu-id="d6199-105">StopByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6199-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6199-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d6199-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6199-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6199-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6199-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d6199-108">DESCRIPTION</span></span>
<span data-ttu-id="d6199-109">**AzManagementGroupDeployment** cmdlet은 시작 되었지만 관리 그룹에서 완료 되지 않은 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="d6199-110">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="d6199-111">관리 그룹에서 배포를 만들려면 New-AzManagementGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="d6199-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d6199-112">EXAMPLES</span></span>

### <span data-ttu-id="d6199-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6199-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="d6199-114">이 명령은 관리 그룹 "myMG"에서 실행 중인 배포 "deployment01"을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="d6199-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="d6199-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="d6199-116">이 명령은 관리 그룹 "myMG"의 배포 "deployment01"를 가져와 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="d6199-117">변수</span><span class="sxs-lookup"><span data-stu-id="d6199-117">PARAMETERS</span></span>

### <span data-ttu-id="d6199-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6199-118">-DefaultProfile</span></span>
<span data-ttu-id="d6199-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6199-120">-Id</span><span class="sxs-lookup"><span data-stu-id="d6199-120">-Id</span></span>
<span data-ttu-id="d6199-121">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d6199-122">예:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d6199-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="d6199-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6199-123">-InputObject</span></span>
<span data-ttu-id="d6199-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-124">The deployment object.</span></span>

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

### <span data-ttu-id="d6199-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d6199-125">-ManagementGroupId</span></span>
<span data-ttu-id="d6199-126">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-126">The management group id.</span></span>

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

### <span data-ttu-id="d6199-127">-이름</span><span class="sxs-lookup"><span data-stu-id="d6199-127">-Name</span></span>
<span data-ttu-id="d6199-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="d6199-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6199-129">-PassThru</span></span>
<span data-ttu-id="d6199-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="d6199-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d6199-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6199-131">-Pre</span></span>
<span data-ttu-id="d6199-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d6199-133">-확인</span><span class="sxs-lookup"><span data-stu-id="d6199-133">-Confirm</span></span>
<span data-ttu-id="d6199-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6199-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6199-135">-WhatIf</span></span>
<span data-ttu-id="d6199-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6199-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6199-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6199-138">CommonParameters</span></span>
<span data-ttu-id="d6199-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6199-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6199-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6199-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6199-141">입력</span><span class="sxs-lookup"><span data-stu-id="d6199-141">INPUTS</span></span>

### <span data-ttu-id="d6199-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d6199-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d6199-143">출력</span><span class="sxs-lookup"><span data-stu-id="d6199-143">OUTPUTS</span></span>

### <span data-ttu-id="d6199-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d6199-144">System.Boolean</span></span>

## <span data-ttu-id="d6199-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d6199-145">NOTES</span></span>

## <span data-ttu-id="d6199-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6199-146">RELATED LINKS</span></span>
