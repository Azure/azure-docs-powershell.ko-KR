---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 4bb969e0d18aca0f05663003c0fe78edf5b0e99d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528482"
---
# <span data-ttu-id="c5c50-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="c5c50-101">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="c5c50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5c50-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c50-103">Linux 컴퓨터에서 성능 카운터 모음을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-103">Starts collection of performance counters from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5c50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5c50-104">SYNTAX</span></span>

### <span data-ttu-id="c5c50-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5c50-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5c50-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c5c50-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5c50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c5c50-107">DESCRIPTION</span></span>
<span data-ttu-id="c5c50-108">**AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet은 작업 영역에서 연결 된 Linux 컴퓨터의 성능 카운터 모음을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-108">The **Enable-AzureRmOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="c5c50-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5c50-109">EXAMPLES</span></span>

## <span data-ttu-id="c5c50-110">변수</span><span class="sxs-lookup"><span data-stu-id="c5c50-110">PARAMETERS</span></span>

### <span data-ttu-id="c5c50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c50-111">-DefaultProfile</span></span>
<span data-ttu-id="c5c50-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c5c50-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5c50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c50-113">-ResourceGroupName</span></span>
<span data-ttu-id="c5c50-114">Linux 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="c5c50-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="c5c50-115">-Workspace</span></span>
<span data-ttu-id="c5c50-116">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c5c50-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5c50-117">-WorkspaceName</span></span>
<span data-ttu-id="c5c50-118">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c5c50-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c5c50-119">-Confirm</span></span>
<span data-ttu-id="c5c50-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c50-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c50-121">-WhatIf</span></span>
<span data-ttu-id="c5c50-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5c50-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5c50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c50-124">CommonParameters</span></span>
<span data-ttu-id="c5c50-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5c50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c50-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c50-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c50-127">입력</span><span class="sxs-lookup"><span data-stu-id="c5c50-127">INPUTS</span></span>

### <span data-ttu-id="c5c50-128">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="c5c50-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="c5c50-129">매개 변수: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5c50-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="c5c50-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5c50-130">System.String</span></span>

## <span data-ttu-id="c5c50-131">출력</span><span class="sxs-lookup"><span data-stu-id="c5c50-131">OUTPUTS</span></span>

### <span data-ttu-id="c5c50-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c5c50-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c5c50-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c5c50-133">NOTES</span></span>
* <span data-ttu-id="c5c50-134">키워드: azure, azurerm, arm, resource, 관리, 관리자, 운영, insights</span><span class="sxs-lookup"><span data-stu-id="c5c50-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c5c50-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5c50-135">RELATED LINKS</span></span>

[<span data-ttu-id="c5c50-136">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="c5c50-136">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

