---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215925"
---
# <span data-ttu-id="cdd09-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="cdd09-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="cdd09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd09-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd09-103">삭제 된 작업 영역을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="cdd09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cdd09-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cdd09-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd09-106">삭제 된 작업 영역을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="cdd09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cdd09-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd09-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cdd09-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="cdd09-109">삭제 된 작업 영역 복원</span><span class="sxs-lookup"><span data-stu-id="cdd09-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="cdd09-110">변수</span><span class="sxs-lookup"><span data-stu-id="cdd09-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd09-111">-DefaultProfile</span></span>
<span data-ttu-id="cdd09-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd09-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cdd09-113">-Force</span></span>
<span data-ttu-id="cdd09-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cdd09-115">-위치</span><span class="sxs-lookup"><span data-stu-id="cdd09-115">-Location</span></span>
<span data-ttu-id="cdd09-116">작업 영역을 만들 지리적 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="cdd09-117">-이름</span><span class="sxs-lookup"><span data-stu-id="cdd09-117">-Name</span></span>
<span data-ttu-id="cdd09-118">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd09-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd09-119">-ResourceGroupName</span></span>
<span data-ttu-id="cdd09-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-120">The resource group name.</span></span>

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

### <span data-ttu-id="cdd09-121">-확인</span><span class="sxs-lookup"><span data-stu-id="cdd09-121">-Confirm</span></span>
<span data-ttu-id="cdd09-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd09-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd09-123">-WhatIf</span></span>
<span data-ttu-id="cdd09-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd09-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdd09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd09-126">CommonParameters</span></span>
<span data-ttu-id="cdd09-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd09-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cdd09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd09-129">입력</span><span class="sxs-lookup"><span data-stu-id="cdd09-129">INPUTS</span></span>

### <span data-ttu-id="cdd09-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cdd09-130">System.String</span></span>

## <span data-ttu-id="cdd09-131">출력</span><span class="sxs-lookup"><span data-stu-id="cdd09-131">OUTPUTS</span></span>

### <span data-ttu-id="cdd09-132">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="cdd09-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="cdd09-133">상속자</span><span class="sxs-lookup"><span data-stu-id="cdd09-133">NOTES</span></span>

## <span data-ttu-id="cdd09-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdd09-134">RELATED LINKS</span></span>
