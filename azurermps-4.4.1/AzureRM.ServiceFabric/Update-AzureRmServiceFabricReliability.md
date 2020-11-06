---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: c8ee3324f7f6e7653d86bef747bdb9831982474e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529125"
---
# <span data-ttu-id="ab8f6-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ab8f6-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="ab8f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8f6-103">클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab8f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab8f6-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab8f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ab8f6-106">**업데이트-AzureRmServiceFabricReliability** 를 사용 하 여 클러스터의 기본 노드 유형의 안정성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="ab8f6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab8f6-107">EXAMPLES</span></span>

### <span data-ttu-id="ab8f6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab8f6-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="ab8f6-109">이 명령은 기본 노드 유형의 안정성 계층을 은색으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="ab8f6-110">변수</span><span class="sxs-lookup"><span data-stu-id="ab8f6-110">PARAMETERS</span></span>

### <span data-ttu-id="ab8f6-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="ab8f6-111">-AutoAddNode</span></span>
<span data-ttu-id="ab8f6-112">안정성을 변경할 때 노드 수를 자동으로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="ab8f6-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ab8f6-113">-Name</span></span>
<span data-ttu-id="ab8f6-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ab8f6-115">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ab8f6-115">-ReliabilityLevel</span></span>
<span data-ttu-id="ab8f6-116">안정성 계층.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-116">Reliability tier.</span></span>

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

### <span data-ttu-id="ab8f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab8f6-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ab8f6-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ab8f6-119">-Confirm</span></span>
<span data-ttu-id="ab8f6-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab8f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab8f6-121">-WhatIf</span></span>
<span data-ttu-id="ab8f6-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab8f6-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab8f6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8f6-124">-DefaultProfile</span></span>
<span data-ttu-id="ab8f6-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8f6-126">CommonParameters</span></span>
<span data-ttu-id="ab8f6-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8f6-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8f6-129">입력</span><span class="sxs-lookup"><span data-stu-id="ab8f6-129">INPUTS</span></span>

### <span data-ttu-id="ab8f6-130">ServiceFabric. ReliabilityLevel/.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="ab8f6-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ab8f6-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="ab8f6-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab8f6-132">System.String</span></span>

## <span data-ttu-id="ab8f6-133">출력</span><span class="sxs-lookup"><span data-stu-id="ab8f6-133">OUTPUTS</span></span>

### <span data-ttu-id="ab8f6-134">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="ab8f6-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="ab8f6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ab8f6-135">NOTES</span></span>

## <span data-ttu-id="ab8f6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab8f6-136">RELATED LINKS</span></span>

