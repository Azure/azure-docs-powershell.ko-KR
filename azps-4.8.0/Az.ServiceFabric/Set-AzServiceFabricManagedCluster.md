---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213948"
---
# <span data-ttu-id="f5a26-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f5a26-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="f5a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a26-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a26-103">클러스터 리소스 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="f5a26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5a26-104">SYNTAX</span></span>

### <span data-ttu-id="f5a26-105">ByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5a26-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a26-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="f5a26-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a26-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="f5a26-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a26-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f5a26-108">DESCRIPTION</span></span>
<span data-ttu-id="f5a26-109">클러스터 리소스 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="f5a26-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f5a26-110">EXAMPLES</span></span>

### <span data-ttu-id="f5a26-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5a26-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="f5a26-112">클러스터에 대 한 dns 이름 및 클라이언트 연결 포트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="f5a26-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f5a26-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="f5a26-114">파이프를 사용 하 여 클러스터에 대 한 dns 이름 및 클라이언트 연결 포트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="f5a26-115">변수</span><span class="sxs-lookup"><span data-stu-id="f5a26-115">PARAMETERS</span></span>

### <span data-ttu-id="f5a26-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5a26-116">-AsJob</span></span>
<span data-ttu-id="f5a26-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f5a26-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="f5a26-118">-ClientConnectionPort</span></span>
<span data-ttu-id="f5a26-119">클러스터에 대 한 클라이언트 연결에 사용 되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="f5a26-120">기본값: 19000.</span><span class="sxs-lookup"><span data-stu-id="f5a26-120">Default: 19000.</span></span>

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

### <span data-ttu-id="f5a26-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="f5a26-121">-CodeVersion</span></span>
<span data-ttu-id="f5a26-122">클러스터 코드 버전.</span><span class="sxs-lookup"><span data-stu-id="f5a26-122">Cluster code version.</span></span> <span data-ttu-id="f5a26-123">업그레이드 모드가 수동 인 경우에만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-123">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="f5a26-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a26-124">-DefaultProfile</span></span>
<span data-ttu-id="f5a26-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a26-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="f5a26-126">-DnsName</span></span>
<span data-ttu-id="f5a26-127">클러스터의 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-127">Cluster's dns name.</span></span>

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

### <span data-ttu-id="f5a26-128">-Http게이트웨이 Connectionport</span><span class="sxs-lookup"><span data-stu-id="f5a26-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="f5a26-129">클러스터에 대 한 http 연결에 사용 되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="f5a26-130">기본값: 19080.</span><span class="sxs-lookup"><span data-stu-id="f5a26-130">Default: 19080.</span></span>

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

### <span data-ttu-id="f5a26-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5a26-131">-InputObject</span></span>
<span data-ttu-id="f5a26-132">관리 되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="f5a26-132">Managed Cluster resource</span></span>

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

### <span data-ttu-id="f5a26-133">-이름</span><span class="sxs-lookup"><span data-stu-id="f5a26-133">-Name</span></span>
<span data-ttu-id="f5a26-134">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-134">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f5a26-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a26-135">-ResourceGroupName</span></span>
<span data-ttu-id="f5a26-136">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-136">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f5a26-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5a26-137">-ResourceId</span></span>
<span data-ttu-id="f5a26-138">관리 되는 클러스터 리소스 id</span><span class="sxs-lookup"><span data-stu-id="f5a26-138">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="f5a26-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="f5a26-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="f5a26-140">역방향 프록시에 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-140">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="f5a26-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="f5a26-141">-UpgradeMode</span></span>
<span data-ttu-id="f5a26-142">클러스터 코드 버전 업그레이드 모드.</span><span class="sxs-lookup"><span data-stu-id="f5a26-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="f5a26-143">자동 또는 수동.</span><span class="sxs-lookup"><span data-stu-id="f5a26-143">Automatic or Manual.</span></span>

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

### <span data-ttu-id="f5a26-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f5a26-144">-Confirm</span></span>
<span data-ttu-id="f5a26-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a26-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a26-146">-WhatIf</span></span>
<span data-ttu-id="f5a26-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5a26-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a26-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a26-149">CommonParameters</span></span>
<span data-ttu-id="f5a26-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a26-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a26-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5a26-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a26-152">입력</span><span class="sxs-lookup"><span data-stu-id="f5a26-152">INPUTS</span></span>

### <span data-ttu-id="f5a26-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f5a26-153">System.String</span></span>

## <span data-ttu-id="f5a26-154">출력</span><span class="sxs-lookup"><span data-stu-id="f5a26-154">OUTPUTS</span></span>

### <span data-ttu-id="f5a26-155">ServiceFabric. a m. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f5a26-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="f5a26-156">상속자</span><span class="sxs-lookup"><span data-stu-id="f5a26-156">NOTES</span></span>

## <span data-ttu-id="f5a26-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5a26-157">RELATED LINKS</span></span>
