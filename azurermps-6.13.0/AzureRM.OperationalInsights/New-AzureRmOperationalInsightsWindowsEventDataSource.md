---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5f3200459cbcca9806a1a7185798889b3457760d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531357"
---
# <span data-ttu-id="ff6fd-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ff6fd-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="ff6fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6fd-103">Windows 운영 체제를 실행 하는 컴퓨터에서 이벤트 로그를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff6fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff6fd-104">SYNTAX</span></span>

### <span data-ttu-id="ff6fd-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff6fd-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6fd-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff6fd-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff6fd-107">DESCRIPTION</span></span>
<span data-ttu-id="ff6fd-108">**AzureRmOperationalInsightsWindowsEventDataSource** Cmdlet은 Azure Operational Insights에서 windows 운영 체제를 실행 하는 연결 된 컴퓨터에서 windows 이벤트 로그를 수집 하는 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="ff6fd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ff6fd-109">EXAMPLES</span></span>

## <span data-ttu-id="ff6fd-110">변수</span><span class="sxs-lookup"><span data-stu-id="ff6fd-110">PARAMETERS</span></span>

### <span data-ttu-id="ff6fd-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="ff6fd-111">-CollectErrors</span></span>
<span data-ttu-id="ff6fd-112">Operational Insights에서 오류 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ff6fd-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="ff6fd-113">-CollectInformation</span></span>
<span data-ttu-id="ff6fd-114">Operational Insights가 정보 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="ff6fd-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="ff6fd-115">-CollectWarnings</span></span>
<span data-ttu-id="ff6fd-116">Operational Insights가 경고 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="ff6fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6fd-117">-DefaultProfile</span></span>
<span data-ttu-id="ff6fd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff6fd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff6fd-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="ff6fd-119">-EventLogName</span></span>
<span data-ttu-id="ff6fd-120">이벤트 로그의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="ff6fd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ff6fd-121">-Force</span></span>
<span data-ttu-id="ff6fd-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff6fd-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ff6fd-123">-Name</span></span>
<span data-ttu-id="ff6fd-124">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="ff6fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff6fd-126">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ff6fd-127">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="ff6fd-127">-Workspace</span></span>
<span data-ttu-id="ff6fd-128">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff6fd-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff6fd-129">-WorkspaceName</span></span>
<span data-ttu-id="ff6fd-130">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff6fd-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ff6fd-131">-Confirm</span></span>
<span data-ttu-id="ff6fd-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6fd-133">-WhatIf</span></span>
<span data-ttu-id="ff6fd-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff6fd-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6fd-136">CommonParameters</span></span>
<span data-ttu-id="ff6fd-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff6fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6fd-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6fd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6fd-139">입력</span><span class="sxs-lookup"><span data-stu-id="ff6fd-139">INPUTS</span></span>

### <span data-ttu-id="ff6fd-140">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="ff6fd-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ff6fd-141">매개 변수: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff6fd-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ff6fd-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff6fd-142">System.String</span></span>

## <span data-ttu-id="ff6fd-143">출력</span><span class="sxs-lookup"><span data-stu-id="ff6fd-143">OUTPUTS</span></span>

### <span data-ttu-id="ff6fd-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ff6fd-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ff6fd-145">상속자</span><span class="sxs-lookup"><span data-stu-id="ff6fd-145">NOTES</span></span>

## <span data-ttu-id="ff6fd-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff6fd-146">RELATED LINKS</span></span>
