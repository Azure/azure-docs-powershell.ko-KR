---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: b9f23105b6fa84781ef1b0f0ba4be0e52e06ee08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697761"
---
# <span data-ttu-id="82edf-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="82edf-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="82edf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82edf-102">SYNOPSIS</span></span>
<span data-ttu-id="82edf-103">자동화에서 hybrid worker 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="82edf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82edf-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82edf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82edf-105">DESCRIPTION</span></span>
<span data-ttu-id="82edf-106">Remove-AzAutomationHybridWorkerGroup cmdlet은 자동화에서 hybrid worker 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="82edf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="82edf-107">EXAMPLES</span></span>

### <span data-ttu-id="82edf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="82edf-108">Example 1</span></span>
<span data-ttu-id="82edf-109">이 명령은 이름으로 hybrid worker를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="82edf-110">변수</span><span class="sxs-lookup"><span data-stu-id="82edf-110">PARAMETERS</span></span>

### <span data-ttu-id="82edf-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82edf-111">-AutomationAccountName</span></span>
<span data-ttu-id="82edf-112">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-112">The automation account name.</span></span>

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

### <span data-ttu-id="82edf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82edf-113">-DefaultProfile</span></span>
<span data-ttu-id="82edf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82edf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="82edf-115">-Name</span></span>
<span data-ttu-id="82edf-116">Hybrid worker 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="82edf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82edf-117">-ResourceGroupName</span></span>
<span data-ttu-id="82edf-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-118">The resource group name.</span></span>

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

### <span data-ttu-id="82edf-119">-확인</span><span class="sxs-lookup"><span data-stu-id="82edf-119">-Confirm</span></span>
<span data-ttu-id="82edf-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82edf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82edf-121">-WhatIf</span></span>
<span data-ttu-id="82edf-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82edf-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82edf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82edf-124">CommonParameters</span></span>
<span data-ttu-id="82edf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82edf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82edf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82edf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82edf-127">입력</span><span class="sxs-lookup"><span data-stu-id="82edf-127">INPUTS</span></span>

### <span data-ttu-id="82edf-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82edf-128">System.String</span></span>

## <span data-ttu-id="82edf-129">출력</span><span class="sxs-lookup"><span data-stu-id="82edf-129">OUTPUTS</span></span>

### <span data-ttu-id="82edf-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="82edf-130">System.Void</span></span>

## <span data-ttu-id="82edf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="82edf-131">NOTES</span></span>

## <span data-ttu-id="82edf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82edf-132">RELATED LINKS</span></span>
