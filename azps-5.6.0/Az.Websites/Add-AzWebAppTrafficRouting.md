---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983931"
---
# <span data-ttu-id="a5b5e-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a5b5e-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="a5b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b5e-103">슬롯에 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="a5b5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5b5e-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b5e-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5b5e-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b5e-106">**Add-AzWebAppTrafficRouting** cmdlet은 Azure Web App Slot에 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="a5b5e-107">예제</span><span class="sxs-lookup"><span data-stu-id="a5b5e-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b5e-108">예제 1 프로덕션 트래픽의 15%를 Stg 슬롯으로 전송하는 라우팅 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="a5b5e-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="a5b5e-109">이 명령은 프로덕션 트래픽의 15%를 Stg 슬롯에 전송하는 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="a5b5e-110">예제 2 라우팅 규칙을 추가하여 프로덕션 트래픽을 Stg 슬롯 범위의 50%에서 90%까지 증분 방식으로 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="a5b5e-111">이 명령은 프로덕션 트래픽을 Stg 슬롯 범위에 증분 방식으로 50%에서 90%로 전송하는 라우팅 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="a5b5e-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5b5e-112">PARAMETERS</span></span>

### <span data-ttu-id="a5b5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b5e-113">-DefaultProfile</span></span>
<span data-ttu-id="a5b5e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b5e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b5e-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5b5e-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a5b5e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a5b5e-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="a5b5e-117">-RoutingRule</span></span>
<span data-ttu-id="a5b5e-118">웹앱 라우팅Rule.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-118">Web App RoutingRule.</span></span>
<span data-ttu-id="a5b5e-119">예: -RoutingRule @{ActionHostName=$slot. DefaultHostName ; ReroutePercentage=$ReroutePercentage; Name=$slotName}</span><span class="sxs-lookup"><span data-stu-id="a5b5e-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="a5b5e-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a5b5e-120">-WebAppName</span></span>
<span data-ttu-id="a5b5e-121">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="a5b5e-121">WebApp Name</span></span>

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

### <span data-ttu-id="a5b5e-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a5b5e-122">-Confirm</span></span>
<span data-ttu-id="a5b5e-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b5e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b5e-124">-WhatIf</span></span>
<span data-ttu-id="a5b5e-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b5e-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b5e-127">CommonParameters</span></span>
<span data-ttu-id="a5b5e-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5b5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b5e-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5b5e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b5e-130">입력</span><span class="sxs-lookup"><span data-stu-id="a5b5e-130">INPUTS</span></span>

### <span data-ttu-id="a5b5e-131">없음</span><span class="sxs-lookup"><span data-stu-id="a5b5e-131">None</span></span>

## <span data-ttu-id="a5b5e-132">출력</span><span class="sxs-lookup"><span data-stu-id="a5b5e-132">OUTPUTS</span></span>

### <span data-ttu-id="a5b5e-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="a5b5e-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="a5b5e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5b5e-134">NOTES</span></span>

## <span data-ttu-id="a5b5e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5b5e-135">RELATED LINKS</span></span>
[<span data-ttu-id="a5b5e-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a5b5e-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="a5b5e-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a5b5e-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="a5b5e-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a5b5e-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
