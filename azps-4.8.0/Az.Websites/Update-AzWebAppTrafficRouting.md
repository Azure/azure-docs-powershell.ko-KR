---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213121"
---
# <span data-ttu-id="3a7cc-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a7cc-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="3a7cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7cc-103">라우팅 규칙을 슬롯에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="3a7cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a7cc-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a7cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3a7cc-105">DESCRIPTION</span></span>
<span data-ttu-id="3a7cc-106">**업데이트 AzWebAppTrafficRouting** Cmdlet은 Azure Web App 슬롯에 대 한 라우팅 규칙 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="3a7cc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3a7cc-107">EXAMPLES</span></span>

### <span data-ttu-id="3a7cc-108">예제 1 프로덕션 traffice의 15%를 Stg 슬롯으로 전송 하도록 라우팅 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="3a7cc-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="3a7cc-109">이 명령은 실제 사용량의 15%를 Stg 슬롯으로 전송 하도록 라우팅 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="3a7cc-110">예제 2 증분 방식으로 프로덕션 traffice을 Stg 슬롯 범위에서 50%에서 90%까지 전송 하도록 라우팅 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="3a7cc-111">이 명령은 증분 방식으로 프로덕션 traffice을 Stg 슬롯 범위에서 50%에서 90%까지 전송 하도록 라우팅 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="3a7cc-112">변수</span><span class="sxs-lookup"><span data-stu-id="3a7cc-112">PARAMETERS</span></span>

### <span data-ttu-id="3a7cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7cc-113">-DefaultProfile</span></span>
<span data-ttu-id="3a7cc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a7cc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a7cc-115">-ResourceGroupName</span></span>
<span data-ttu-id="3a7cc-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a7cc-116">ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a7cc-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a7cc-117">-RoutingRule</span></span>
<span data-ttu-id="3a7cc-118">웹 앱 RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-118">Web App RoutingRule.</span></span>
<span data-ttu-id="3a7cc-119">예:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage Name = $slotName}</span><span class="sxs-lookup"><span data-stu-id="3a7cc-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a7cc-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3a7cc-120">-WebAppName</span></span>
<span data-ttu-id="3a7cc-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="3a7cc-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a7cc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="3a7cc-122">-Confirm</span></span>
<span data-ttu-id="3a7cc-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a7cc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a7cc-124">-WhatIf</span></span>
<span data-ttu-id="3a7cc-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a7cc-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a7cc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7cc-127">CommonParameters</span></span>
<span data-ttu-id="3a7cc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7cc-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7cc-130">입력</span><span class="sxs-lookup"><span data-stu-id="3a7cc-130">INPUTS</span></span>

### <span data-ttu-id="3a7cc-131">않아야</span><span class="sxs-lookup"><span data-stu-id="3a7cc-131">None</span></span>

## <span data-ttu-id="3a7cc-132">출력</span><span class="sxs-lookup"><span data-stu-id="3a7cc-132">OUTPUTS</span></span>

### <span data-ttu-id="3a7cc-133">RampUpRule/. m i.</span><span class="sxs-lookup"><span data-stu-id="3a7cc-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="3a7cc-134">상속자</span><span class="sxs-lookup"><span data-stu-id="3a7cc-134">NOTES</span></span>

## <span data-ttu-id="3a7cc-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a7cc-135">RELATED LINKS</span></span>

[<span data-ttu-id="3a7cc-136">추가-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a7cc-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3a7cc-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a7cc-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3a7cc-138">제거-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3a7cc-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)