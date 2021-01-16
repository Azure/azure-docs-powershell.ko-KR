---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326752"
---
# <span data-ttu-id="9e544-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="9e544-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="9e544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e544-102">SYNOPSIS</span></span>
<span data-ttu-id="9e544-103">HDInsight 클러스터에서 모니터링을 사용하도록 설정하면 사용하도록 설정하는 동안 지정된 모니터링 작업 영역으로 관련 로그가 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="9e544-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e544-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e544-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e544-105">DESCRIPTION</span></span>
<span data-ttu-id="9e544-106">**Enable-AzHDInsightMonitoring** cmdlet을 사용하면 Azure HDInsight 클러스터에서 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="9e544-107">예제</span><span class="sxs-lookup"><span data-stu-id="9e544-107">EXAMPLES</span></span>

### <span data-ttu-id="9e544-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e544-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="9e544-109">HDInsight 클러스터에서 모니터링을 사용하도록 설정하고 관련 로그는 ID가 1d364e89-bb71-4503-aa3d-a23535aea7bd인 모니터링 작업 영역으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="9e544-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e544-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="9e544-111">HDInsight 클러스터에서 모니터링을 사용하도록 설정하고 관련 로그는 ID가 1d364e89-bb71-4503-aa3d-a23535aea7bd인 모니터링 작업 영역으로 전송됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="9e544-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e544-112">PARAMETERS</span></span>

### <span data-ttu-id="9e544-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e544-113">-DefaultProfile</span></span>
<span data-ttu-id="9e544-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e544-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e544-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9e544-115">-Name</span></span>
<span data-ttu-id="9e544-116">모니터링을 사용하도록 설정할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="9e544-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9e544-117">-PrimaryKey</span></span>
<span data-ttu-id="9e544-118">모니터링 작업 영역의 기본 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e544-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e544-119">-ResourceGroupName</span></span>
<span data-ttu-id="9e544-120">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="9e544-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="9e544-121">-WorkspaceId</span></span>
<span data-ttu-id="9e544-122">모니터링 작업 영역의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e544-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e544-123">-Confirm</span></span>
<span data-ttu-id="9e544-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e544-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e544-125">-WhatIf</span></span>
<span data-ttu-id="9e544-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9e544-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e544-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e544-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e544-128">CommonParameters</span></span>
<span data-ttu-id="9e544-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e544-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e544-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e544-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e544-131">입력</span><span class="sxs-lookup"><span data-stu-id="9e544-131">INPUTS</span></span>

### <span data-ttu-id="9e544-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9e544-132">System.String</span></span>

## <span data-ttu-id="9e544-133">출력</span><span class="sxs-lookup"><span data-stu-id="9e544-133">OUTPUTS</span></span>

### <span data-ttu-id="9e544-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e544-134">System.Boolean</span></span>

## <span data-ttu-id="9e544-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e544-135">NOTES</span></span>

## <span data-ttu-id="9e544-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e544-136">RELATED LINKS</span></span>
