---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357883"
---
# <span data-ttu-id="0f2fa-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0f2fa-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="0f2fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2fa-103">클러스터에서 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-103">Remove a service from the cluster.</span></span> <span data-ttu-id="0f2fa-104">배포된 ARM 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="0f2fa-105">구문</span><span class="sxs-lookup"><span data-stu-id="0f2fa-105">SYNTAX</span></span>

### <span data-ttu-id="0f2fa-106">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="0f2fa-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f2fa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f2fa-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f2fa-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0f2fa-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f2fa-109">설명</span><span class="sxs-lookup"><span data-stu-id="0f2fa-109">DESCRIPTION</span></span>
<span data-ttu-id="0f2fa-110">이 cmdlet은 클러스터의 서비스 양식을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="0f2fa-111">예제</span><span class="sxs-lookup"><span data-stu-id="0f2fa-111">EXAMPLES</span></span>

### <span data-ttu-id="0f2fa-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0f2fa-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="0f2fa-113">이 예제에서는 "testApp~testService1" 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="0f2fa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f2fa-114">PARAMETERS</span></span>

### <span data-ttu-id="0f2fa-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="0f2fa-115">-ApplicationName</span></span>
<span data-ttu-id="0f2fa-116">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="0f2fa-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0f2fa-117">-ClusterName</span></span>
<span data-ttu-id="0f2fa-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0f2fa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2fa-119">-DefaultProfile</span></span>
<span data-ttu-id="0f2fa-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f2fa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0f2fa-121">-Force</span></span>
<span data-ttu-id="0f2fa-122">프롬프트 없이 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="0f2fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f2fa-123">-InputObject</span></span>
<span data-ttu-id="0f2fa-124">서비스 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-124">The service resource.</span></span>

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

### <span data-ttu-id="0f2fa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0f2fa-125">-Name</span></span>
<span data-ttu-id="0f2fa-126">서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="0f2fa-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f2fa-127">-PassThru</span></span>
<span data-ttu-id="0f2fa-128">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="0f2fa-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0f2fa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2fa-129">-ResourceGroupName</span></span>
<span data-ttu-id="0f2fa-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0f2fa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f2fa-131">-ResourceId</span></span>
<span data-ttu-id="0f2fa-132">서비스의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="0f2fa-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f2fa-133">-Confirm</span></span>
<span data-ttu-id="0f2fa-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2fa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2fa-135">-WhatIf</span></span>
<span data-ttu-id="0f2fa-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0f2fa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f2fa-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2fa-138">CommonParameters</span></span>
<span data-ttu-id="0f2fa-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2fa-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f2fa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2fa-141">입력</span><span class="sxs-lookup"><span data-stu-id="0f2fa-141">INPUTS</span></span>

### <span data-ttu-id="0f2fa-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0f2fa-142">System.String</span></span>

### <span data-ttu-id="0f2fa-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="0f2fa-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="0f2fa-144">출력</span><span class="sxs-lookup"><span data-stu-id="0f2fa-144">OUTPUTS</span></span>

### <span data-ttu-id="0f2fa-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f2fa-145">System.Boolean</span></span>

## <span data-ttu-id="0f2fa-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f2fa-146">NOTES</span></span>

## <span data-ttu-id="0f2fa-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f2fa-147">RELATED LINKS</span></span>
