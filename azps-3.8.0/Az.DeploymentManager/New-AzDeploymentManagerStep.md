---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044403"
---
# <span data-ttu-id="bdbaf-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="bdbaf-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="bdbaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbaf-103">단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-103">Creates a step.</span></span>

## <span data-ttu-id="bdbaf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdbaf-104">SYNTAX</span></span>

### <span data-ttu-id="bdbaf-105">Wait (기본값)</span><span class="sxs-lookup"><span data-stu-id="bdbaf-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbaf-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="bdbaf-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbaf-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="bdbaf-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdbaf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bdbaf-108">DESCRIPTION</span></span>
<span data-ttu-id="bdbaf-109">**AzDeploymentManagerStep** cmdlet은 롤아웃에서 참조할 수 있는 배포 단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="bdbaf-110">*Name* , *ResourceGroupName* 및 required 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="bdbaf-111">반환 된 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerStep cmdlet을 사용 하 여 단계에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="bdbaf-112">예제의</span><span class="sxs-lookup"><span data-stu-id="bdbaf-112">EXAMPLES</span></span>

### <span data-ttu-id="bdbaf-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="bdbaf-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="bdbaf-114">중앙 US와 이름이 ContosoService1WaitStep 인 ContosoResourceGroup에 리소스 위치로 이동 하는 단계를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="bdbaf-115">Duration 속성은 다음 단계를 실행 하기 전에 롤아웃이 대기 하는 기간을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="bdbaf-116">변수</span><span class="sxs-lookup"><span data-stu-id="bdbaf-116">PARAMETERS</span></span>

### <span data-ttu-id="bdbaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbaf-117">-DefaultProfile</span></span>
<span data-ttu-id="bdbaf-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdbaf-119">-기간</span><span class="sxs-lookup"><span data-stu-id="bdbaf-119">-Duration</span></span>
<span data-ttu-id="bdbaf-120">ISO 8601 형식으로 대기할 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="bdbaf-121">예: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="bdbaf-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="bdbaf-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="bdbaf-122">-HealthCheckProperties</span></span>
<span data-ttu-id="bdbaf-123">상태 검사 속성</span><span class="sxs-lookup"><span data-stu-id="bdbaf-123">The health check properties.</span></span>

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

### <span data-ttu-id="bdbaf-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="bdbaf-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="bdbaf-125">상태 검사 속성이 정의 되어 있는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="bdbaf-126">-위치</span><span class="sxs-lookup"><span data-stu-id="bdbaf-126">-Location</span></span>
<span data-ttu-id="bdbaf-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-127">The location of the resource.</span></span>

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

### <span data-ttu-id="bdbaf-128">-이름</span><span class="sxs-lookup"><span data-stu-id="bdbaf-128">-Name</span></span>
<span data-ttu-id="bdbaf-129">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-129">The name of the step.</span></span>

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

### <span data-ttu-id="bdbaf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbaf-130">-ResourceGroupName</span></span>
<span data-ttu-id="bdbaf-131">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="bdbaf-131">The resource group.</span></span>

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

### <span data-ttu-id="bdbaf-132">태그</span><span class="sxs-lookup"><span data-stu-id="bdbaf-132">-Tag</span></span>
<span data-ttu-id="bdbaf-133">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="bdbaf-134">-확인</span><span class="sxs-lookup"><span data-stu-id="bdbaf-134">-Confirm</span></span>
<span data-ttu-id="bdbaf-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdbaf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbaf-136">-WhatIf</span></span>
<span data-ttu-id="bdbaf-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdbaf-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdbaf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbaf-139">CommonParameters</span></span>
<span data-ttu-id="bdbaf-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbaf-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbaf-142">입력</span><span class="sxs-lookup"><span data-stu-id="bdbaf-142">INPUTS</span></span>

### <span data-ttu-id="bdbaf-143">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="bdbaf-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bdbaf-144">출력</span><span class="sxs-lookup"><span data-stu-id="bdbaf-144">OUTPUTS</span></span>

### <span data-ttu-id="bdbaf-145">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="bdbaf-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="bdbaf-146">상속자</span><span class="sxs-lookup"><span data-stu-id="bdbaf-146">NOTES</span></span>

## <span data-ttu-id="bdbaf-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdbaf-147">RELATED LINKS</span></span>
