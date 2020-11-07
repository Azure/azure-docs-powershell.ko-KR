---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700987"
---
# <span data-ttu-id="58d1b-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="58d1b-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="58d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="58d1b-103">서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-103">Deletes the service topology.</span></span> <span data-ttu-id="58d1b-104">서비스 토폴로지를 삭제 하기 전에 먼저 서비스 토폴로지로 만든 모든 서비스를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="58d1b-105">구문과</span><span class="sxs-lookup"><span data-stu-id="58d1b-105">SYNTAX</span></span>

### <span data-ttu-id="58d1b-106">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="58d1b-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d1b-107">리소스</span><span class="sxs-lookup"><span data-stu-id="58d1b-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d1b-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="58d1b-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d1b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="58d1b-109">DESCRIPTION</span></span>
<span data-ttu-id="58d1b-110">**AzDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="58d1b-111">이름 및 리소스 그룹 이름을 기준으로 서비스 토폴로지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="58d1b-112">또는 ServiceTopology 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="58d1b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="58d1b-113">EXAMPLES</span></span>

### <span data-ttu-id="58d1b-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="58d1b-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="58d1b-115">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="58d1b-116">예제 2: 리소스 식별자를 사용 하 여 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="58d1b-117">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="58d1b-118">예제 3: 서비스 토폴로지 개체를 사용 하 여 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="58d1b-119">이 명령은 name 및 ResourceGroup이 $serviceTopologyObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="58d1b-120">변수</span><span class="sxs-lookup"><span data-stu-id="58d1b-120">PARAMETERS</span></span>

### <span data-ttu-id="58d1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d1b-121">-DefaultProfile</span></span>
<span data-ttu-id="58d1b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d1b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58d1b-123">-InputObject</span></span>
<span data-ttu-id="58d1b-124">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="58d1b-125">-Name</span></span>
<span data-ttu-id="58d1b-126">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58d1b-127">-PassThru</span></span>
<span data-ttu-id="58d1b-128">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="58d1b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="58d1b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d1b-129">-ResourceGroupName</span></span>
<span data-ttu-id="58d1b-130">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="58d1b-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58d1b-131">-ResourceId</span></span>
<span data-ttu-id="58d1b-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d1b-133">-확인</span><span class="sxs-lookup"><span data-stu-id="58d1b-133">-Confirm</span></span>
<span data-ttu-id="58d1b-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d1b-135">-WhatIf</span></span>
<span data-ttu-id="58d1b-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58d1b-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58d1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d1b-138">CommonParameters</span></span>
<span data-ttu-id="58d1b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58d1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d1b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d1b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d1b-141">입력</span><span class="sxs-lookup"><span data-stu-id="58d1b-141">INPUTS</span></span>

### <span data-ttu-id="58d1b-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58d1b-142">System.String</span></span>

### <span data-ttu-id="58d1b-143">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="58d1b-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="58d1b-144">출력</span><span class="sxs-lookup"><span data-stu-id="58d1b-144">OUTPUTS</span></span>

### <span data-ttu-id="58d1b-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="58d1b-145">System.Boolean</span></span>

## <span data-ttu-id="58d1b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="58d1b-146">NOTES</span></span>

## <span data-ttu-id="58d1b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58d1b-147">RELATED LINKS</span></span>