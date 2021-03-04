---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: 11534ff7102295cd312410c5ecbae932fd9459e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969840"
---
# <span data-ttu-id="7e20d-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="7e20d-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="7e20d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e20d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e20d-103">클러스터에 인증서 일반 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="7e20d-104">이렇게 하면 클라이언트 인증을 위해 클러스터가 다시 인증서를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="7e20d-105">구문</span><span class="sxs-lookup"><span data-stu-id="7e20d-105">SYNTAX</span></span>

### <span data-ttu-id="7e20d-106">ClientCertByTpByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e20d-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e20d-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="7e20d-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e20d-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="7e20d-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e20d-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="7e20d-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e20d-110">설명</span><span class="sxs-lookup"><span data-stu-id="7e20d-110">DESCRIPTION</span></span>
<span data-ttu-id="7e20d-111">클러스터에 인증서 일반 이름 또는 지문을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="7e20d-112">이렇게 하면 클라이언트 인증을 위해 클러스터가 다시 인증서를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="7e20d-113">예제</span><span class="sxs-lookup"><span data-stu-id="7e20d-113">EXAMPLES</span></span>

### <span data-ttu-id="7e20d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e20d-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="7e20d-115">이 명령은 지문 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'가 있는 인증서를 클러스터에 추가하여 클라이언트가 인증서를 관리자로 사용하여 클러스터와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="7e20d-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="7e20d-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="7e20d-117">이 명령은 'Contoso.com' 및 발급자 2개가 있는 읽기 전용 클라이언트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="7e20d-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="7e20d-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="7e20d-119">이 명령은 'Contoso.com' 및 2개 발급자(배관)가 있는 읽기 전용 클라이언트 인증서를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="7e20d-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e20d-120">PARAMETERS</span></span>

### <span data-ttu-id="7e20d-121">-Admin</span><span class="sxs-lookup"><span data-stu-id="7e20d-121">-Admin</span></span>
<span data-ttu-id="7e20d-122">클라이언트 인증서에 관리자 수준이 있는지 지정하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="7e20d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e20d-123">-AsJob</span></span>
<span data-ttu-id="7e20d-124">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7e20d-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="7e20d-125">-CommonName</span></span>
<span data-ttu-id="7e20d-126">클라이언트 인증서 일반 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="7e20d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e20d-127">-DefaultProfile</span></span>
<span data-ttu-id="7e20d-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e20d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e20d-129">-InputObject</span></span>
<span data-ttu-id="7e20d-130">관리되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="7e20d-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="7e20d-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="7e20d-131">-IssuerThumbprint</span></span>
<span data-ttu-id="7e20d-132">클라이언트 인증서에 대한 발급자 지문 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="7e20d-133">CommonName과 함께만 사용.</span><span class="sxs-lookup"><span data-stu-id="7e20d-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="7e20d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7e20d-134">-Name</span></span>
<span data-ttu-id="7e20d-135">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7e20d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e20d-136">-ResourceGroupName</span></span>
<span data-ttu-id="7e20d-137">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7e20d-138">-지문</span><span class="sxs-lookup"><span data-stu-id="7e20d-138">-Thumbprint</span></span>
<span data-ttu-id="7e20d-139">클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="7e20d-140">-확인</span><span class="sxs-lookup"><span data-stu-id="7e20d-140">-Confirm</span></span>
<span data-ttu-id="7e20d-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e20d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e20d-142">-WhatIf</span></span>
<span data-ttu-id="7e20d-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e20d-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e20d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e20d-145">CommonParameters</span></span>
<span data-ttu-id="7e20d-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e20d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e20d-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e20d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e20d-148">입력</span><span class="sxs-lookup"><span data-stu-id="7e20d-148">INPUTS</span></span>

### <span data-ttu-id="7e20d-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7e20d-149">System.String</span></span>

## <span data-ttu-id="7e20d-150">출력</span><span class="sxs-lookup"><span data-stu-id="7e20d-150">OUTPUTS</span></span>

### <span data-ttu-id="7e20d-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="7e20d-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="7e20d-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e20d-152">NOTES</span></span>

## <span data-ttu-id="7e20d-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e20d-153">RELATED LINKS</span></span>
