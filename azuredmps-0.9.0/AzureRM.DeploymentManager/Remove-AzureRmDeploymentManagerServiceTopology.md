---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523160"
---
# <span data-ttu-id="6a38e-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6a38e-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="6a38e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a38e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a38e-103">서비스 토폴로지와 해당 리소스를 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="6a38e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a38e-104">SYNTAX</span></span>

### <span data-ttu-id="6a38e-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a38e-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a38e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="6a38e-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a38e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6a38e-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a38e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6a38e-108">DESCRIPTION</span></span>
<span data-ttu-id="6a38e-109">**AzureRmDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="6a38e-110">이름 및 리소스 그룹 이름을 기준으로 서비스 토폴로지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="6a38e-111">또는 ServiceTopology 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="6a38e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6a38e-112">EXAMPLES</span></span>

### <span data-ttu-id="6a38e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a38e-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="6a38e-114">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6a38e-115">예제 2: 리소스 식별자를 사용 하 여 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="6a38e-116">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6a38e-117">예제 3: 서비스 토폴로지 개체를 사용 하 여 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="6a38e-118">이 명령은 name 및 ResourceGroup이 $serviceTopologyObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 서비스 토폴로지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="6a38e-119">변수</span><span class="sxs-lookup"><span data-stu-id="6a38e-119">PARAMETERS</span></span>

### <span data-ttu-id="6a38e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a38e-120">-DefaultProfile</span></span>
<span data-ttu-id="6a38e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a38e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6a38e-122">-Force</span></span>
<span data-ttu-id="6a38e-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6a38e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="6a38e-124">-Name</span></span>
<span data-ttu-id="6a38e-125">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-125">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a38e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a38e-126">-PassThru</span></span>
<span data-ttu-id="6a38e-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="6a38e-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6a38e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a38e-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a38e-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="6a38e-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a38e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a38e-130">-ResourceId</span></span>
<span data-ttu-id="6a38e-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-131">The resource identifier.</span></span>

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

### <span data-ttu-id="6a38e-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6a38e-132">-ServiceTopology</span></span>
<span data-ttu-id="6a38e-133">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="6a38e-134">-확인</span><span class="sxs-lookup"><span data-stu-id="6a38e-134">-Confirm</span></span>
<span data-ttu-id="6a38e-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a38e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a38e-136">-WhatIf</span></span>
<span data-ttu-id="6a38e-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a38e-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a38e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a38e-139">CommonParameters</span></span>
<span data-ttu-id="6a38e-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a38e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a38e-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a38e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a38e-142">입력</span><span class="sxs-lookup"><span data-stu-id="6a38e-142">INPUTS</span></span>

### <span data-ttu-id="6a38e-143">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="6a38e-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="6a38e-144">출력</span><span class="sxs-lookup"><span data-stu-id="6a38e-144">OUTPUTS</span></span>

### <span data-ttu-id="6a38e-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6a38e-145">System.Boolean</span></span>

## <span data-ttu-id="6a38e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="6a38e-146">NOTES</span></span>

## <span data-ttu-id="6a38e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a38e-147">RELATED LINKS</span></span>

[<span data-ttu-id="6a38e-148">새로운 AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6a38e-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="6a38e-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6a38e-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="6a38e-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6a38e-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)