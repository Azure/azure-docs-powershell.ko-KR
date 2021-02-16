---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207424"
---
# <span data-ttu-id="8c61f-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8c61f-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="8c61f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c61f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c61f-103">라우팅 규칙을 슬롯으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="8c61f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c61f-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c61f-105">설명</span><span class="sxs-lookup"><span data-stu-id="8c61f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c61f-106">**Update-AzWebAppTrafficRouting** cmdlet은 Azure 웹앱 슬롯에 대한 라우팅 규칙 구성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="8c61f-107">예제</span><span class="sxs-lookup"><span data-stu-id="8c61f-107">EXAMPLES</span></span>

### <span data-ttu-id="8c61f-108">예제 1 프로덕션 트래픽의 15%를 Stg 슬롯으로 전송하는 라우팅 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="8c61f-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="8c61f-109">이 명령은 프로덕션 트래픽의 15%를 Stg 슬롯으로 전송하는 라우팅 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="8c61f-110">예제 2 증분 방식으로 프로덕션 트래픽을 Stg 슬롯 범위로 전송하는 라우팅 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="8c61f-111">이 명령은 프로덕션 트래픽을 Stg 슬롯 범위에 전송하는 라우팅 규칙을 증분 방식으로 50%에서 90%로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="8c61f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c61f-112">PARAMETERS</span></span>

### <span data-ttu-id="8c61f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c61f-113">-DefaultProfile</span></span>
<span data-ttu-id="8c61f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c61f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c61f-115">-ResourceGroupName</span></span>
<span data-ttu-id="8c61f-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c61f-116">ResourceGroupName</span></span>
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

### <span data-ttu-id="8c61f-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="8c61f-117">-RoutingRule</span></span>
<span data-ttu-id="8c61f-118">웹앱 RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="8c61f-118">Web App RoutingRule.</span></span>
<span data-ttu-id="8c61f-119">예: -RoutingRule @{ActionHostName=$slot. DefaultHostName; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="8c61f-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="8c61f-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="8c61f-120">-WebAppName</span></span>
<span data-ttu-id="8c61f-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="8c61f-121">WebApp Name</span></span>

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

### <span data-ttu-id="8c61f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c61f-122">-Confirm</span></span>
<span data-ttu-id="8c61f-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c61f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c61f-124">-WhatIf</span></span>
<span data-ttu-id="8c61f-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8c61f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c61f-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c61f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c61f-127">CommonParameters</span></span>
<span data-ttu-id="8c61f-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c61f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c61f-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c61f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c61f-130">입력</span><span class="sxs-lookup"><span data-stu-id="8c61f-130">INPUTS</span></span>

### <span data-ttu-id="8c61f-131">없음</span><span class="sxs-lookup"><span data-stu-id="8c61f-131">None</span></span>

## <span data-ttu-id="8c61f-132">출력</span><span class="sxs-lookup"><span data-stu-id="8c61f-132">OUTPUTS</span></span>

### <span data-ttu-id="8c61f-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="8c61f-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="8c61f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c61f-134">NOTES</span></span>

## <span data-ttu-id="8c61f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c61f-135">RELATED LINKS</span></span>

[<span data-ttu-id="8c61f-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8c61f-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="8c61f-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8c61f-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="8c61f-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="8c61f-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)