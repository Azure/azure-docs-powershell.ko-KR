---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: 343c5c1a35334a25643aea576a9c545d1349e1f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873022"
---
# <span data-ttu-id="970f2-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="970f2-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="970f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="970f2-102">SYNOPSIS</span></span>
<span data-ttu-id="970f2-103">클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="970f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="970f2-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="970f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="970f2-105">DESCRIPTION</span></span>
<span data-ttu-id="970f2-106">**업데이트-AzServiceFabricReliability** 를 사용 하 여 클러스터의 기본 노드 유형의 안정성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="970f2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="970f2-107">EXAMPLES</span></span>

### <span data-ttu-id="970f2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="970f2-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="970f2-109">이 명령은 기본 노드 유형의 안정성 계층을 은색으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="970f2-110">변수</span><span class="sxs-lookup"><span data-stu-id="970f2-110">PARAMETERS</span></span>

### <span data-ttu-id="970f2-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="970f2-111">-AutoAddNode</span></span>
<span data-ttu-id="970f2-112">안정성을 변경할 때 노드 수 자동으로 추가</span><span class="sxs-lookup"><span data-stu-id="970f2-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="970f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="970f2-113">-DefaultProfile</span></span>
<span data-ttu-id="970f2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="970f2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="970f2-115">-Name</span></span>
<span data-ttu-id="970f2-116">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="970f2-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="970f2-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="970f2-117">-ReliabilityLevel</span></span>
<span data-ttu-id="970f2-118">안정성 계층</span><span class="sxs-lookup"><span data-stu-id="970f2-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="970f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="970f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="970f2-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="970f2-121">-확인</span><span class="sxs-lookup"><span data-stu-id="970f2-121">-Confirm</span></span>
<span data-ttu-id="970f2-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="970f2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="970f2-123">-WhatIf</span></span>
<span data-ttu-id="970f2-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="970f2-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="970f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970f2-126">CommonParameters</span></span>
<span data-ttu-id="970f2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="970f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970f2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="970f2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970f2-129">입력</span><span class="sxs-lookup"><span data-stu-id="970f2-129">INPUTS</span></span>

### <span data-ttu-id="970f2-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="970f2-130">System.String</span></span>

### <span data-ttu-id="970f2-131">ServiceFabric. ReliabilityLevel/.</span><span class="sxs-lookup"><span data-stu-id="970f2-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="970f2-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="970f2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="970f2-133">출력</span><span class="sxs-lookup"><span data-stu-id="970f2-133">OUTPUTS</span></span>

### <span data-ttu-id="970f2-134">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="970f2-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="970f2-135">상속자</span><span class="sxs-lookup"><span data-stu-id="970f2-135">NOTES</span></span>

## <span data-ttu-id="970f2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="970f2-136">RELATED LINKS</span></span>
