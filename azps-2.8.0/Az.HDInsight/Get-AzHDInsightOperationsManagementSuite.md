---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689828"
---
# <span data-ttu-id="fdd64-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="fdd64-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="fdd64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdd64-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd64-103">클러스터의 OMS (Operations Management Suite) 설치 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="fdd64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdd64-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdd64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fdd64-105">DESCRIPTION</span></span>
<span data-ttu-id="fdd64-106">**AzHDInsightOperationsManagementSuite** Cmdlet은 Azure HDInsight 클러스터에서 OMS 설치의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="fdd64-107">OMS를 사용 하는 경우에는 OMS 작업 영역 id도 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="fdd64-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fdd64-108">EXAMPLES</span></span>

### <span data-ttu-id="fdd64-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdd64-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="fdd64-110">ClusterMonitoringEnabled 속성이 true 이기 때문에 OMS (Operations Management Suite)가 클러스터에서 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="fdd64-111">로그가 흐르는 OMS 작업 영역 id가 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fdd64-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fdd64-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fdd64-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="fdd64-113">ClusterMonitoringEnabled 속성이 true 이기 때문에 OMS (Operations Management Suite)가 클러스터에서 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="fdd64-114">로그가 흐르는 OMS 작업 영역 id가 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="fdd64-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="fdd64-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="fdd64-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="fdd64-116">ClusterMonitoringEnabled 속성이 false 이기 때문에 OMS (Operations Management Suite)는 클러스터에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="fdd64-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="fdd64-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="fdd64-118">ClusterMonitoringEnabled 속성이 false 이기 때문에 OMS (Operations Management Suite)는 클러스터에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="fdd64-119">변수</span><span class="sxs-lookup"><span data-stu-id="fdd64-119">PARAMETERS</span></span>

### <span data-ttu-id="fdd64-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd64-120">-DefaultProfile</span></span>
<span data-ttu-id="fdd64-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fdd64-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdd64-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fdd64-122">-Name</span></span>
<span data-ttu-id="fdd64-123">OMS (Operations Management Suite) 상태를 가져올 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd64-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd64-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdd64-125">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-125">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="fdd64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd64-126">CommonParameters</span></span>
<span data-ttu-id="fdd64-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd64-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd64-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd64-129">입력</span><span class="sxs-lookup"><span data-stu-id="fdd64-129">INPUTS</span></span>

### <span data-ttu-id="fdd64-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdd64-130">System.String</span></span>

## <span data-ttu-id="fdd64-131">출력</span><span class="sxs-lookup"><span data-stu-id="fdd64-131">OUTPUTS</span></span>

### <span data-ttu-id="fdd64-132">AzureHDInsightOMS를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdd64-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="fdd64-133">상속자</span><span class="sxs-lookup"><span data-stu-id="fdd64-133">NOTES</span></span>

## <span data-ttu-id="fdd64-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdd64-134">RELATED LINKS</span></span>
