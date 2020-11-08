---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1475296638cec105713eaa390bcce6552e5502ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215856"
---
# <span data-ttu-id="b6cf7-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="b6cf7-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="b6cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cf7-103">클러스터에서 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="b6cf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6cf7-104">SYNTAX</span></span>

### <span data-ttu-id="b6cf7-105">ByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6cf7-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cf7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cf7-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cf7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6cf7-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6cf7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b6cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="b6cf7-109">이 cmdlet은 클러스터의 서비스 양식을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="b6cf7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b6cf7-110">EXAMPLES</span></span>

### <span data-ttu-id="b6cf7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6cf7-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="b6cf7-112">이 예제에서는 "testApp ~ testService1" 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="b6cf7-113">변수</span><span class="sxs-lookup"><span data-stu-id="b6cf7-113">PARAMETERS</span></span>

### <span data-ttu-id="b6cf7-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b6cf7-114">-ApplicationName</span></span>
<span data-ttu-id="b6cf7-115">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="b6cf7-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b6cf7-116">-ClusterName</span></span>
<span data-ttu-id="b6cf7-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b6cf7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cf7-118">-DefaultProfile</span></span>
<span data-ttu-id="b6cf7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6cf7-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b6cf7-120">-Force</span></span>
<span data-ttu-id="b6cf7-121">메시지를 표시 하지 않고 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="b6cf7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6cf7-122">-InputObject</span></span>
<span data-ttu-id="b6cf7-123">서비스 리소스.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-123">The service resource.</span></span>

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

### <span data-ttu-id="b6cf7-124">-이름</span><span class="sxs-lookup"><span data-stu-id="b6cf7-124">-Name</span></span>
<span data-ttu-id="b6cf7-125">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="b6cf7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6cf7-126">-PassThru</span></span>
<span data-ttu-id="b6cf7-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b6cf7-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b6cf7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cf7-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6cf7-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b6cf7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cf7-130">-ResourceId</span></span>
<span data-ttu-id="b6cf7-131">서비스 팔에 대 한 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="b6cf7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b6cf7-132">-Confirm</span></span>
<span data-ttu-id="b6cf7-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6cf7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6cf7-134">-WhatIf</span></span>
<span data-ttu-id="b6cf7-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6cf7-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6cf7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cf7-137">CommonParameters</span></span>
<span data-ttu-id="b6cf7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cf7-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cf7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cf7-140">입력</span><span class="sxs-lookup"><span data-stu-id="b6cf7-140">INPUTS</span></span>

### <span data-ttu-id="b6cf7-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b6cf7-141">System.String</span></span>

### <span data-ttu-id="b6cf7-142">ServiceFabric. a i m. PSService</span><span class="sxs-lookup"><span data-stu-id="b6cf7-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="b6cf7-143">출력</span><span class="sxs-lookup"><span data-stu-id="b6cf7-143">OUTPUTS</span></span>

### <span data-ttu-id="b6cf7-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b6cf7-144">System.Boolean</span></span>

## <span data-ttu-id="b6cf7-145">상속자</span><span class="sxs-lookup"><span data-stu-id="b6cf7-145">NOTES</span></span>

## <span data-ttu-id="b6cf7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6cf7-146">RELATED LINKS</span></span>
