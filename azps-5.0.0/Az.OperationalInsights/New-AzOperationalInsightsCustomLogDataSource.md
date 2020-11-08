---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217231"
---
# <span data-ttu-id="4ba43-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="4ba43-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="4ba43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba43-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba43-103">사용자 지정 로그 수집 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="4ba43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ba43-104">SYNTAX</span></span>

### <span data-ttu-id="4ba43-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ba43-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ba43-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4ba43-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ba43-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ba43-107">DESCRIPTION</span></span>
<span data-ttu-id="4ba43-108">**새 AzOperationalInsightsCustomLogDataSource** cmdlet은 사용자 지정 로그 수집 정책을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="4ba43-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4ba43-109">EXAMPLES</span></span>

## <span data-ttu-id="4ba43-110">변수</span><span class="sxs-lookup"><span data-stu-id="4ba43-110">PARAMETERS</span></span>

### <span data-ttu-id="4ba43-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="4ba43-111">-CustomLogRawJson</span></span>
<span data-ttu-id="4ba43-112">사용자 지정 컬렉션 정책을 JSON (원시 JavaScript 개체 표기) 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="4ba43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba43-113">-DefaultProfile</span></span>
<span data-ttu-id="4ba43-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ba43-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ba43-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ba43-115">-Force</span></span>
<span data-ttu-id="4ba43-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ba43-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4ba43-117">-Name</span></span>
<span data-ttu-id="4ba43-118">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="4ba43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba43-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ba43-120">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="4ba43-121">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="4ba43-121">-Workspace</span></span>
<span data-ttu-id="4ba43-122">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4ba43-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ba43-123">-WorkspaceName</span></span>
<span data-ttu-id="4ba43-124">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4ba43-125">-확인</span><span class="sxs-lookup"><span data-stu-id="4ba43-125">-Confirm</span></span>
<span data-ttu-id="4ba43-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba43-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba43-127">-WhatIf</span></span>
<span data-ttu-id="4ba43-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba43-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba43-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba43-130">CommonParameters</span></span>
<span data-ttu-id="4ba43-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ba43-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba43-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba43-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba43-133">입력</span><span class="sxs-lookup"><span data-stu-id="4ba43-133">INPUTS</span></span>

### <span data-ttu-id="4ba43-134">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="4ba43-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="4ba43-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ba43-135">System.String</span></span>

## <span data-ttu-id="4ba43-136">출력</span><span class="sxs-lookup"><span data-stu-id="4ba43-136">OUTPUTS</span></span>

### <span data-ttu-id="4ba43-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="4ba43-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="4ba43-138">상속자</span><span class="sxs-lookup"><span data-stu-id="4ba43-138">NOTES</span></span>

## <span data-ttu-id="4ba43-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ba43-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ba43-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="4ba43-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="4ba43-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="4ba43-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


