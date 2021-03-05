---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 8a3ca4ed215dccbcc3cbfb541d7e023871bf6490
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005360"
---
# <span data-ttu-id="33fc5-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="33fc5-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="33fc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="33fc5-103">클러스터 리소스 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="33fc5-104">구문</span><span class="sxs-lookup"><span data-stu-id="33fc5-104">SYNTAX</span></span>

### <span data-ttu-id="33fc5-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="33fc5-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33fc5-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="33fc5-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33fc5-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="33fc5-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33fc5-108">설명</span><span class="sxs-lookup"><span data-stu-id="33fc5-108">DESCRIPTION</span></span>
<span data-ttu-id="33fc5-109">클러스터 리소스 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="33fc5-110">예제</span><span class="sxs-lookup"><span data-stu-id="33fc5-110">EXAMPLES</span></span>

### <span data-ttu-id="33fc5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="33fc5-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="33fc5-112">클러스터에 대한 dns 이름 및 클라이언트 연결 포트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="33fc5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="33fc5-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="33fc5-114">클러스터에 대한 dns 이름 및 클라이언트 연결 포트를 파이핑으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="33fc5-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="33fc5-115">PARAMETERS</span></span>

### <span data-ttu-id="33fc5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33fc5-116">-AsJob</span></span>
<span data-ttu-id="33fc5-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="33fc5-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="33fc5-118">-ClientConnectionPort</span></span>
<span data-ttu-id="33fc5-119">클러스터에 대한 클라이언트 연결에 사용되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="33fc5-120">기본값: 19000입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="33fc5-121">-CodeVersion</span></span>
<span data-ttu-id="33fc5-122">클러스터 코드 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-122">Cluster code version.</span></span> <span data-ttu-id="33fc5-123">업그레이드 모드가 수동인 경우만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fc5-124">-DefaultProfile</span></span>
<span data-ttu-id="33fc5-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33fc5-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="33fc5-126">-DnsName</span></span>
<span data-ttu-id="33fc5-127">클러스터의 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="33fc5-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="33fc5-129">클러스터에 대한 http 연결에 사용되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="33fc5-130">기본값: 19080.</span><span class="sxs-lookup"><span data-stu-id="33fc5-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33fc5-131">-InputObject</span></span>
<span data-ttu-id="33fc5-132">관리되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="33fc5-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="33fc5-133">-Name</span></span>
<span data-ttu-id="33fc5-134">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33fc5-135">-ResourceGroupName</span></span>
<span data-ttu-id="33fc5-136">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33fc5-137">-ResourceId</span></span>
<span data-ttu-id="33fc5-138">관리되는 클러스터 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="33fc5-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="33fc5-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="33fc5-140">역방향 프록시에서 사용되는 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="33fc5-141">-UpgradeMode</span></span>
<span data-ttu-id="33fc5-142">클러스터 코드 버전 업그레이드 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="33fc5-143">자동 또는 수동.</span><span class="sxs-lookup"><span data-stu-id="33fc5-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fc5-144">-확인</span><span class="sxs-lookup"><span data-stu-id="33fc5-144">-Confirm</span></span>
<span data-ttu-id="33fc5-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33fc5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33fc5-146">-WhatIf</span></span>
<span data-ttu-id="33fc5-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33fc5-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33fc5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fc5-149">CommonParameters</span></span>
<span data-ttu-id="33fc5-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33fc5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fc5-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33fc5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fc5-152">입력</span><span class="sxs-lookup"><span data-stu-id="33fc5-152">INPUTS</span></span>

### <span data-ttu-id="33fc5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="33fc5-153">System.String</span></span>

## <span data-ttu-id="33fc5-154">출력</span><span class="sxs-lookup"><span data-stu-id="33fc5-154">OUTPUTS</span></span>

### <span data-ttu-id="33fc5-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="33fc5-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="33fc5-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33fc5-156">NOTES</span></span>

## <span data-ttu-id="33fc5-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33fc5-157">RELATED LINKS</span></span>
