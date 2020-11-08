---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215458"
---
# <span data-ttu-id="7e36e-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="7e36e-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="7e36e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e36e-102">SYNOPSIS</span></span>
<span data-ttu-id="7e36e-103">ResourceGroup에서 지정한 전용 Eventhub 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="7e36e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e36e-104">SYNTAX</span></span>

### <span data-ttu-id="7e36e-105">Cluster속성 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e36e-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e36e-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7e36e-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e36e-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e36e-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e36e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7e36e-108">DESCRIPTION</span></span>
<span data-ttu-id="7e36e-109">Remove-AzEventHubCluster cmdlet은 지정 된 resourcegroup에서 지정 된 전용 eventhub 클러스터 이름을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="7e36e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7e36e-110">EXAMPLES</span></span>

### <span data-ttu-id="7e36e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e36e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="7e36e-112">Eventhub-클러스터-5557 클러스터를 RSG-Cluster27651 resourcegroup에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="7e36e-113">변수</span><span class="sxs-lookup"><span data-stu-id="7e36e-113">PARAMETERS</span></span>

### <span data-ttu-id="7e36e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e36e-114">-AsJob</span></span>
<span data-ttu-id="7e36e-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7e36e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e36e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e36e-116">-DefaultProfile</span></span>
<span data-ttu-id="7e36e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e36e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e36e-118">-InputObject</span></span>
<span data-ttu-id="7e36e-119">클러스터 개체</span><span class="sxs-lookup"><span data-stu-id="7e36e-119">Cluster Object</span></span>

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

### <span data-ttu-id="7e36e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7e36e-120">-Name</span></span>
<span data-ttu-id="7e36e-121">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="7e36e-121">Cluster Name</span></span>

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

### <span data-ttu-id="7e36e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e36e-122">-PassThru</span></span>
<span data-ttu-id="7e36e-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="7e36e-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7e36e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e36e-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e36e-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7e36e-125">Resource Group Name</span></span>

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

### <span data-ttu-id="7e36e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e36e-126">-ResourceId</span></span>
<span data-ttu-id="7e36e-127">클러스터 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7e36e-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="7e36e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="7e36e-128">-Confirm</span></span>
<span data-ttu-id="7e36e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e36e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e36e-130">-WhatIf</span></span>
<span data-ttu-id="7e36e-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e36e-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e36e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e36e-133">CommonParameters</span></span>
<span data-ttu-id="7e36e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e36e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e36e-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e36e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e36e-136">입력</span><span class="sxs-lookup"><span data-stu-id="7e36e-136">INPUTS</span></span>

### <span data-ttu-id="7e36e-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e36e-137">System.String</span></span>

### <span data-ttu-id="7e36e-138">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="7e36e-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7e36e-139">출력</span><span class="sxs-lookup"><span data-stu-id="7e36e-139">OUTPUTS</span></span>

### <span data-ttu-id="7e36e-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7e36e-140">System.Boolean</span></span>

## <span data-ttu-id="7e36e-141">상속자</span><span class="sxs-lookup"><span data-stu-id="7e36e-141">NOTES</span></span>

## <span data-ttu-id="7e36e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e36e-142">RELATED LINKS</span></span>
