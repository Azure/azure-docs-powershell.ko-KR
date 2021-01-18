---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494770"
---
# <span data-ttu-id="6c02d-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6c02d-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="6c02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c02d-102">SYNOPSIS</span></span>
<span data-ttu-id="6c02d-103">새 관리되는 클러스터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-103">Create new managed cluster.</span></span>

## <span data-ttu-id="6c02d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c02d-104">SYNTAX</span></span>

### <span data-ttu-id="6c02d-105">ClientCertByTp(기본값)</span><span class="sxs-lookup"><span data-stu-id="6c02d-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c02d-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="6c02d-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c02d-107">설명</span><span class="sxs-lookup"><span data-stu-id="6c02d-107">DESCRIPTION</span></span>
<span data-ttu-id="6c02d-108">이 cmdlet은 노드 유형 없이 관리되는 클러스터 리소스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="6c02d-109">클러스터를 부트스트롯하기 위해 기본 노드 유형을 추가해야 합니다. [New-AzServiceFabricManagedNodeType을 사용하세요.](./New-AzServiceFabricManagedNodeType.md)</span><span class="sxs-lookup"><span data-stu-id="6c02d-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="6c02d-110">예제</span><span class="sxs-lookup"><span data-stu-id="6c02d-110">EXAMPLES</span></span>

### <span data-ttu-id="6c02d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c02d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="6c02d-112">이 명령은 기본 기본 SKU를 사용하여 클러스터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="6c02d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6c02d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="6c02d-114">이 명령은 초기 관리 클라이언트 인증서 및 표준 SKU를 사용하여 centraluseuap에 클러스터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="6c02d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c02d-115">PARAMETERS</span></span>

### <span data-ttu-id="6c02d-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="6c02d-116">-AdminPassword</span></span>
<span data-ttu-id="6c02d-117">가상 머신에 사용되는 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="6c02d-118">-AdminUserName</span></span>
<span data-ttu-id="6c02d-119">가상 머신에 사용되는 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="6c02d-120">기본값: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="6c02d-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c02d-121">-AsJob</span></span>
<span data-ttu-id="6c02d-122">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6c02d-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="6c02d-123">-ClientCertCommonName</span></span>
<span data-ttu-id="6c02d-124">클라이언트 인증서 일반 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="6c02d-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="6c02d-126">클라이언트 인증서에 관리자 수준이 있는지 지정하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="6c02d-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="6c02d-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="6c02d-128">클라이언트 인증서에 대한 발급자 지문 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="6c02d-129">ClientCertCommonName과 함께만 사용.</span><span class="sxs-lookup"><span data-stu-id="6c02d-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="6c02d-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="6c02d-131">클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="6c02d-132">-ClientConnectionPort</span></span>
<span data-ttu-id="6c02d-133">클러스터에 대한 클라이언트 연결에 사용되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="6c02d-134">기본값: 19000.</span><span class="sxs-lookup"><span data-stu-id="6c02d-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="6c02d-135">-CodeVersion</span></span>
<span data-ttu-id="6c02d-136">클러스터 서비스 패브릭 코드 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="6c02d-137">업그레이드 모드가 수동인 경우만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-137">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c02d-138">-DefaultProfile</span></span>
<span data-ttu-id="6c02d-139">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c02d-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="6c02d-140">-DnsName</span></span>
<span data-ttu-id="6c02d-141">클러스터의 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-141">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="6c02d-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="6c02d-143">클러스터에 대한 http 연결에 사용되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="6c02d-144">기본값: 19080.</span><span class="sxs-lookup"><span data-stu-id="6c02d-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-145">-Location</span><span class="sxs-lookup"><span data-stu-id="6c02d-145">-Location</span></span>
<span data-ttu-id="6c02d-146">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="6c02d-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-147">-Name</span><span class="sxs-lookup"><span data-stu-id="6c02d-147">-Name</span></span>
<span data-ttu-id="6c02d-148">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c02d-149">-ResourceGroupName</span></span>
<span data-ttu-id="6c02d-150">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="6c02d-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="6c02d-152">역방향 프록시에서 사용하는 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="6c02d-153">-Sku</span></span>
<span data-ttu-id="6c02d-154">클러스터의 SKU, 옵션은 Basic입니다. 최소 3개 시드 노드를 가지며 1개 노드 유형 및 표준만 허용합니다. 최소 5개 시드 노드를 가지며 여러 노드 유형을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="6c02d-155">-UpgradeMode</span></span>
<span data-ttu-id="6c02d-156">클러스터 서비스 패브릭 코드 버전 업그레이드 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="6c02d-157">자동 또는 수동.</span><span class="sxs-lookup"><span data-stu-id="6c02d-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c02d-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="6c02d-158">-UseTestExtension</span></span>
<span data-ttu-id="6c02d-159">클러스터를 지정하는 경우 서비스 테스트 vmss 확장으로 등급이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="6c02d-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c02d-160">-Confirm</span></span>
<span data-ttu-id="6c02d-161">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c02d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c02d-162">-WhatIf</span></span>
<span data-ttu-id="6c02d-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6c02d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c02d-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c02d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c02d-165">CommonParameters</span></span>
<span data-ttu-id="6c02d-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c02d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c02d-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c02d-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c02d-168">입력</span><span class="sxs-lookup"><span data-stu-id="6c02d-168">INPUTS</span></span>

### <span data-ttu-id="6c02d-169">System.String</span><span class="sxs-lookup"><span data-stu-id="6c02d-169">System.String</span></span>

## <span data-ttu-id="6c02d-170">출력</span><span class="sxs-lookup"><span data-stu-id="6c02d-170">OUTPUTS</span></span>

### <span data-ttu-id="6c02d-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="6c02d-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="6c02d-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c02d-172">NOTES</span></span>

## <span data-ttu-id="6c02d-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c02d-173">RELATED LINKS</span></span>

[<span data-ttu-id="6c02d-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="6c02d-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)