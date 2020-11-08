---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213954"
---
# <span data-ttu-id="f96ae-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f96ae-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="f96ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f96ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f96ae-103">Remvoe는 손도장 또는 일반 이름으로 클라이언트 인증서를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="f96ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f96ae-104">SYNTAX</span></span>

### <span data-ttu-id="f96ae-105">ClientCertByTpByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="f96ae-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f96ae-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="f96ae-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f96ae-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="f96ae-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f96ae-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="f96ae-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f96ae-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f96ae-109">DESCRIPTION</span></span>
<span data-ttu-id="f96ae-110">Remvoe는 손도장 또는 일반 이름으로 클라이언트 인증서를 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="f96ae-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f96ae-111">EXAMPLES</span></span>

### <span data-ttu-id="f96ae-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f96ae-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="f96ae-113">일반 이름으로 클라이언트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="f96ae-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f96ae-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f96ae-115">지문을 기준으로 클라이언트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="f96ae-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="f96ae-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f96ae-117">파이핑에서 클라이언트 인증서를 지문을 사용 하 여 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="f96ae-118">변수</span><span class="sxs-lookup"><span data-stu-id="f96ae-118">PARAMETERS</span></span>

### <span data-ttu-id="f96ae-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f96ae-119">-AsJob</span></span>
<span data-ttu-id="f96ae-120">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f96ae-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="f96ae-121">-CommonName</span></span>
<span data-ttu-id="f96ae-122">클라이언트 인증서 일반 이름.</span><span class="sxs-lookup"><span data-stu-id="f96ae-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="f96ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96ae-123">-DefaultProfile</span></span>
<span data-ttu-id="f96ae-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f96ae-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f96ae-125">-InputObject</span></span>
<span data-ttu-id="f96ae-126">관리 되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="f96ae-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="f96ae-127">-이름</span><span class="sxs-lookup"><span data-stu-id="f96ae-127">-Name</span></span>
<span data-ttu-id="f96ae-128">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f96ae-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f96ae-129">-PassThru</span></span>
<span data-ttu-id="f96ae-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="f96ae-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f96ae-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f96ae-131">-ResourceGroupName</span></span>
<span data-ttu-id="f96ae-132">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f96ae-133">-지문</span><span class="sxs-lookup"><span data-stu-id="f96ae-133">-Thumbprint</span></span>
<span data-ttu-id="f96ae-134">클라이언트 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="f96ae-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="f96ae-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f96ae-135">-Confirm</span></span>
<span data-ttu-id="f96ae-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f96ae-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f96ae-137">-WhatIf</span></span>
<span data-ttu-id="f96ae-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f96ae-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f96ae-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96ae-140">CommonParameters</span></span>
<span data-ttu-id="f96ae-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f96ae-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96ae-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f96ae-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96ae-143">입력</span><span class="sxs-lookup"><span data-stu-id="f96ae-143">INPUTS</span></span>

### <span data-ttu-id="f96ae-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f96ae-144">System.String</span></span>

## <span data-ttu-id="f96ae-145">출력</span><span class="sxs-lookup"><span data-stu-id="f96ae-145">OUTPUTS</span></span>

### <span data-ttu-id="f96ae-146">ServiceFabric. a m. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="f96ae-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="f96ae-147">상속자</span><span class="sxs-lookup"><span data-stu-id="f96ae-147">NOTES</span></span>

## <span data-ttu-id="f96ae-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f96ae-148">RELATED LINKS</span></span>
