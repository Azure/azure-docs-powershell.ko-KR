---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214041"
---
# <span data-ttu-id="5986f-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5986f-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="5986f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5986f-102">SYNOPSIS</span></span>
<span data-ttu-id="5986f-103">컴퓨터에서 IIS 로그 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="5986f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5986f-104">SYNTAX</span></span>

### <span data-ttu-id="5986f-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5986f-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5986f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5986f-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5986f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5986f-107">DESCRIPTION</span></span>
<span data-ttu-id="5986f-108">**AzOperationalInsightsIISLogCollection** cmdlet은 작업 영역에 연결 된 컴퓨터의 IIS (인터넷 정보 서비스) 로그 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="5986f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5986f-109">EXAMPLES</span></span>

## <span data-ttu-id="5986f-110">변수</span><span class="sxs-lookup"><span data-stu-id="5986f-110">PARAMETERS</span></span>

### <span data-ttu-id="5986f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5986f-111">-DefaultProfile</span></span>
<span data-ttu-id="5986f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5986f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5986f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5986f-113">-ResourceGroupName</span></span>
<span data-ttu-id="5986f-114">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5986f-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="5986f-115">-Workspace</span></span>
<span data-ttu-id="5986f-116">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5986f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5986f-117">-WorkspaceName</span></span>
<span data-ttu-id="5986f-118">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5986f-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5986f-119">-Confirm</span></span>
<span data-ttu-id="5986f-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5986f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5986f-121">-WhatIf</span></span>
<span data-ttu-id="5986f-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5986f-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5986f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5986f-124">CommonParameters</span></span>
<span data-ttu-id="5986f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5986f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5986f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5986f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5986f-127">입력</span><span class="sxs-lookup"><span data-stu-id="5986f-127">INPUTS</span></span>

### <span data-ttu-id="5986f-128">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="5986f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5986f-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5986f-129">System.String</span></span>

## <span data-ttu-id="5986f-130">출력</span><span class="sxs-lookup"><span data-stu-id="5986f-130">OUTPUTS</span></span>

### <span data-ttu-id="5986f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5986f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5986f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5986f-132">NOTES</span></span>
* <span data-ttu-id="5986f-133">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="5986f-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5986f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5986f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5986f-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5986f-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


