---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490895"
---
# <span data-ttu-id="a64ee-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a64ee-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="a64ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a64ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a64ee-103">데이터 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-103">Deletes a data source.</span></span>

## <span data-ttu-id="a64ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="a64ee-104">SYNTAX</span></span>

### <span data-ttu-id="a64ee-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a64ee-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a64ee-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a64ee-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a64ee-107">설명</span><span class="sxs-lookup"><span data-stu-id="a64ee-107">DESCRIPTION</span></span>
<span data-ttu-id="a64ee-108">**Remove-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="a64ee-109">예제</span><span class="sxs-lookup"><span data-stu-id="a64ee-109">EXAMPLES</span></span>

## <span data-ttu-id="a64ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a64ee-110">PARAMETERS</span></span>

### <span data-ttu-id="a64ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a64ee-111">-DefaultProfile</span></span>
<span data-ttu-id="a64ee-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a64ee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a64ee-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a64ee-113">-Force</span></span>
<span data-ttu-id="a64ee-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a64ee-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a64ee-115">-Name</span></span>
<span data-ttu-id="a64ee-116">삭제할 데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="a64ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a64ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="a64ee-118">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="a64ee-119">-Workspace</span><span class="sxs-lookup"><span data-stu-id="a64ee-119">-Workspace</span></span>
<span data-ttu-id="a64ee-120">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a64ee-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a64ee-121">-WorkspaceName</span></span>
<span data-ttu-id="a64ee-122">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a64ee-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a64ee-123">-Confirm</span></span>
<span data-ttu-id="a64ee-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a64ee-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a64ee-125">-WhatIf</span></span>
<span data-ttu-id="a64ee-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a64ee-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a64ee-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a64ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a64ee-128">CommonParameters</span></span>
<span data-ttu-id="a64ee-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a64ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a64ee-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a64ee-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a64ee-131">입력</span><span class="sxs-lookup"><span data-stu-id="a64ee-131">INPUTS</span></span>

### <span data-ttu-id="a64ee-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a64ee-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a64ee-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a64ee-133">System.String</span></span>

## <span data-ttu-id="a64ee-134">출력</span><span class="sxs-lookup"><span data-stu-id="a64ee-134">OUTPUTS</span></span>

### <span data-ttu-id="a64ee-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="a64ee-135">System.Void</span></span>

## <span data-ttu-id="a64ee-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a64ee-136">NOTES</span></span>
* <span data-ttu-id="a64ee-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="a64ee-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a64ee-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a64ee-138">RELATED LINKS</span></span>

[<span data-ttu-id="a64ee-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a64ee-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="a64ee-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="a64ee-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


