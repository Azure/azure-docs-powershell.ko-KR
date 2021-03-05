---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 794cc94ece2452f1fd5518d64d4071d7fa6ec326
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963755"
---
# <span data-ttu-id="71f86-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="71f86-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="71f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71f86-102">SYNOPSIS</span></span>
<span data-ttu-id="71f86-103">실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="71f86-103">Cancel a running deployment</span></span>

## <span data-ttu-id="71f86-104">구문</span><span class="sxs-lookup"><span data-stu-id="71f86-104">SYNTAX</span></span>

### <span data-ttu-id="71f86-105">StopByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="71f86-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71f86-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="71f86-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71f86-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="71f86-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71f86-108">설명</span><span class="sxs-lookup"><span data-stu-id="71f86-108">DESCRIPTION</span></span>
<span data-ttu-id="71f86-109">**Stop-AzDeployment** cmdlet은 시작했지만 완료되지 않은 구독 범위의 배포를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="71f86-110">배포를 중지하려면 배포에 프로비전 또는 실패와 같은 완료된 상태가 아닌 프로비전과 같은 불완전한 프로비전 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="71f86-111">구독 범위에서 배포를 만들하려면 New-AzDeployment cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="71f86-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="71f86-112">이 cmdlet은 실행 중인 배포 하나만 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="71f86-113">이름 매개 *변수를* 사용하여 특정 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="71f86-114">예제</span><span class="sxs-lookup"><span data-stu-id="71f86-114">EXAMPLES</span></span>

### <span data-ttu-id="71f86-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="71f86-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="71f86-116">이 명령은 현재 구독 범위에서 실행 중인 배포 "deployment01"을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="71f86-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="71f86-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="71f86-118">이 명령은 현재 구독 범위에서 배포 "deployment01"을 얻게 하여 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="71f86-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71f86-119">PARAMETERS</span></span>

### <span data-ttu-id="71f86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f86-120">-DefaultProfile</span></span>
<span data-ttu-id="71f86-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71f86-122">-Id</span><span class="sxs-lookup"><span data-stu-id="71f86-122">-Id</span></span>
<span data-ttu-id="71f86-123">배포의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="71f86-124">예제: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="71f86-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="71f86-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71f86-125">-InputObject</span></span>
<span data-ttu-id="71f86-126">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-126">The deployment object.</span></span>

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

### <span data-ttu-id="71f86-127">-Name</span><span class="sxs-lookup"><span data-stu-id="71f86-127">-Name</span></span>
<span data-ttu-id="71f86-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="71f86-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71f86-129">-PassThru</span></span>
<span data-ttu-id="71f86-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="71f86-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="71f86-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="71f86-131">-Pre</span></span>
<span data-ttu-id="71f86-132">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="71f86-133">-확인</span><span class="sxs-lookup"><span data-stu-id="71f86-133">-Confirm</span></span>
<span data-ttu-id="71f86-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f86-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f86-135">-WhatIf</span></span>
<span data-ttu-id="71f86-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f86-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f86-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f86-138">CommonParameters</span></span>
<span data-ttu-id="71f86-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71f86-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f86-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71f86-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f86-141">입력</span><span class="sxs-lookup"><span data-stu-id="71f86-141">INPUTS</span></span>

### <span data-ttu-id="71f86-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDMicrosoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="71f86-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="71f86-143">출력</span><span class="sxs-lookup"><span data-stu-id="71f86-143">OUTPUTS</span></span>

### <span data-ttu-id="71f86-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71f86-144">System.Boolean</span></span>

## <span data-ttu-id="71f86-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71f86-145">NOTES</span></span>

## <span data-ttu-id="71f86-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71f86-146">RELATED LINKS</span></span>
