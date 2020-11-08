---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217571"
---
# <span data-ttu-id="791ac-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="791ac-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="791ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="791ac-102">SYNOPSIS</span></span>
<span data-ttu-id="791ac-103">클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="791ac-103">update cluster</span></span>

## <span data-ttu-id="791ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="791ac-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="791ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="791ac-105">DESCRIPTION</span></span>
<span data-ttu-id="791ac-106">클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="791ac-106">update cluster</span></span>

## <span data-ttu-id="791ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="791ac-107">EXAMPLES</span></span>

### <span data-ttu-id="791ac-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="791ac-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="791ac-109">키 자격 증명 정보 및 sku로 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="791ac-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="791ac-110">변수</span><span class="sxs-lookup"><span data-stu-id="791ac-110">PARAMETERS</span></span>

### <span data-ttu-id="791ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="791ac-111">-AsJob</span></span>
<span data-ttu-id="791ac-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="791ac-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="791ac-113">-ClusterName</span></span>
<span data-ttu-id="791ac-114">클러스터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791ac-115">-DefaultProfile</span></span>
<span data-ttu-id="791ac-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="791ac-117">-KeyName</span></span>
<span data-ttu-id="791ac-118">키 이름</span><span class="sxs-lookup"><span data-stu-id="791ac-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="791ac-119">-KeyVaultUri</span></span>
<span data-ttu-id="791ac-120">이 keyvault에 대해 키 자격 증명 Uri, "보호 제거" 및 "소프트 삭제"를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="791ac-121">-KeyVersion</span></span>
<span data-ttu-id="791ac-122">키 버전</span><span class="sxs-lookup"><span data-stu-id="791ac-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="791ac-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="791ac-125">-SkuCapacity</span></span>
<span data-ttu-id="791ac-126">Sku 용량</span><span class="sxs-lookup"><span data-stu-id="791ac-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-127">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="791ac-127">-SkuName</span></span>
<span data-ttu-id="791ac-128">Sku 이름-이제 ' CapacityReservation ' 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-128">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-129">태그</span><span class="sxs-lookup"><span data-stu-id="791ac-129">-Tags</span></span>
<span data-ttu-id="791ac-130">클러스터의 태그</span><span class="sxs-lookup"><span data-stu-id="791ac-130">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-131">-확인</span><span class="sxs-lookup"><span data-stu-id="791ac-131">-Confirm</span></span>
<span data-ttu-id="791ac-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="791ac-133">-WhatIf</span></span>
<span data-ttu-id="791ac-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="791ac-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791ac-136">CommonParameters</span></span>
<span data-ttu-id="791ac-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="791ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791ac-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="791ac-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791ac-139">입력</span><span class="sxs-lookup"><span data-stu-id="791ac-139">INPUTS</span></span>

### <span data-ttu-id="791ac-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="791ac-140">System.String</span></span>

## <span data-ttu-id="791ac-141">출력</span><span class="sxs-lookup"><span data-stu-id="791ac-141">OUTPUTS</span></span>

### <span data-ttu-id="791ac-142">OperationalInsights. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="791ac-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="791ac-143">상속자</span><span class="sxs-lookup"><span data-stu-id="791ac-143">NOTES</span></span>

## <span data-ttu-id="791ac-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="791ac-144">RELATED LINKS</span></span>
