---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 7593ad23952b9920fdd7e7fa9d75e22e9fe65059
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997598"
---
# <span data-ttu-id="d7bd8-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d7bd8-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="d7bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bd8-103">Linux 컴퓨터에서 syslog 데이터의 컬렉션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="d7bd8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7bd8-104">SYNTAX</span></span>

### <span data-ttu-id="d7bd8-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7bd8-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7bd8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d7bd8-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bd8-107">설명</span><span class="sxs-lookup"><span data-stu-id="d7bd8-107">DESCRIPTION</span></span>
<span data-ttu-id="d7bd8-108">**Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet은 작업 영역의 연결된 Linux 컴퓨터에서 syslog 데이터의 수집을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d7bd8-109">예제</span><span class="sxs-lookup"><span data-stu-id="d7bd8-109">EXAMPLES</span></span>

## <span data-ttu-id="d7bd8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d7bd8-110">PARAMETERS</span></span>

### <span data-ttu-id="d7bd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bd8-111">-DefaultProfile</span></span>
<span data-ttu-id="d7bd8-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d7bd8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7bd8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bd8-113">-ResourceGroupName</span></span>
<span data-ttu-id="d7bd8-114">Linux 컴퓨터가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d7bd8-115">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="d7bd8-115">-Workspace</span></span>
<span data-ttu-id="d7bd8-116">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d7bd8-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d7bd8-117">-WorkspaceName</span></span>
<span data-ttu-id="d7bd8-118">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d7bd8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d7bd8-119">-Confirm</span></span>
<span data-ttu-id="d7bd8-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bd8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bd8-121">-WhatIf</span></span>
<span data-ttu-id="d7bd8-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7bd8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bd8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bd8-124">CommonParameters</span></span>
<span data-ttu-id="d7bd8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bd8-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7bd8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bd8-127">입력</span><span class="sxs-lookup"><span data-stu-id="d7bd8-127">INPUTS</span></span>

### <span data-ttu-id="d7bd8-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7bd8-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d7bd8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d7bd8-129">System.String</span></span>

## <span data-ttu-id="d7bd8-130">출력</span><span class="sxs-lookup"><span data-stu-id="d7bd8-130">OUTPUTS</span></span>

### <span data-ttu-id="d7bd8-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d7bd8-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d7bd8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7bd8-132">NOTES</span></span>
* <span data-ttu-id="d7bd8-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="d7bd8-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d7bd8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7bd8-134">RELATED LINKS</span></span>

[<span data-ttu-id="d7bd8-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="d7bd8-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="d7bd8-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="d7bd8-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


