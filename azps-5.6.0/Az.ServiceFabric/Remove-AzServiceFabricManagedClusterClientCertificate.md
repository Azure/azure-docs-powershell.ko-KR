---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: f0ba5cb4d461bbc70ba742ae46ba4b9489923545
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005483"
---
# <span data-ttu-id="59339-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="59339-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="59339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59339-102">SYNOPSIS</span></span>
<span data-ttu-id="59339-103">지문 또는 일반적인 이름으로 클라이언트 인증서를 Remvoe합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="59339-104">구문</span><span class="sxs-lookup"><span data-stu-id="59339-104">SYNTAX</span></span>

### <span data-ttu-id="59339-105">ClientCertByTpByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="59339-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59339-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="59339-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59339-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="59339-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59339-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="59339-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59339-109">설명</span><span class="sxs-lookup"><span data-stu-id="59339-109">DESCRIPTION</span></span>
<span data-ttu-id="59339-110">지문 또는 일반적인 이름으로 클라이언트 인증서를 Remvoe합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="59339-111">예제</span><span class="sxs-lookup"><span data-stu-id="59339-111">EXAMPLES</span></span>

### <span data-ttu-id="59339-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="59339-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="59339-113">일반적인 이름으로 클라이언트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="59339-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="59339-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="59339-115">지문으로 클라이언트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="59339-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="59339-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="59339-117">배관을 사용하여 지문으로 클라이언트 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="59339-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="59339-118">PARAMETERS</span></span>

### <span data-ttu-id="59339-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59339-119">-AsJob</span></span>
<span data-ttu-id="59339-120">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="59339-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="59339-121">-CommonName</span></span>
<span data-ttu-id="59339-122">클라이언트 인증서 일반 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59339-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="59339-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59339-123">-DefaultProfile</span></span>
<span data-ttu-id="59339-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59339-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59339-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59339-125">-InputObject</span></span>
<span data-ttu-id="59339-126">관리되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="59339-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="59339-127">-Name</span><span class="sxs-lookup"><span data-stu-id="59339-127">-Name</span></span>
<span data-ttu-id="59339-128">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59339-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59339-129">-PassThru</span></span>
<span data-ttu-id="59339-130">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="59339-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="59339-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59339-131">-ResourceGroupName</span></span>
<span data-ttu-id="59339-132">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59339-133">-지문</span><span class="sxs-lookup"><span data-stu-id="59339-133">-Thumbprint</span></span>
<span data-ttu-id="59339-134">클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="59339-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59339-135">-확인</span><span class="sxs-lookup"><span data-stu-id="59339-135">-Confirm</span></span>
<span data-ttu-id="59339-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59339-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59339-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59339-137">-WhatIf</span></span>
<span data-ttu-id="59339-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="59339-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59339-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59339-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59339-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59339-140">CommonParameters</span></span>
<span data-ttu-id="59339-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59339-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59339-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59339-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59339-143">입력</span><span class="sxs-lookup"><span data-stu-id="59339-143">INPUTS</span></span>

### <span data-ttu-id="59339-144">System.String</span><span class="sxs-lookup"><span data-stu-id="59339-144">System.String</span></span>

## <span data-ttu-id="59339-145">출력</span><span class="sxs-lookup"><span data-stu-id="59339-145">OUTPUTS</span></span>

### <span data-ttu-id="59339-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="59339-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="59339-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59339-147">NOTES</span></span>

## <span data-ttu-id="59339-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59339-148">RELATED LINKS</span></span>
