---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 94706768c6e5f222abe5a74ea32549f356abe1c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326661"
---
# <span data-ttu-id="fb7ae-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fb7ae-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="fb7ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7ae-103">Linux 컴퓨터에서 사용자 지정 로그 수집을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="fb7ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb7ae-104">SYNTAX</span></span>

### <span data-ttu-id="fb7ae-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb7ae-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7ae-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb7ae-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7ae-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb7ae-107">DESCRIPTION</span></span>
<span data-ttu-id="fb7ae-108">**Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet은 작업 영역의 연결된 Linux 컴퓨터에서 사용자 지정 로그의 수집을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="fb7ae-109">예제</span><span class="sxs-lookup"><span data-stu-id="fb7ae-109">EXAMPLES</span></span>

## <span data-ttu-id="fb7ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb7ae-110">PARAMETERS</span></span>

### <span data-ttu-id="fb7ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7ae-111">-DefaultProfile</span></span>
<span data-ttu-id="fb7ae-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb7ae-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb7ae-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7ae-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb7ae-114">Linux 컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="fb7ae-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="fb7ae-115">-Workspace</span></span>
<span data-ttu-id="fb7ae-116">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb7ae-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb7ae-117">-WorkspaceName</span></span>
<span data-ttu-id="fb7ae-118">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb7ae-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb7ae-119">-Confirm</span></span>
<span data-ttu-id="fb7ae-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7ae-121">-WhatIf</span></span>
<span data-ttu-id="fb7ae-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb7ae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7ae-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7ae-124">CommonParameters</span></span>
<span data-ttu-id="fb7ae-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7ae-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fb7ae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7ae-127">입력</span><span class="sxs-lookup"><span data-stu-id="fb7ae-127">INPUTS</span></span>

### <span data-ttu-id="fb7ae-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb7ae-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fb7ae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fb7ae-129">System.String</span></span>

## <span data-ttu-id="fb7ae-130">출력</span><span class="sxs-lookup"><span data-stu-id="fb7ae-130">OUTPUTS</span></span>

### <span data-ttu-id="fb7ae-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fb7ae-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fb7ae-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb7ae-132">NOTES</span></span>
* <span data-ttu-id="fb7ae-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="fb7ae-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fb7ae-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb7ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb7ae-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fb7ae-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


