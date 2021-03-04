---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 16aabb8fe12569c6c230248fcea8038e1a162f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997556"
---
# <span data-ttu-id="fb583-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fb583-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="fb583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb583-102">SYNOPSIS</span></span>
<span data-ttu-id="fb583-103">Linux 컴퓨터에서 사용자 지정 로그 컬렉션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="fb583-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb583-104">SYNTAX</span></span>

### <span data-ttu-id="fb583-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb583-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb583-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb583-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb583-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb583-107">DESCRIPTION</span></span>
<span data-ttu-id="fb583-108">**Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet은 작업 영역의 연결된 Linux 컴퓨터에서 사용자 지정 로그의 컬렉션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="fb583-109">예제</span><span class="sxs-lookup"><span data-stu-id="fb583-109">EXAMPLES</span></span>

## <span data-ttu-id="fb583-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fb583-110">PARAMETERS</span></span>

### <span data-ttu-id="fb583-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb583-111">-DefaultProfile</span></span>
<span data-ttu-id="fb583-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb583-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb583-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb583-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb583-114">Linux 컴퓨터가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="fb583-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="fb583-115">-Workspace</span></span>
<span data-ttu-id="fb583-116">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb583-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb583-117">-WorkspaceName</span></span>
<span data-ttu-id="fb583-118">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb583-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fb583-119">-Confirm</span></span>
<span data-ttu-id="fb583-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb583-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb583-121">-WhatIf</span></span>
<span data-ttu-id="fb583-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb583-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb583-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb583-124">CommonParameters</span></span>
<span data-ttu-id="fb583-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb583-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb583-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fb583-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb583-127">입력</span><span class="sxs-lookup"><span data-stu-id="fb583-127">INPUTS</span></span>

### <span data-ttu-id="fb583-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb583-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fb583-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fb583-129">System.String</span></span>

## <span data-ttu-id="fb583-130">출력</span><span class="sxs-lookup"><span data-stu-id="fb583-130">OUTPUTS</span></span>

### <span data-ttu-id="fb583-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fb583-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fb583-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb583-132">NOTES</span></span>
* <span data-ttu-id="fb583-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="fb583-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fb583-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb583-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb583-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fb583-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


