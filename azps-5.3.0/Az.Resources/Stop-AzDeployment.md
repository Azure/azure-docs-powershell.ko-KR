---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490272"
---
# <span data-ttu-id="1dea0-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1dea0-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="1dea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dea0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dea0-103">실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="1dea0-103">Cancel a running deployment</span></span>

## <span data-ttu-id="1dea0-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dea0-104">SYNTAX</span></span>

### <span data-ttu-id="1dea0-105">StopByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1dea0-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dea0-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1dea0-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dea0-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="1dea0-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dea0-108">설명</span><span class="sxs-lookup"><span data-stu-id="1dea0-108">DESCRIPTION</span></span>
<span data-ttu-id="1dea0-109">**Stop-AzDeployment** cmdlet은 시작했지만 완료되지 않은 구독 범위에서 배포를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="1dea0-110">배포를 중지하려면 배포에 프로비전 또는 실패와 같은 완료된 상태가 아닌 프로비전과 같은 불완전한 프로비전 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="1dea0-111">구독 범위에서 배포를 만들하려면 New-AzDeployment cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="1dea0-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="1dea0-112">이 cmdlet은 실행 중인 배포 하나만 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="1dea0-113">Name 매개 *변수를* 사용하여 특정 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="1dea0-114">예제</span><span class="sxs-lookup"><span data-stu-id="1dea0-114">EXAMPLES</span></span>

### <span data-ttu-id="1dea0-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dea0-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="1dea0-116">이 명령은 현재 구독 범위에서 실행 중인 배포 "deployment01"을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="1dea0-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="1dea0-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="1dea0-118">이 명령은 현재 구독 범위에서 배포 "deployment01"을 얻게 하여 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="1dea0-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dea0-119">PARAMETERS</span></span>

### <span data-ttu-id="1dea0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dea0-120">-DefaultProfile</span></span>
<span data-ttu-id="1dea0-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dea0-122">-Id</span><span class="sxs-lookup"><span data-stu-id="1dea0-122">-Id</span></span>
<span data-ttu-id="1dea0-123">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="1dea0-124">예: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="1dea0-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="1dea0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dea0-125">-InputObject</span></span>
<span data-ttu-id="1dea0-126">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-126">The deployment object.</span></span>

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

### <span data-ttu-id="1dea0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1dea0-127">-Name</span></span>
<span data-ttu-id="1dea0-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dea0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dea0-129">-PassThru</span></span>
<span data-ttu-id="1dea0-130">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="1dea0-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1dea0-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="1dea0-131">-Pre</span></span>
<span data-ttu-id="1dea0-132">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1dea0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dea0-133">-Confirm</span></span>
<span data-ttu-id="1dea0-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dea0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dea0-135">-WhatIf</span></span>
<span data-ttu-id="1dea0-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1dea0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dea0-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dea0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dea0-138">CommonParameters</span></span>
<span data-ttu-id="1dea0-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dea0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dea0-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1dea0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dea0-141">입력</span><span class="sxs-lookup"><span data-stu-id="1dea0-141">INPUTS</span></span>

### <span data-ttu-id="1dea0-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="1dea0-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1dea0-143">출력</span><span class="sxs-lookup"><span data-stu-id="1dea0-143">OUTPUTS</span></span>

### <span data-ttu-id="1dea0-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1dea0-144">System.Boolean</span></span>

## <span data-ttu-id="1dea0-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dea0-145">NOTES</span></span>

## <span data-ttu-id="1dea0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dea0-146">RELATED LINKS</span></span>
