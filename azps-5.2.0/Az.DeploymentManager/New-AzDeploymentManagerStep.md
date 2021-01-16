---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355922"
---
# <span data-ttu-id="e0686-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="e0686-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="e0686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0686-102">SYNOPSIS</span></span>
<span data-ttu-id="e0686-103">단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-103">Creates a step.</span></span>

## <span data-ttu-id="e0686-104">구문</span><span class="sxs-lookup"><span data-stu-id="e0686-104">SYNTAX</span></span>

### <span data-ttu-id="e0686-105">대기(기본값)</span><span class="sxs-lookup"><span data-stu-id="e0686-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0686-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="e0686-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0686-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="e0686-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0686-108">설명</span><span class="sxs-lookup"><span data-stu-id="e0686-108">DESCRIPTION</span></span>
<span data-ttu-id="e0686-109">**New-AzDeploymentManagerStep** cmdlet은 롤아웃에서 참조할 수 있는 배포 단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="e0686-110">*이름,* *ResourceGroupName 및* 필수 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="e0686-111">반환된 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerStep cmdlet을 사용하여 단계에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="e0686-112">예제</span><span class="sxs-lookup"><span data-stu-id="e0686-112">EXAMPLES</span></span>

### <span data-ttu-id="e0686-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="e0686-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="e0686-114">ContosoResourceGroup에서 미국 중부와 함께 리소스의 위치로 이름이 ContosoService1WaitStep인 단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="e0686-115">Duration 속성은 다음 단계를 실행하기 전에 롤아웃이 대기하는 기간을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="e0686-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0686-116">PARAMETERS</span></span>

### <span data-ttu-id="e0686-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0686-117">-DefaultProfile</span></span>
<span data-ttu-id="e0686-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0686-119">-Duration</span><span class="sxs-lookup"><span data-stu-id="e0686-119">-Duration</span></span>
<span data-ttu-id="e0686-120">ISO 8601 형식으로 대기하는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="e0686-121">예: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="e0686-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="e0686-122">-HealthCheckProperties</span></span>
<span data-ttu-id="e0686-123">상태 검사 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="e0686-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="e0686-125">상태 검사 속성이 정의되는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-126">-Location</span><span class="sxs-lookup"><span data-stu-id="e0686-126">-Location</span></span>
<span data-ttu-id="e0686-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e0686-128">-Name</span></span>
<span data-ttu-id="e0686-129">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0686-130">-ResourceGroupName</span></span>
<span data-ttu-id="e0686-131">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0686-132">-Tag</span></span>
<span data-ttu-id="e0686-133">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0686-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0686-134">-Confirm</span></span>
<span data-ttu-id="e0686-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0686-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0686-136">-WhatIf</span></span>
<span data-ttu-id="e0686-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e0686-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0686-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0686-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0686-139">CommonParameters</span></span>
<span data-ttu-id="e0686-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e0686-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0686-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e0686-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0686-142">입력</span><span class="sxs-lookup"><span data-stu-id="e0686-142">INPUTS</span></span>

### <span data-ttu-id="e0686-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0686-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e0686-144">출력</span><span class="sxs-lookup"><span data-stu-id="e0686-144">OUTPUTS</span></span>

### <span data-ttu-id="e0686-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="e0686-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="e0686-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e0686-146">NOTES</span></span>

## <span data-ttu-id="e0686-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0686-147">RELATED LINKS</span></span>
