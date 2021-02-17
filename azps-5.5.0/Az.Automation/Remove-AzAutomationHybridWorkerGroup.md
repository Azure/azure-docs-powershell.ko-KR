---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205488"
---
# <span data-ttu-id="25aa8-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="25aa8-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="25aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="25aa8-103">Automation에서 Hybrid Worker 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="25aa8-104">구문</span><span class="sxs-lookup"><span data-stu-id="25aa8-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25aa8-105">설명</span><span class="sxs-lookup"><span data-stu-id="25aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="25aa8-106">이 Remove-AzAutomationHybridWorkerGroup cmdlet은 Automation에서 Hybrid Worker 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="25aa8-107">예제</span><span class="sxs-lookup"><span data-stu-id="25aa8-107">EXAMPLES</span></span>

### <span data-ttu-id="25aa8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="25aa8-108">Example 1</span></span>
<span data-ttu-id="25aa8-109">이 명령은 이름에 의해 Hybrid Worker를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="25aa8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25aa8-110">PARAMETERS</span></span>

### <span data-ttu-id="25aa8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25aa8-111">-AutomationAccountName</span></span>
<span data-ttu-id="25aa8-112">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-112">The automation account name.</span></span>

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

### <span data-ttu-id="25aa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25aa8-113">-DefaultProfile</span></span>
<span data-ttu-id="25aa8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25aa8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="25aa8-115">-Name</span></span>
<span data-ttu-id="25aa8-116">Hybrid Worker 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25aa8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25aa8-117">-ResourceGroupName</span></span>
<span data-ttu-id="25aa8-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-118">The resource group name.</span></span>

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

### <span data-ttu-id="25aa8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25aa8-119">-Confirm</span></span>
<span data-ttu-id="25aa8-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25aa8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25aa8-121">-WhatIf</span></span>
<span data-ttu-id="25aa8-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25aa8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25aa8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25aa8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25aa8-124">CommonParameters</span></span>
<span data-ttu-id="25aa8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25aa8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25aa8-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25aa8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25aa8-127">입력</span><span class="sxs-lookup"><span data-stu-id="25aa8-127">INPUTS</span></span>

### <span data-ttu-id="25aa8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="25aa8-128">System.String</span></span>

## <span data-ttu-id="25aa8-129">출력</span><span class="sxs-lookup"><span data-stu-id="25aa8-129">OUTPUTS</span></span>

### <span data-ttu-id="25aa8-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="25aa8-130">System.Void</span></span>

## <span data-ttu-id="25aa8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25aa8-131">NOTES</span></span>

## <span data-ttu-id="25aa8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25aa8-132">RELATED LINKS</span></span>
