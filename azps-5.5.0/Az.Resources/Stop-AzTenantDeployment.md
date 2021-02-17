---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178748"
---
# <span data-ttu-id="04ade-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="04ade-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="04ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ade-102">SYNOPSIS</span></span>
<span data-ttu-id="04ade-103">테넌트 범위에서 실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="04ade-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="04ade-104">구문</span><span class="sxs-lookup"><span data-stu-id="04ade-104">SYNTAX</span></span>

### <span data-ttu-id="04ade-105">StopByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="04ade-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ade-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="04ade-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ade-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="04ade-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ade-108">설명</span><span class="sxs-lookup"><span data-stu-id="04ade-108">DESCRIPTION</span></span>
<span data-ttu-id="04ade-109">**Stop-AzTenantDeployment** cmdlet은 현재 테넌트 범위에서 시작했지만 완료되지 않은 배포를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="04ade-110">배포를 중지하려면 배포에 프로비전 또는 실패와 같은 완료된 상태가 아닌 프로비전과 같은 불완전한 프로비전 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="04ade-111">테넌트 범위에서 배포를 만들 경우 New-AzTenantDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="04ade-112">예제</span><span class="sxs-lookup"><span data-stu-id="04ade-112">EXAMPLES</span></span>

### <span data-ttu-id="04ade-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="04ade-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="04ade-114">이 명령은 현재 테넌트 범위에서 실행 중인 배포 "deployment01"을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="04ade-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="04ade-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="04ade-116">이 명령은 현재 테넌트 범위에서 배포 "deployment01"을 구하고 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="04ade-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04ade-117">PARAMETERS</span></span>

### <span data-ttu-id="04ade-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ade-118">-DefaultProfile</span></span>
<span data-ttu-id="04ade-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04ade-120">-Id</span><span class="sxs-lookup"><span data-stu-id="04ade-120">-Id</span></span>
<span data-ttu-id="04ade-121">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="04ade-122">예: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="04ade-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="04ade-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ade-123">-InputObject</span></span>
<span data-ttu-id="04ade-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-124">The deployment object.</span></span>

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

### <span data-ttu-id="04ade-125">-Name</span><span class="sxs-lookup"><span data-stu-id="04ade-125">-Name</span></span>
<span data-ttu-id="04ade-126">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="04ade-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04ade-127">-PassThru</span></span>
<span data-ttu-id="04ade-128">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="04ade-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="04ade-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="04ade-129">-Pre</span></span>
<span data-ttu-id="04ade-130">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="04ade-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04ade-131">-Confirm</span></span>
<span data-ttu-id="04ade-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ade-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ade-133">-WhatIf</span></span>
<span data-ttu-id="04ade-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="04ade-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ade-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ade-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ade-136">CommonParameters</span></span>
<span data-ttu-id="04ade-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04ade-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ade-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04ade-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ade-139">입력</span><span class="sxs-lookup"><span data-stu-id="04ade-139">INPUTS</span></span>

### <span data-ttu-id="04ade-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="04ade-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="04ade-141">출력</span><span class="sxs-lookup"><span data-stu-id="04ade-141">OUTPUTS</span></span>

### <span data-ttu-id="04ade-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04ade-142">System.Boolean</span></span>

## <span data-ttu-id="04ade-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04ade-143">NOTES</span></span>

## <span data-ttu-id="04ade-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04ade-144">RELATED LINKS</span></span>
