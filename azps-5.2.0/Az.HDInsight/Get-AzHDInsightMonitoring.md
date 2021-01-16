---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338234"
---
# <span data-ttu-id="ecca3-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ecca3-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="ecca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecca3-102">SYNOPSIS</span></span>
<span data-ttu-id="ecca3-103">클러스터의 모니터링 설치 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="ecca3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecca3-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecca3-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecca3-105">DESCRIPTION</span></span>
<span data-ttu-id="ecca3-106">**Get-AzHDInsightMonitoring** cmdlet은 Azure HDInsight 클러스터에서 설치 모니터링 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="ecca3-107">모니터링을 사용하도록 설정하면 로그 분석 작업 영역 ID도 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="ecca3-108">예제</span><span class="sxs-lookup"><span data-stu-id="ecca3-108">EXAMPLES</span></span>

### <span data-ttu-id="ecca3-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ecca3-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="ecca3-110">ClusterMonitoringEnabled 속성이 true이기 때문에 클러스터에서 모니터링이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="ecca3-111">로그가 흐르는 모니터링 작업 영역 ID는 1d364e89-bb71-4503-aa3d-a23535aea7bd입니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="ecca3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ecca3-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="ecca3-113">ClusterMonitoringEnabled 속성이 true이기 때문에 클러스터에서 모니터링이 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="ecca3-114">로그가 흐르는 모니터링 작업 영역 ID는 1d364e89-bb71-4503-aa3d-a23535aea7bd입니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="ecca3-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="ecca3-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="ecca3-116">ClusterMonitoringEnabled 속성이 false이기 때문에 클러스터에서 모니터링이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="ecca3-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="ecca3-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="ecca3-118">ClusterMonitoringEnabled 속성이 false이기 때문에 클러스터에서 모니터링이 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="ecca3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecca3-119">PARAMETERS</span></span>

### <span data-ttu-id="ecca3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecca3-120">-DefaultProfile</span></span>
<span data-ttu-id="ecca3-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ecca3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecca3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ecca3-122">-Name</span></span>
<span data-ttu-id="ecca3-123">모니터링 상태를 얻을 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-123">The name of the cluster to get the status of monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecca3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecca3-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecca3-125">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecca3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecca3-126">CommonParameters</span></span>
<span data-ttu-id="ecca3-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecca3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecca3-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecca3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecca3-129">입력</span><span class="sxs-lookup"><span data-stu-id="ecca3-129">INPUTS</span></span>

### <span data-ttu-id="ecca3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ecca3-130">System.String</span></span>

## <span data-ttu-id="ecca3-131">출력</span><span class="sxs-lookup"><span data-stu-id="ecca3-131">OUTPUTS</span></span>

### <span data-ttu-id="ecca3-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="ecca3-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="ecca3-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecca3-133">NOTES</span></span>

## <span data-ttu-id="ecca3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecca3-134">RELATED LINKS</span></span>
