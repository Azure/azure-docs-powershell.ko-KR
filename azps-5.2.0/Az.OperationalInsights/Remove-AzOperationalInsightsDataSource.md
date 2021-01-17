---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359171"
---
# <span data-ttu-id="ae15a-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ae15a-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="ae15a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae15a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae15a-103">데이터 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-103">Deletes a data source.</span></span>

## <span data-ttu-id="ae15a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae15a-104">SYNTAX</span></span>

### <span data-ttu-id="ae15a-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ae15a-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae15a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ae15a-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae15a-107">설명</span><span class="sxs-lookup"><span data-stu-id="ae15a-107">DESCRIPTION</span></span>
<span data-ttu-id="ae15a-108">**Remove-AzOperationalInsightsDataSource** cmdlet은 데이터 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="ae15a-109">예제</span><span class="sxs-lookup"><span data-stu-id="ae15a-109">EXAMPLES</span></span>

## <span data-ttu-id="ae15a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae15a-110">PARAMETERS</span></span>

### <span data-ttu-id="ae15a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae15a-111">-DefaultProfile</span></span>
<span data-ttu-id="ae15a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae15a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae15a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ae15a-113">-Force</span></span>
<span data-ttu-id="ae15a-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae15a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ae15a-115">-Name</span></span>
<span data-ttu-id="ae15a-116">삭제할 데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="ae15a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae15a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae15a-118">컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ae15a-119">-Workspace</span><span class="sxs-lookup"><span data-stu-id="ae15a-119">-Workspace</span></span>
<span data-ttu-id="ae15a-120">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ae15a-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ae15a-121">-WorkspaceName</span></span>
<span data-ttu-id="ae15a-122">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ae15a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae15a-123">-Confirm</span></span>
<span data-ttu-id="ae15a-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae15a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae15a-125">-WhatIf</span></span>
<span data-ttu-id="ae15a-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ae15a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae15a-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae15a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae15a-128">CommonParameters</span></span>
<span data-ttu-id="ae15a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae15a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae15a-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ae15a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae15a-131">입력</span><span class="sxs-lookup"><span data-stu-id="ae15a-131">INPUTS</span></span>

### <span data-ttu-id="ae15a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ae15a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ae15a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ae15a-133">System.String</span></span>

## <span data-ttu-id="ae15a-134">출력</span><span class="sxs-lookup"><span data-stu-id="ae15a-134">OUTPUTS</span></span>

### <span data-ttu-id="ae15a-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="ae15a-135">System.Void</span></span>

## <span data-ttu-id="ae15a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae15a-136">NOTES</span></span>
* <span data-ttu-id="ae15a-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="ae15a-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ae15a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae15a-138">RELATED LINKS</span></span>

[<span data-ttu-id="ae15a-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ae15a-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="ae15a-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ae15a-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


