---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049058"
---
# <span data-ttu-id="6ad12-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ad12-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="6ad12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad12-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad12-103">HDInsight 클러스터의 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="6ad12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ad12-104">SYNTAX</span></span>

### <span data-ttu-id="6ad12-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ad12-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad12-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad12-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ad12-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ad12-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ad12-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ad12-108">DESCRIPTION</span></span>
<span data-ttu-id="6ad12-109">**AzHDInsightClusterAutoscaleConfiguration** Cmdlet은 HDInsight 클러스터의 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="6ad12-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ad12-110">EXAMPLES</span></span>

### <span data-ttu-id="6ad12-111">예제 1: HDInsight 클러스터의 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="6ad12-112">이 명령은 HDInsight 클러스터의 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="6ad12-113">변수</span><span class="sxs-lookup"><span data-stu-id="6ad12-113">PARAMETERS</span></span>

### <span data-ttu-id="6ad12-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ad12-114">-AsJob</span></span>
<span data-ttu-id="6ad12-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ad12-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ad12-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6ad12-116">-ClusterName</span></span>
<span data-ttu-id="6ad12-117">클러스터의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad12-118">-DefaultProfile</span></span>
<span data-ttu-id="6ad12-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ad12-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ad12-120">-InputObject</span></span>
<span data-ttu-id="6ad12-121">입력 개체를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad12-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ad12-123">리소스 그룹의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad12-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ad12-124">-ResourceId</span></span>
<span data-ttu-id="6ad12-125">리소스 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad12-126">-확인</span><span class="sxs-lookup"><span data-stu-id="6ad12-126">-Confirm</span></span>
<span data-ttu-id="6ad12-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ad12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ad12-128">-WhatIf</span></span>
<span data-ttu-id="6ad12-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ad12-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ad12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad12-131">CommonParameters</span></span>
<span data-ttu-id="6ad12-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ad12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad12-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ad12-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad12-134">입력</span><span class="sxs-lookup"><span data-stu-id="6ad12-134">INPUTS</span></span>

### <span data-ttu-id="6ad12-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ad12-135">System.String</span></span>

### <span data-ttu-id="6ad12-136">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="6ad12-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="6ad12-137">출력</span><span class="sxs-lookup"><span data-stu-id="6ad12-137">OUTPUTS</span></span>

### <span data-ttu-id="6ad12-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6ad12-138">System.Boolean</span></span>

## <span data-ttu-id="6ad12-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6ad12-139">NOTES</span></span>

## <span data-ttu-id="6ad12-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ad12-140">RELATED LINKS</span></span>

<span data-ttu-id="6ad12-141">[새로운 AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="6ad12-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
