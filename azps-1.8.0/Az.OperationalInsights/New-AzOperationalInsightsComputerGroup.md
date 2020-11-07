---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: ce3a935dc97e63615e3bb1253fd5eedcb5c702da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699848"
---
# <span data-ttu-id="6f9c9-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="6f9c9-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="6f9c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9c9-103">컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-103">Creates a computer group.</span></span>

## <span data-ttu-id="6f9c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f9c9-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f9c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="6f9c9-106">**AzOperationalInsightsComputerGroup** cmdlet은 리소스 그룹 및 위치에 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="6f9c9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f9c9-107">EXAMPLES</span></span>

## <span data-ttu-id="6f9c9-108">변수</span><span class="sxs-lookup"><span data-stu-id="6f9c9-108">PARAMETERS</span></span>

### <span data-ttu-id="6f9c9-109">-범주</span><span class="sxs-lookup"><span data-stu-id="6f9c9-109">-Category</span></span>
<span data-ttu-id="6f9c9-110">컴퓨터 그룹의 범주를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="6f9c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9c9-111">-DefaultProfile</span></span>
<span data-ttu-id="6f9c9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6f9c9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f9c9-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6f9c9-113">-DisplayName</span></span>
<span data-ttu-id="6f9c9-114">컴퓨터 그룹의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="6f9c9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6f9c9-115">-Force</span></span>
<span data-ttu-id="6f9c9-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f9c9-117">-쿼리</span><span class="sxs-lookup"><span data-stu-id="6f9c9-117">-Query</span></span>
<span data-ttu-id="6f9c9-118">컴퓨터 그룹의 쿼리를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f9c9-120">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6f9c9-121">Cmdlet이이 리소스 그룹에 컴퓨터 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-121">The cmdlet creates computer group in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9c9-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="6f9c9-122">-SavedSearchId</span></span>
<span data-ttu-id="6f9c9-123">컴퓨터 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-123">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9c9-124">-버전</span><span class="sxs-lookup"><span data-stu-id="6f9c9-124">-Version</span></span>
<span data-ttu-id="6f9c9-125">버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9c9-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f9c9-126">-WorkspaceName</span></span>
<span data-ttu-id="6f9c9-127">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9c9-128">-확인</span><span class="sxs-lookup"><span data-stu-id="6f9c9-128">-Confirm</span></span>
<span data-ttu-id="6f9c9-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f9c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f9c9-130">-WhatIf</span></span>
<span data-ttu-id="6f9c9-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f9c9-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f9c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9c9-133">CommonParameters</span></span>
<span data-ttu-id="6f9c9-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9c9-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9c9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9c9-136">입력</span><span class="sxs-lookup"><span data-stu-id="6f9c9-136">INPUTS</span></span>

### <span data-ttu-id="6f9c9-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f9c9-137">System.String</span></span>

### <span data-ttu-id="6f9c9-138">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="6f9c9-138">System.Int64</span></span>

## <span data-ttu-id="6f9c9-139">출력</span><span class="sxs-lookup"><span data-stu-id="6f9c9-139">OUTPUTS</span></span>

### <span data-ttu-id="6f9c9-140">System .Net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="6f9c9-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="6f9c9-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6f9c9-141">NOTES</span></span>

## <span data-ttu-id="6f9c9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f9c9-142">RELATED LINKS</span></span>