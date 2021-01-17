---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384987"
---
# <span data-ttu-id="1eb28-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="1eb28-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="1eb28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb28-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb28-103">컴퓨터에서 IIS 로그 수집을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="1eb28-104">구문</span><span class="sxs-lookup"><span data-stu-id="1eb28-104">SYNTAX</span></span>

### <span data-ttu-id="1eb28-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1eb28-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eb28-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1eb28-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb28-107">설명</span><span class="sxs-lookup"><span data-stu-id="1eb28-107">DESCRIPTION</span></span>
<span data-ttu-id="1eb28-108">**Disable-AzOperationalInsightsIISLogCollection** cmdlet은 작업 영역의 연결된 컴퓨터에서 IIS(인터넷 정보 서비스) 로그 수집을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="1eb28-109">예제</span><span class="sxs-lookup"><span data-stu-id="1eb28-109">EXAMPLES</span></span>

## <span data-ttu-id="1eb28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1eb28-110">PARAMETERS</span></span>

### <span data-ttu-id="1eb28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb28-111">-DefaultProfile</span></span>
<span data-ttu-id="1eb28-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1eb28-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1eb28-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb28-113">-ResourceGroupName</span></span>
<span data-ttu-id="1eb28-114">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="1eb28-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="1eb28-115">-Workspace</span></span>
<span data-ttu-id="1eb28-116">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1eb28-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1eb28-117">-WorkspaceName</span></span>
<span data-ttu-id="1eb28-118">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1eb28-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1eb28-119">-Confirm</span></span>
<span data-ttu-id="1eb28-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb28-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb28-121">-WhatIf</span></span>
<span data-ttu-id="1eb28-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1eb28-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eb28-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb28-124">CommonParameters</span></span>
<span data-ttu-id="1eb28-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1eb28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb28-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1eb28-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb28-127">입력</span><span class="sxs-lookup"><span data-stu-id="1eb28-127">INPUTS</span></span>

### <span data-ttu-id="1eb28-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1eb28-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1eb28-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1eb28-129">System.String</span></span>

## <span data-ttu-id="1eb28-130">출력</span><span class="sxs-lookup"><span data-stu-id="1eb28-130">OUTPUTS</span></span>

### <span data-ttu-id="1eb28-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1eb28-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1eb28-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1eb28-132">NOTES</span></span>
* <span data-ttu-id="1eb28-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="1eb28-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="1eb28-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1eb28-134">RELATED LINKS</span></span>

[<span data-ttu-id="1eb28-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="1eb28-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


