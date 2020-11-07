---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightMonitoring.md
ms.openlocfilehash: 2d91c96d20797988a7def2d11d633f36b08cb8cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879806"
---
# <span data-ttu-id="aadc0-101">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="aadc0-101">Get-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="aadc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aadc0-102">SYNOPSIS</span></span>
<span data-ttu-id="aadc0-103">클러스터의 설치 모니터링 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-103">Gets the status of monitoring installation on the cluster.</span></span>

## <span data-ttu-id="aadc0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aadc0-104">SYNTAX</span></span>

```
Get-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aadc0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aadc0-105">DESCRIPTION</span></span>
<span data-ttu-id="aadc0-106">**AzHDInsightMonitoring** Cmdlet은 Azure HDInsight 클러스터에서의 모니터링 설치 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-106">The **Get-AzHDInsightMonitoring** cmdlet gets the status of monitoring installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="aadc0-107">모니터링을 사용 하도록 설정 하면 로그 분석 작업 영역 id도 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-107">If monitoring is enabled then it will also return the log analytics workspace id.</span></span>

## <span data-ttu-id="aadc0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="aadc0-108">EXAMPLES</span></span>

### <span data-ttu-id="aadc0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="aadc0-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="aadc0-110">ClusterMonitoringEnabled 속성이 true 이기 때문에 클러스터에서 모니터링을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-110">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="aadc0-111">로그가 흐르는 모니터링 작업 영역 id가 1d364e89-bb71-4503-aa3d-a23535aea7bd.</span><span class="sxs-lookup"><span data-stu-id="aadc0-111">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="aadc0-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="aadc0-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="aadc0-113">ClusterMonitoringEnabled 속성이 true 이기 때문에 클러스터에서 모니터링을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-113">Monitoring is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="aadc0-114">로그가 흐르는 모니터링 작업 영역 id가 1d364e89-bb71-4503-aa3d-a23535aea7bd.</span><span class="sxs-lookup"><span data-stu-id="aadc0-114">The monitoring workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="aadc0-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="aadc0-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="aadc0-116">ClusterMonitoringEnabled 속성이 false 이기 때문에 클러스터에서 모니터링을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-116">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="aadc0-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="aadc0-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

{'ClusterMonitoringEnabled':'false', 'workspaceId': null}
```

<span data-ttu-id="aadc0-118">ClusterMonitoringEnabled 속성이 false 이기 때문에 클러스터에서 모니터링을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-118">Monitoring is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="aadc0-119">변수</span><span class="sxs-lookup"><span data-stu-id="aadc0-119">PARAMETERS</span></span>

### <span data-ttu-id="aadc0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadc0-120">-DefaultProfile</span></span>
<span data-ttu-id="aadc0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aadc0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aadc0-122">-이름</span><span class="sxs-lookup"><span data-stu-id="aadc0-122">-Name</span></span>
<span data-ttu-id="aadc0-123">모니터링 상태를 얻을 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-123">The name of the cluster to get the status of monitoring.</span></span>

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

### <span data-ttu-id="aadc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aadc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="aadc0-125">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="aadc0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadc0-126">CommonParameters</span></span>
<span data-ttu-id="aadc0-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadc0-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aadc0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadc0-129">입력</span><span class="sxs-lookup"><span data-stu-id="aadc0-129">INPUTS</span></span>

### <span data-ttu-id="aadc0-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aadc0-130">System.String</span></span>

## <span data-ttu-id="aadc0-131">출력</span><span class="sxs-lookup"><span data-stu-id="aadc0-131">OUTPUTS</span></span>

### <span data-ttu-id="aadc0-132">AzureHDInsightMonitoring를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="aadc0-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightMonitoring</span></span>

## <span data-ttu-id="aadc0-133">상속자</span><span class="sxs-lookup"><span data-stu-id="aadc0-133">NOTES</span></span>

## <span data-ttu-id="aadc0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aadc0-134">RELATED LINKS</span></span>
