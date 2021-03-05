---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 992cd2a381e9eda89b9388ec1ed37f74a76e9adf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005419"
---
# <span data-ttu-id="30927-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="30927-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="30927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30927-102">SYNOPSIS</span></span>
<span data-ttu-id="30927-103">클러스터에서 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-103">Remove a service from the cluster.</span></span> <span data-ttu-id="30927-104">배포된 ARM 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="30927-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="30927-105">구문</span><span class="sxs-lookup"><span data-stu-id="30927-105">SYNTAX</span></span>

### <span data-ttu-id="30927-106">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="30927-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30927-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30927-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30927-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="30927-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30927-109">설명</span><span class="sxs-lookup"><span data-stu-id="30927-109">DESCRIPTION</span></span>
<span data-ttu-id="30927-110">이 cmdlet은 클러스터의 서비스 폼을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="30927-111">예제</span><span class="sxs-lookup"><span data-stu-id="30927-111">EXAMPLES</span></span>

### <span data-ttu-id="30927-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="30927-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="30927-113">이 예제에서는 "testApp~testService1"을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="30927-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="30927-114">PARAMETERS</span></span>

### <span data-ttu-id="30927-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="30927-115">-ApplicationName</span></span>
<span data-ttu-id="30927-116">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30927-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="30927-117">-ClusterName</span></span>
<span data-ttu-id="30927-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30927-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30927-119">-DefaultProfile</span></span>
<span data-ttu-id="30927-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30927-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30927-121">-Force</span><span class="sxs-lookup"><span data-stu-id="30927-121">-Force</span></span>
<span data-ttu-id="30927-122">프롬프트 없이 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="30927-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30927-123">-InputObject</span></span>
<span data-ttu-id="30927-124">서비스 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="30927-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30927-125">-Name</span><span class="sxs-lookup"><span data-stu-id="30927-125">-Name</span></span>
<span data-ttu-id="30927-126">서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30927-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30927-127">-PassThru</span></span>
<span data-ttu-id="30927-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="30927-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="30927-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30927-129">-ResourceGroupName</span></span>
<span data-ttu-id="30927-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30927-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30927-131">-ResourceId</span></span>
<span data-ttu-id="30927-132">서비스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="30927-132">Arm ResourceId of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30927-133">-확인</span><span class="sxs-lookup"><span data-stu-id="30927-133">-Confirm</span></span>
<span data-ttu-id="30927-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="30927-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30927-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30927-135">-WhatIf</span></span>
<span data-ttu-id="30927-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="30927-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30927-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30927-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30927-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30927-138">CommonParameters</span></span>
<span data-ttu-id="30927-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30927-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30927-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30927-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30927-141">입력</span><span class="sxs-lookup"><span data-stu-id="30927-141">INPUTS</span></span>

### <span data-ttu-id="30927-142">System.String</span><span class="sxs-lookup"><span data-stu-id="30927-142">System.String</span></span>

### <span data-ttu-id="30927-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="30927-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="30927-144">출력</span><span class="sxs-lookup"><span data-stu-id="30927-144">OUTPUTS</span></span>

### <span data-ttu-id="30927-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30927-145">System.Boolean</span></span>

## <span data-ttu-id="30927-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30927-146">NOTES</span></span>

## <span data-ttu-id="30927-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30927-147">RELATED LINKS</span></span>
