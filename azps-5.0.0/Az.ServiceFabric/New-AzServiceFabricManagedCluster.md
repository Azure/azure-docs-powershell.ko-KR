---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216539"
---
# <span data-ttu-id="dba00-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dba00-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="dba00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba00-102">SYNOPSIS</span></span>
<span data-ttu-id="dba00-103">새 관리 되는 클러스터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-103">Create new managed cluster.</span></span>

## <span data-ttu-id="dba00-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dba00-104">SYNTAX</span></span>

### <span data-ttu-id="dba00-105">ClientCertByTp (기본값)</span><span class="sxs-lookup"><span data-stu-id="dba00-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba00-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="dba00-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba00-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dba00-107">DESCRIPTION</span></span>
<span data-ttu-id="dba00-108">이 cmdlet은 노드 형식을 사용 하지 않고 관리 되는 클러스터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="dba00-109">클러스터를 부트스트랩 하려면 [AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md)를 사용 하 여 기본 노드 유형을 추가 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="dba00-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dba00-110">EXAMPLES</span></span>

### <span data-ttu-id="dba00-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dba00-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="dba00-112">이 명령은 기본 sku를 사용 하 여 클러스터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="dba00-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dba00-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="dba00-114">이 명령은 초기 관리 클라이언트 인증서와 표준 sku를 사용 하 여 centraluseuap에서 클러스터 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="dba00-115">변수</span><span class="sxs-lookup"><span data-stu-id="dba00-115">PARAMETERS</span></span>

### <span data-ttu-id="dba00-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="dba00-116">-AdminPassword</span></span>
<span data-ttu-id="dba00-117">가상 컴퓨터에 사용 되는 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="dba00-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="dba00-118">-AdminUserName</span></span>
<span data-ttu-id="dba00-119">가상 컴퓨터에 사용 되는 관리자 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="dba00-120">기본값: vmadmin.</span><span class="sxs-lookup"><span data-stu-id="dba00-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="dba00-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dba00-121">-AsJob</span></span>
<span data-ttu-id="dba00-122">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dba00-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="dba00-123">-ClientCertCommonName</span></span>
<span data-ttu-id="dba00-124">클라이언트 인증서 일반 이름.</span><span class="sxs-lookup"><span data-stu-id="dba00-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="dba00-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="dba00-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="dba00-126">클라이언트 인증서에 관리자 수준이 있는지 여부를 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="dba00-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="dba00-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="dba00-128">클라이언트 인증서에 대 한 발급자 지문 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="dba00-129">ClientCertCommonName와 조합 하 여 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="dba00-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="dba00-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="dba00-131">클라이언트 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="dba00-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="dba00-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="dba00-132">-ClientConnectionPort</span></span>
<span data-ttu-id="dba00-133">클러스터에 대 한 클라이언트 연결에 사용 되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="dba00-134">기본값: 19000.</span><span class="sxs-lookup"><span data-stu-id="dba00-134">Default: 19000.</span></span>

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

### <span data-ttu-id="dba00-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="dba00-135">-CodeVersion</span></span>
<span data-ttu-id="dba00-136">클러스터 서비스 패브릭 코드 버전.</span><span class="sxs-lookup"><span data-stu-id="dba00-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="dba00-137">업그레이드 모드가 수동 인 경우에만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="dba00-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba00-138">-DefaultProfile</span></span>
<span data-ttu-id="dba00-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba00-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="dba00-140">-DnsName</span></span>
<span data-ttu-id="dba00-141">클러스터의 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="dba00-142">-Http게이트웨이 Connectionport</span><span class="sxs-lookup"><span data-stu-id="dba00-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="dba00-143">클러스터에 대 한 http 연결에 사용 되는 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="dba00-144">기본값: 19080.</span><span class="sxs-lookup"><span data-stu-id="dba00-144">Default: 19080.</span></span>

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

### <span data-ttu-id="dba00-145">-위치</span><span class="sxs-lookup"><span data-stu-id="dba00-145">-Location</span></span>
<span data-ttu-id="dba00-146">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="dba00-146">The resource location</span></span>

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

### <span data-ttu-id="dba00-147">-이름</span><span class="sxs-lookup"><span data-stu-id="dba00-147">-Name</span></span>
<span data-ttu-id="dba00-148">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="dba00-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba00-149">-ResourceGroupName</span></span>
<span data-ttu-id="dba00-150">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="dba00-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="dba00-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="dba00-152">역방향 프록시에 사용 되는 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="dba00-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="dba00-153">-Sku</span></span>
<span data-ttu-id="dba00-154">클러스터의 Sku, 옵션은 기본적으로 3 개의 시드 노드를 포함 하 고 1 개 노드 유형 및 표준만 허용 합니다. 최소 5 시드 노드가 있고 여러 노드 유형을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="dba00-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="dba00-155">-UpgradeMode</span></span>
<span data-ttu-id="dba00-156">클러스터 서비스 패브릭 코드 버전 업그레이드 모드.</span><span class="sxs-lookup"><span data-stu-id="dba00-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="dba00-157">자동 또는 수동.</span><span class="sxs-lookup"><span data-stu-id="dba00-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="dba00-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="dba00-158">-UseTestExtension</span></span>
<span data-ttu-id="dba00-159">지정 하는 경우 클러스터는 서비스 테스트 vmss 확장명을 사용 하 여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="dba00-160">-확인</span><span class="sxs-lookup"><span data-stu-id="dba00-160">-Confirm</span></span>
<span data-ttu-id="dba00-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba00-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba00-162">-WhatIf</span></span>
<span data-ttu-id="dba00-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba00-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba00-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba00-165">CommonParameters</span></span>
<span data-ttu-id="dba00-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dba00-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba00-167">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dba00-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba00-168">입력</span><span class="sxs-lookup"><span data-stu-id="dba00-168">INPUTS</span></span>

### <span data-ttu-id="dba00-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dba00-169">System.String</span></span>

## <span data-ttu-id="dba00-170">출력</span><span class="sxs-lookup"><span data-stu-id="dba00-170">OUTPUTS</span></span>

### <span data-ttu-id="dba00-171">ServiceFabric. a m. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dba00-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="dba00-172">상속자</span><span class="sxs-lookup"><span data-stu-id="dba00-172">NOTES</span></span>

## <span data-ttu-id="dba00-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dba00-173">RELATED LINKS</span></span>

[<span data-ttu-id="dba00-174">새로운 AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="dba00-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)