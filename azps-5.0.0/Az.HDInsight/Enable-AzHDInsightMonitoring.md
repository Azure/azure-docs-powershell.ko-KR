---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215379"
---
# <span data-ttu-id="4118e-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="4118e-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="4118e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4118e-102">SYNOPSIS</span></span>
<span data-ttu-id="4118e-103">HDInsight 클러스터에서 모니터링을 사용 하도록 설정 하 고, 사용 중에 지정 된 모니터링 작업 영역으로 관련 로그를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="4118e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4118e-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4118e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4118e-105">DESCRIPTION</span></span>
<span data-ttu-id="4118e-106">AzHDInsightMonitoring cmdlet을 **사용** 하면 Azure HDInsight 클러스터에서 모니터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4118e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4118e-107">EXAMPLES</span></span>

### <span data-ttu-id="4118e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4118e-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="4118e-109">HDInsight 클러스터에서 모니터링을 사용할 수 있으며, 관련 로그가 id 1d364e89-bb71-4503-aa3d-a23535aea7bd를 사용 하 여 모니터링 작업 영역으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="4118e-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="4118e-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="4118e-111">HDInsight 클러스터에서 모니터링을 사용할 수 있으며, 관련 로그가 id 1d364e89-bb71-4503-aa3d-a23535aea7bd를 사용 하 여 모니터링 작업 영역으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="4118e-112">변수</span><span class="sxs-lookup"><span data-stu-id="4118e-112">PARAMETERS</span></span>

### <span data-ttu-id="4118e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4118e-113">-DefaultProfile</span></span>
<span data-ttu-id="4118e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4118e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4118e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4118e-115">-Name</span></span>
<span data-ttu-id="4118e-116">모니터링을 사용할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="4118e-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4118e-117">-PrimaryKey</span></span>
<span data-ttu-id="4118e-118">모니터링 작업 영역의 기본 키입니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="4118e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4118e-119">-ResourceGroupName</span></span>
<span data-ttu-id="4118e-120">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="4118e-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4118e-121">-WorkspaceId</span></span>
<span data-ttu-id="4118e-122">모니터링 작업 영역의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="4118e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4118e-123">-Confirm</span></span>
<span data-ttu-id="4118e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4118e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4118e-125">-WhatIf</span></span>
<span data-ttu-id="4118e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4118e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4118e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4118e-128">CommonParameters</span></span>
<span data-ttu-id="4118e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4118e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4118e-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4118e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4118e-131">입력</span><span class="sxs-lookup"><span data-stu-id="4118e-131">INPUTS</span></span>

### <span data-ttu-id="4118e-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4118e-132">System.String</span></span>

## <span data-ttu-id="4118e-133">출력</span><span class="sxs-lookup"><span data-stu-id="4118e-133">OUTPUTS</span></span>

### <span data-ttu-id="4118e-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4118e-134">System.Boolean</span></span>

## <span data-ttu-id="4118e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4118e-135">NOTES</span></span>

## <span data-ttu-id="4118e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4118e-136">RELATED LINKS</span></span>
