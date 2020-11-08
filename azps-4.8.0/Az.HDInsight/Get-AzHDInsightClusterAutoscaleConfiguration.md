---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056722"
---
# <span data-ttu-id="281f7-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="281f7-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="281f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="281f7-102">SYNOPSIS</span></span>
<span data-ttu-id="281f7-103">HDInsight 클러스터의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="281f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="281f7-104">SYNTAX</span></span>

### <span data-ttu-id="281f7-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="281f7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="281f7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="281f7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="281f7-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="281f7-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="281f7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="281f7-108">DESCRIPTION</span></span>
<span data-ttu-id="281f7-109">**AzHDInsightClusterAutoscaleConfiguration** Cmdlet은 HDInsight 클러스터의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="281f7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="281f7-110">EXAMPLES</span></span>

### <span data-ttu-id="281f7-111">예제 1: HDInsight 클러스터의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="281f7-112">이 명령은 HDInsight 클러스터의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="281f7-113">변수</span><span class="sxs-lookup"><span data-stu-id="281f7-113">PARAMETERS</span></span>

### <span data-ttu-id="281f7-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="281f7-114">-ClusterName</span></span>
<span data-ttu-id="281f7-115">클러스터의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="281f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281f7-116">-DefaultProfile</span></span>
<span data-ttu-id="281f7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="281f7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="281f7-118">-InputObject</span></span>
<span data-ttu-id="281f7-119">입력 개체를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="281f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="281f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="281f7-121">리소스 그룹의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="281f7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="281f7-122">-ResourceId</span></span>
<span data-ttu-id="281f7-123">리소스 id를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="281f7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281f7-124">CommonParameters</span></span>
<span data-ttu-id="281f7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="281f7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281f7-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="281f7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281f7-127">입력</span><span class="sxs-lookup"><span data-stu-id="281f7-127">INPUTS</span></span>

### <span data-ttu-id="281f7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="281f7-128">System.String</span></span>

### <span data-ttu-id="281f7-129">AzureHDInsightCluster의. m m.</span><span class="sxs-lookup"><span data-stu-id="281f7-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="281f7-130">출력</span><span class="sxs-lookup"><span data-stu-id="281f7-130">OUTPUTS</span></span>

### <span data-ttu-id="281f7-131">AzureHDInsightAutoscale의. m m.</span><span class="sxs-lookup"><span data-stu-id="281f7-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="281f7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="281f7-132">NOTES</span></span>

## <span data-ttu-id="281f7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="281f7-133">RELATED LINKS</span></span>

<span data-ttu-id="281f7-134">[새로운 AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [제거-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="281f7-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
