---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215862"
---
# <span data-ttu-id="89ae5-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="89ae5-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="89ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="89ae5-103">클러스터 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-103">Remove cluster resource.</span></span>

## <span data-ttu-id="89ae5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89ae5-104">SYNTAX</span></span>

### <span data-ttu-id="89ae5-105">ByObj (기본값)</span><span class="sxs-lookup"><span data-stu-id="89ae5-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ae5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="89ae5-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ae5-107">ById</span><span class="sxs-lookup"><span data-stu-id="89ae5-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ae5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="89ae5-108">DESCRIPTION</span></span>
<span data-ttu-id="89ae5-109">클러스터 제거 이렇게 하면 클러스터의 노드 유형도 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="89ae5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="89ae5-110">EXAMPLES</span></span>

### <span data-ttu-id="89ae5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="89ae5-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="89ae5-112">클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-112">Remove cluster.</span></span>

### <span data-ttu-id="89ae5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="89ae5-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="89ae5-114">파이프를 사용 하 여 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="89ae5-115">변수</span><span class="sxs-lookup"><span data-stu-id="89ae5-115">PARAMETERS</span></span>

### <span data-ttu-id="89ae5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89ae5-116">-AsJob</span></span>
<span data-ttu-id="89ae5-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="89ae5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ae5-118">-DefaultProfile</span></span>
<span data-ttu-id="89ae5-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ae5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ae5-120">-InputObject</span></span>
<span data-ttu-id="89ae5-121">관리 되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="89ae5-121">Managed Cluster resource</span></span>

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

### <span data-ttu-id="89ae5-122">-이름</span><span class="sxs-lookup"><span data-stu-id="89ae5-122">-Name</span></span>
<span data-ttu-id="89ae5-123">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ae5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89ae5-124">-PassThru</span></span>
<span data-ttu-id="89ae5-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="89ae5-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="89ae5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ae5-126">-ResourceGroupName</span></span>
<span data-ttu-id="89ae5-127">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ae5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ae5-128">-ResourceId</span></span>
<span data-ttu-id="89ae5-129">관리 되는 클러스터 리소스 id</span><span class="sxs-lookup"><span data-stu-id="89ae5-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89ae5-130">-확인</span><span class="sxs-lookup"><span data-stu-id="89ae5-130">-Confirm</span></span>
<span data-ttu-id="89ae5-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ae5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ae5-132">-WhatIf</span></span>
<span data-ttu-id="89ae5-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ae5-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ae5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ae5-135">CommonParameters</span></span>
<span data-ttu-id="89ae5-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ae5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ae5-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89ae5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ae5-138">입력</span><span class="sxs-lookup"><span data-stu-id="89ae5-138">INPUTS</span></span>

### <span data-ttu-id="89ae5-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89ae5-139">System.String</span></span>

## <span data-ttu-id="89ae5-140">출력</span><span class="sxs-lookup"><span data-stu-id="89ae5-140">OUTPUTS</span></span>

### <span data-ttu-id="89ae5-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="89ae5-141">System.Boolean</span></span>

## <span data-ttu-id="89ae5-142">상속자</span><span class="sxs-lookup"><span data-stu-id="89ae5-142">NOTES</span></span>

## <span data-ttu-id="89ae5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89ae5-143">RELATED LINKS</span></span>
