---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: d4b184dfbf834822110369e40fbbfb4eb168e424
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056349"
---
# <span data-ttu-id="ad41e-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="ad41e-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="ad41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad41e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad41e-103">HDInsight 클러스터의 특정 호스트를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="ad41e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad41e-104">SYNTAX</span></span>

### <span data-ttu-id="ad41e-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad41e-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [[-DefaultProfile] <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad41e-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad41e-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [[-DefaultProfile] <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad41e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ad41e-107">DESCRIPTION</span></span>
<span data-ttu-id="ad41e-108">AzHDInsightHost cmdlet을 **다시 시작** 하면 HDInsight 클러스터의 특정 호스트가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="ad41e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ad41e-109">EXAMPLES</span></span>

### <span data-ttu-id="ad41e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad41e-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="ad41e-111">이 명령은 worknode1, worknode2 클러스터의 호스트 두 개를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="ad41e-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ad41e-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="ad41e-113">이 명령은 cmdlet ' Get-AzHDInsightHost '와 상호 작용 하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="ad41e-114">변수</span><span class="sxs-lookup"><span data-stu-id="ad41e-114">PARAMETERS</span></span>

### <span data-ttu-id="ad41e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad41e-115">-AsJob</span></span>
<span data-ttu-id="ad41e-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ad41e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad41e-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="ad41e-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="ad41e-118">호스트의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad41e-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ad41e-119">-ClusterName</span></span>
<span data-ttu-id="ad41e-120">클러스터의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="ad41e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad41e-121">-DefaultProfile</span></span>
<span data-ttu-id="ad41e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad41e-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ad41e-123">-Name</span></span>
<span data-ttu-id="ad41e-124">호스트의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad41e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad41e-125">-PassThru</span></span>
<span data-ttu-id="ad41e-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="ad41e-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ad41e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad41e-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad41e-128">리소스 그룹의 이름을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad41e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="ad41e-129">-Confirm</span></span>
<span data-ttu-id="ad41e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad41e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad41e-131">-WhatIf</span></span>
<span data-ttu-id="ad41e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad41e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad41e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad41e-134">CommonParameters</span></span>
<span data-ttu-id="ad41e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad41e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad41e-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad41e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad41e-137">입력</span><span class="sxs-lookup"><span data-stu-id="ad41e-137">INPUTS</span></span>

### <span data-ttu-id="ad41e-138">System.webserver. IList ' 1 [[AzureHDInsightHostInfo, Microsoft azure. 3.2.0.0,, Culture = 중립, PublicKeyToken = null]],  \*. t e.</span><span class="sxs-lookup"><span data-stu-id="ad41e-138">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo, Microsoft.Azure.PowerShell.Cmdlets.HDInsight, Version=3.2.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ad41e-139">출력</span><span class="sxs-lookup"><span data-stu-id="ad41e-139">OUTPUTS</span></span>

### <span data-ttu-id="ad41e-140">Microsoft. Azure. 관리. 클러스터</span><span class="sxs-lookup"><span data-stu-id="ad41e-140">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="ad41e-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ad41e-141">NOTES</span></span>

## <span data-ttu-id="ad41e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad41e-142">RELATED LINKS</span></span>
