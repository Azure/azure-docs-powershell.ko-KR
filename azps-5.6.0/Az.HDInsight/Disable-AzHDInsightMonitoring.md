---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 04e4a2e45f799367060c76e30807f75eaedb0465
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968992"
---
# <span data-ttu-id="bd8d4-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="bd8d4-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="bd8d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd8d4-102">SYNOPSIS</span></span>
<span data-ttu-id="bd8d4-103">HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정하면 관련 로그가 사용 중에 지정된 모니터링 작업 영역으로 흐르지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="bd8d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd8d4-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd8d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd8d4-105">DESCRIPTION</span></span>
<span data-ttu-id="bd8d4-106">**Disable-AzHDInsightMonitoring** cmdlet은 Azure HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="bd8d4-107">예제</span><span class="sxs-lookup"><span data-stu-id="bd8d4-107">EXAMPLES</span></span>

### <span data-ttu-id="bd8d4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd8d4-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="bd8d4-109">HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정하고 관련 로그가 모니터링 작업 영역으로 흐르는 것이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="bd8d4-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="bd8d4-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="bd8d4-111">HDInsight 클러스터에서 모니터링을 사용하지 않도록 설정하고 관련 로그가 모니터링 작업 영역으로 흐르는 것이 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="bd8d4-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd8d4-112">PARAMETERS</span></span>

### <span data-ttu-id="bd8d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd8d4-113">-DefaultProfile</span></span>
<span data-ttu-id="bd8d4-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd8d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd8d4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bd8d4-115">-Name</span></span>
<span data-ttu-id="bd8d4-116">모니터링을 사용하지 않도록 설정하는 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="bd8d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd8d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd8d4-118">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="bd8d4-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bd8d4-119">-Confirm</span></span>
<span data-ttu-id="bd8d4-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd8d4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd8d4-121">-WhatIf</span></span>
<span data-ttu-id="bd8d4-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd8d4-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd8d4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd8d4-124">CommonParameters</span></span>
<span data-ttu-id="bd8d4-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd8d4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd8d4-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd8d4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd8d4-127">입력</span><span class="sxs-lookup"><span data-stu-id="bd8d4-127">INPUTS</span></span>

### <span data-ttu-id="bd8d4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bd8d4-128">System.String</span></span>

## <span data-ttu-id="bd8d4-129">출력</span><span class="sxs-lookup"><span data-stu-id="bd8d4-129">OUTPUTS</span></span>

### <span data-ttu-id="bd8d4-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd8d4-130">System.Boolean</span></span>

## <span data-ttu-id="bd8d4-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd8d4-131">NOTES</span></span>

## <span data-ttu-id="bd8d4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd8d4-132">RELATED LINKS</span></span>
