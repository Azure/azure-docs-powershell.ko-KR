---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702324"
---
# <span data-ttu-id="c88e0-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c88e0-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="c88e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c88e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c88e0-103">자동화에서 hybrid worker 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c88e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c88e0-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c88e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c88e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c88e0-106">Remove-AzureRmAutomationHybridWorkerGroup cmdlet은 자동화에서 hybrid worker 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="c88e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c88e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c88e0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c88e0-108">Example 1</span></span>
<span data-ttu-id="c88e0-109">이 명령은 이름으로 hybrid worker를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="c88e0-110">변수</span><span class="sxs-lookup"><span data-stu-id="c88e0-110">PARAMETERS</span></span>

### <span data-ttu-id="c88e0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c88e0-111">-AutomationAccountName</span></span>
<span data-ttu-id="c88e0-112">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-112">The automation account name.</span></span>

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

### <span data-ttu-id="c88e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88e0-113">-DefaultProfile</span></span>
<span data-ttu-id="c88e0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88e0-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c88e0-115">-Name</span></span>
<span data-ttu-id="c88e0-116">Hybrid worker 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="c88e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="c88e0-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-118">The resource group name.</span></span>

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

### <span data-ttu-id="c88e0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c88e0-119">-Confirm</span></span>
<span data-ttu-id="c88e0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c88e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88e0-121">-WhatIf</span></span>
<span data-ttu-id="c88e0-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c88e0-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c88e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88e0-124">CommonParameters</span></span>
<span data-ttu-id="c88e0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c88e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88e0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c88e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88e0-127">입력</span><span class="sxs-lookup"><span data-stu-id="c88e0-127">INPUTS</span></span>

### <span data-ttu-id="c88e0-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c88e0-128">System.String</span></span>

## <span data-ttu-id="c88e0-129">출력</span><span class="sxs-lookup"><span data-stu-id="c88e0-129">OUTPUTS</span></span>

### <span data-ttu-id="c88e0-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c88e0-130">System.Void</span></span>

## <span data-ttu-id="c88e0-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c88e0-131">NOTES</span></span>

## <span data-ttu-id="c88e0-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c88e0-132">RELATED LINKS</span></span>
