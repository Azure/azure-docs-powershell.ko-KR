---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494806"
---
# <span data-ttu-id="95744-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="95744-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="95744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95744-102">SYNOPSIS</span></span>
<span data-ttu-id="95744-103">클러스터에 인증서 일반 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="95744-104">이렇게 하면 클라이언트 인증을 위해 클러스터에 인증서가 다시 등록됩니다.</span><span class="sxs-lookup"><span data-stu-id="95744-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="95744-105">구문</span><span class="sxs-lookup"><span data-stu-id="95744-105">SYNTAX</span></span>

### <span data-ttu-id="95744-106">ClientCertByTpByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="95744-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95744-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="95744-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95744-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="95744-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95744-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="95744-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95744-110">설명</span><span class="sxs-lookup"><span data-stu-id="95744-110">DESCRIPTION</span></span>
<span data-ttu-id="95744-111">클러스터에 인증서 일반 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="95744-112">이렇게 하면 클라이언트 인증을 위해 클러스터에 인증서가 다시 등록됩니다.</span><span class="sxs-lookup"><span data-stu-id="95744-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="95744-113">예제</span><span class="sxs-lookup"><span data-stu-id="95744-113">EXAMPLES</span></span>

### <span data-ttu-id="95744-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="95744-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="95744-115">이 명령은 지문 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'가 있는 인증서를 클러스터에 추가합니다. 따라서 클라이언트는 인증서를 관리자로 사용하여 클러스터와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95744-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="95744-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="95744-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="95744-117">이 명령은 일반 이름이 'Contoso.com' 및 발급자 2명인 읽기 전용 클라이언트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="95744-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="95744-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="95744-119">이 명령은 일반 이름이 'Contoso.com'인 읽기 전용 클라이언트 인증서와 파이핑을 사용하여 발급자 2명을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="95744-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95744-120">PARAMETERS</span></span>

### <span data-ttu-id="95744-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="95744-121">-Admin</span></span>
<span data-ttu-id="95744-122">클라이언트 인증서에 관리자 수준이 있는지 지정하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95744-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="95744-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95744-123">-AsJob</span></span>
<span data-ttu-id="95744-124">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95744-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="95744-125">-CommonName</span></span>
<span data-ttu-id="95744-126">클라이언트 인증서 일반 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95744-126">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95744-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95744-127">-DefaultProfile</span></span>
<span data-ttu-id="95744-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95744-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95744-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95744-129">-InputObject</span></span>
<span data-ttu-id="95744-130">관리되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="95744-130">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95744-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="95744-131">-IssuerThumbprint</span></span>
<span data-ttu-id="95744-132">클라이언트 인증서에 대한 발급자 지문 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="95744-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="95744-133">CommonName과 함께만 사용</span><span class="sxs-lookup"><span data-stu-id="95744-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95744-134">-Name</span><span class="sxs-lookup"><span data-stu-id="95744-134">-Name</span></span>
<span data-ttu-id="95744-135">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95744-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95744-136">-ResourceGroupName</span></span>
<span data-ttu-id="95744-137">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95744-138">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="95744-138">-Thumbprint</span></span>
<span data-ttu-id="95744-139">클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="95744-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95744-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95744-140">-Confirm</span></span>
<span data-ttu-id="95744-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95744-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95744-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95744-142">-WhatIf</span></span>
<span data-ttu-id="95744-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="95744-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95744-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95744-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95744-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95744-145">CommonParameters</span></span>
<span data-ttu-id="95744-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95744-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95744-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="95744-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95744-148">입력</span><span class="sxs-lookup"><span data-stu-id="95744-148">INPUTS</span></span>

### <span data-ttu-id="95744-149">System.String</span><span class="sxs-lookup"><span data-stu-id="95744-149">System.String</span></span>

## <span data-ttu-id="95744-150">출력</span><span class="sxs-lookup"><span data-stu-id="95744-150">OUTPUTS</span></span>

### <span data-ttu-id="95744-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="95744-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="95744-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95744-152">NOTES</span></span>

## <span data-ttu-id="95744-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95744-153">RELATED LINKS</span></span>
