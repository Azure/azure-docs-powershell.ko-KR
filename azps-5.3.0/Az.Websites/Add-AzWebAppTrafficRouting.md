---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380815"
---
# <span data-ttu-id="f14ba-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f14ba-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="f14ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f14ba-102">SYNOPSIS</span></span>
<span data-ttu-id="f14ba-103">슬롯에 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="f14ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="f14ba-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f14ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="f14ba-105">DESCRIPTION</span></span>
<span data-ttu-id="f14ba-106">**Add-AzWebAppTrafficRouting** cmdlet은 Azure 웹앱 슬롯에 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="f14ba-107">예제</span><span class="sxs-lookup"><span data-stu-id="f14ba-107">EXAMPLES</span></span>

### <span data-ttu-id="f14ba-108">예제 1 라우팅 규칙을 추가하여 프로덕션 트래픽의 15%를 Stg 슬롯으로 전송</span><span class="sxs-lookup"><span data-stu-id="f14ba-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="f14ba-109">이 명령은 프로덕션 트래픽의 15%를 Stg 슬롯으로 전송하는 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="f14ba-110">예제 2 라우팅 규칙을 추가하여 프로덕션 트래픽을 Stg 슬롯 범위의 50%에서 90% 증분 방식으로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="f14ba-111">이 명령은 프로덕션 트래픽을 50%에서 90% 증분 방식으로 Stg 슬롯 범위로 전송하는 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="f14ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f14ba-112">PARAMETERS</span></span>

### <span data-ttu-id="f14ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14ba-113">-DefaultProfile</span></span>
<span data-ttu-id="f14ba-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f14ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="f14ba-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f14ba-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f14ba-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="f14ba-117">-RoutingRule</span></span>
<span data-ttu-id="f14ba-118">웹앱 RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="f14ba-118">Web App RoutingRule.</span></span>
<span data-ttu-id="f14ba-119">예: -RoutingRule @{ActionHostName=$slot. DefaultHostName; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="f14ba-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="f14ba-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f14ba-120">-WebAppName</span></span>
<span data-ttu-id="f14ba-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="f14ba-121">WebApp Name</span></span>

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

### <span data-ttu-id="f14ba-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f14ba-122">-Confirm</span></span>
<span data-ttu-id="f14ba-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f14ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14ba-124">-WhatIf</span></span>
<span data-ttu-id="f14ba-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f14ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f14ba-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f14ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14ba-127">CommonParameters</span></span>
<span data-ttu-id="f14ba-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f14ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14ba-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f14ba-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14ba-130">입력</span><span class="sxs-lookup"><span data-stu-id="f14ba-130">INPUTS</span></span>

### <span data-ttu-id="f14ba-131">없음</span><span class="sxs-lookup"><span data-stu-id="f14ba-131">None</span></span>

## <span data-ttu-id="f14ba-132">출력</span><span class="sxs-lookup"><span data-stu-id="f14ba-132">OUTPUTS</span></span>

### <span data-ttu-id="f14ba-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="f14ba-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="f14ba-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f14ba-134">NOTES</span></span>

## <span data-ttu-id="f14ba-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f14ba-135">RELATED LINKS</span></span>
[<span data-ttu-id="f14ba-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f14ba-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f14ba-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f14ba-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f14ba-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f14ba-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
