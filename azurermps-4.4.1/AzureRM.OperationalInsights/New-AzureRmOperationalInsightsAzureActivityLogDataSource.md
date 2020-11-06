---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 15138ee817cddb992f5b6bbe0beccee10620ffdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530740"
---
# <span data-ttu-id="15d5e-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="15d5e-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="15d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="15d5e-103">지정 된 구독에서 Azure Activity 로그를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15d5e-104">SYNTAX</span></span>

### <span data-ttu-id="15d5e-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="15d5e-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15d5e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="15d5e-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15d5e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="15d5e-107">DESCRIPTION</span></span>
<span data-ttu-id="15d5e-108">New-AzureRmOperationalInsightsAzureActivityLogDataSource에서 로그 분석을 사용 하 여 지정 된 구독에서 Azure 활동 로그를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="15d5e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15d5e-109">EXAMPLES</span></span>

### <span data-ttu-id="15d5e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="15d5e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="15d5e-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="15d5e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="15d5e-112">변수</span><span class="sxs-lookup"><span data-stu-id="15d5e-112">PARAMETERS</span></span>

### <span data-ttu-id="15d5e-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="15d5e-113">-BackfillStartTime</span></span>
<span data-ttu-id="15d5e-114">1 주일 전에 백필 로그를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d5e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="15d5e-115">-Force</span></span>
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

### <span data-ttu-id="15d5e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="15d5e-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d5e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15d5e-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d5e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15d5e-118">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d5e-119">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="15d5e-119">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15d5e-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15d5e-120">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15d5e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="15d5e-121">-Confirm</span></span>
<span data-ttu-id="15d5e-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15d5e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15d5e-123">-WhatIf</span></span>
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

### <span data-ttu-id="15d5e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d5e-124">-DefaultProfile</span></span>
<span data-ttu-id="15d5e-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d5e-126">CommonParameters</span></span>
<span data-ttu-id="15d5e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d5e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d5e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d5e-129">입력</span><span class="sxs-lookup"><span data-stu-id="15d5e-129">INPUTS</span></span>

### <span data-ttu-id="15d5e-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="15d5e-130">PSWorkspace</span></span>
<span data-ttu-id="15d5e-131">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="15d5e-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="15d5e-132">출력</span><span class="sxs-lookup"><span data-stu-id="15d5e-132">OUTPUTS</span></span>

### <span data-ttu-id="15d5e-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="15d5e-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="15d5e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="15d5e-134">NOTES</span></span>

## <span data-ttu-id="15d5e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15d5e-135">RELATED LINKS</span></span>

