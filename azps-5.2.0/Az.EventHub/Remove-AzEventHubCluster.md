---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353145"
---
# <span data-ttu-id="a22d5-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="a22d5-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="a22d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a22d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a22d5-103">ResourceGroup에서 지정된 Dedicated Eventhub 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="a22d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="a22d5-104">SYNTAX</span></span>

### <span data-ttu-id="a22d5-105">ClusterPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a22d5-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a22d5-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a22d5-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a22d5-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a22d5-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a22d5-108">설명</span><span class="sxs-lookup"><span data-stu-id="a22d5-108">DESCRIPTION</span></span>
<span data-ttu-id="a22d5-109">Remove-AzEventHubCluster cmdlet은 주어진 리소스 그룹에서 주어진 전용 eventhub 클러스터 이름을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="a22d5-110">예제</span><span class="sxs-lookup"><span data-stu-id="a22d5-110">EXAMPLES</span></span>

### <span data-ttu-id="a22d5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a22d5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="a22d5-112">리소스 그룹에서 Eventhub-Cluster-5557 클러스터를 RSG-Cluster27651 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="a22d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a22d5-113">PARAMETERS</span></span>

### <span data-ttu-id="a22d5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a22d5-114">-AsJob</span></span>
<span data-ttu-id="a22d5-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a22d5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a22d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22d5-116">-DefaultProfile</span></span>
<span data-ttu-id="a22d5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a22d5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a22d5-118">-InputObject</span></span>
<span data-ttu-id="a22d5-119">클러스터 개체</span><span class="sxs-lookup"><span data-stu-id="a22d5-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a22d5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a22d5-120">-Name</span></span>
<span data-ttu-id="a22d5-121">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="a22d5-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22d5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a22d5-122">-PassThru</span></span>
<span data-ttu-id="a22d5-123">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="a22d5-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a22d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a22d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a22d5-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a22d5-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22d5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a22d5-126">-ResourceId</span></span>
<span data-ttu-id="a22d5-127">클러스터 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a22d5-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22d5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a22d5-128">-Confirm</span></span>
<span data-ttu-id="a22d5-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a22d5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a22d5-130">-WhatIf</span></span>
<span data-ttu-id="a22d5-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a22d5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a22d5-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a22d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22d5-133">CommonParameters</span></span>
<span data-ttu-id="a22d5-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a22d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22d5-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a22d5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22d5-136">입력</span><span class="sxs-lookup"><span data-stu-id="a22d5-136">INPUTS</span></span>

### <span data-ttu-id="a22d5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a22d5-137">System.String</span></span>

### <span data-ttu-id="a22d5-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a22d5-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="a22d5-139">출력</span><span class="sxs-lookup"><span data-stu-id="a22d5-139">OUTPUTS</span></span>

### <span data-ttu-id="a22d5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a22d5-140">System.Boolean</span></span>

## <span data-ttu-id="a22d5-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a22d5-141">NOTES</span></span>

## <span data-ttu-id="a22d5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a22d5-142">RELATED LINKS</span></span>
