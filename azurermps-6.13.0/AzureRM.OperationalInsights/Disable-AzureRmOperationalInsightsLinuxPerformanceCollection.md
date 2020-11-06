---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: e6a77e8e89f710e1f8f827a27b1e1709ca8e3f1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527808"
---
# <span data-ttu-id="24c7e-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="24c7e-101">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="24c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="24c7e-103">Linux 컴퓨터에서 성능 카운터 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-103">Stops collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24c7e-104">SYNTAX</span></span>

### <span data-ttu-id="24c7e-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="24c7e-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c7e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="24c7e-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c7e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="24c7e-108">**AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet은 작업 영역에서 연결 된 Linux 컴퓨터의 성능 카운터 수집을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-108">The **Disable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="24c7e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="24c7e-109">EXAMPLES</span></span>

## <span data-ttu-id="24c7e-110">변수</span><span class="sxs-lookup"><span data-stu-id="24c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="24c7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c7e-111">-DefaultProfile</span></span>
<span data-ttu-id="24c7e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24c7e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c7e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c7e-113">-ResourceGroupName</span></span>
<span data-ttu-id="24c7e-114">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="24c7e-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="24c7e-115">-Workspace</span></span>
<span data-ttu-id="24c7e-116">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="24c7e-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24c7e-117">-WorkspaceName</span></span>
<span data-ttu-id="24c7e-118">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="24c7e-119">-확인</span><span class="sxs-lookup"><span data-stu-id="24c7e-119">-Confirm</span></span>
<span data-ttu-id="24c7e-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c7e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c7e-121">-WhatIf</span></span>
<span data-ttu-id="24c7e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c7e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c7e-124">CommonParameters</span></span>
<span data-ttu-id="24c7e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c7e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c7e-127">입력</span><span class="sxs-lookup"><span data-stu-id="24c7e-127">INPUTS</span></span>

### <span data-ttu-id="24c7e-128">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="24c7e-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="24c7e-129">매개 변수: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24c7e-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="24c7e-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24c7e-130">System.String</span></span>

## <span data-ttu-id="24c7e-131">출력</span><span class="sxs-lookup"><span data-stu-id="24c7e-131">OUTPUTS</span></span>

### <span data-ttu-id="24c7e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="24c7e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="24c7e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="24c7e-133">NOTES</span></span>
* <span data-ttu-id="24c7e-134">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="24c7e-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="24c7e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24c7e-135">RELATED LINKS</span></span>

[<span data-ttu-id="24c7e-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="24c7e-136">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="24c7e-137">새로운 AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="24c7e-137">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


