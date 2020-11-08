---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226177"
---
# <span data-ttu-id="b15b2-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b15b2-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="b15b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b15b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b15b2-103">인증서 일반 이름 또는 지문을 클러스터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="b15b2-104">이렇게 하면 클라이언트 인증을 위해 agains 인증서가 클러스터에 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="b15b2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="b15b2-105">SYNTAX</span></span>

### <span data-ttu-id="b15b2-106">ClientCertByTpByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="b15b2-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b15b2-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="b15b2-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b15b2-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="b15b2-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b15b2-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="b15b2-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b15b2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b15b2-110">DESCRIPTION</span></span>
<span data-ttu-id="b15b2-111">인증서 일반 이름 또는 지문을 클러스터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="b15b2-112">이렇게 하면 클라이언트 인증을 위해 agains 인증서가 클러스터에 등록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="b15b2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b15b2-113">EXAMPLES</span></span>

### <span data-ttu-id="b15b2-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="b15b2-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="b15b2-115">이 명령은 지문이 ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' 인 인증서를 클러스터에 추가 하므로 클라이언트가 관리자 권한으로이 인증서를 사용 하 여 클러스터와 통신할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="b15b2-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="b15b2-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="b15b2-117">이 명령은 일반 이름 ' Contoso.com ' 및 2 발급자 인 읽기 전용 클라이언트 인증서를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="b15b2-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="b15b2-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="b15b2-119">이 명령은 일반 이름이 ' Contoso.com '이 고 발급자가 2 인 읽기 전용 클라이언트 인증서를 파이핑에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="b15b2-120">변수</span><span class="sxs-lookup"><span data-stu-id="b15b2-120">PARAMETERS</span></span>

### <span data-ttu-id="b15b2-121">-관리자</span><span class="sxs-lookup"><span data-stu-id="b15b2-121">-Admin</span></span>
<span data-ttu-id="b15b2-122">클라이언트 인증서에 관리자 수준이 있는지 여부를 지정 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="b15b2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b15b2-123">-AsJob</span></span>
<span data-ttu-id="b15b2-124">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b15b2-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b15b2-125">-CommonName</span></span>
<span data-ttu-id="b15b2-126">클라이언트 인증서 일반 이름.</span><span class="sxs-lookup"><span data-stu-id="b15b2-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="b15b2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15b2-127">-DefaultProfile</span></span>
<span data-ttu-id="b15b2-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15b2-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b15b2-129">-InputObject</span></span>
<span data-ttu-id="b15b2-130">관리 되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="b15b2-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="b15b2-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b15b2-131">-IssuerThumbprint</span></span>
<span data-ttu-id="b15b2-132">클라이언트 인증서에 대 한 발급자 지문 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="b15b2-133">CommonName와 조합 하 여 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="b15b2-134">-이름</span><span class="sxs-lookup"><span data-stu-id="b15b2-134">-Name</span></span>
<span data-ttu-id="b15b2-135">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b15b2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15b2-136">-ResourceGroupName</span></span>
<span data-ttu-id="b15b2-137">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b15b2-138">-지문</span><span class="sxs-lookup"><span data-stu-id="b15b2-138">-Thumbprint</span></span>
<span data-ttu-id="b15b2-139">클라이언트 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="b15b2-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="b15b2-140">-확인</span><span class="sxs-lookup"><span data-stu-id="b15b2-140">-Confirm</span></span>
<span data-ttu-id="b15b2-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b15b2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15b2-142">-WhatIf</span></span>
<span data-ttu-id="b15b2-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b15b2-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b15b2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15b2-145">CommonParameters</span></span>
<span data-ttu-id="b15b2-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b15b2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15b2-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b15b2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15b2-148">입력</span><span class="sxs-lookup"><span data-stu-id="b15b2-148">INPUTS</span></span>

### <span data-ttu-id="b15b2-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b15b2-149">System.String</span></span>

## <span data-ttu-id="b15b2-150">출력</span><span class="sxs-lookup"><span data-stu-id="b15b2-150">OUTPUTS</span></span>

### <span data-ttu-id="b15b2-151">ServiceFabric. a m. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b15b2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b15b2-152">상속자</span><span class="sxs-lookup"><span data-stu-id="b15b2-152">NOTES</span></span>

## <span data-ttu-id="b15b2-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b15b2-153">RELATED LINKS</span></span>
