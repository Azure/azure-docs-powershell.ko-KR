---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 7061d70ca1f4bc38c9ac8cc12ad75f01a3fed8b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386205"
---
# <span data-ttu-id="04c85-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="04c85-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="04c85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04c85-102">SYNOPSIS</span></span>
<span data-ttu-id="04c85-103">논리 앱의 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="04c85-104">구문</span><span class="sxs-lookup"><span data-stu-id="04c85-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c85-105">설명</span><span class="sxs-lookup"><span data-stu-id="04c85-105">DESCRIPTION</span></span>
<span data-ttu-id="04c85-106">**Get-AzLogicAppTrigger** cmdlet은 논리 앱에서 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="04c85-107">이 cmdlet은 **WorkflowTrigger 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="04c85-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="04c85-108">워크플로, 리소스 그룹 및 트리거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="04c85-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="04c85-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="04c85-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="04c85-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="04c85-113">예제</span><span class="sxs-lookup"><span data-stu-id="04c85-113">EXAMPLES</span></span>

### <span data-ttu-id="04c85-114">예제 1: 논리 앱의 트리거를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="04c85-115">이 명령은 LogicApp05라는 논리 앱에서 Trigger01이라는 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="04c85-116">예제 2: 논리 앱의 모든 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="04c85-117">이 명령은 LogicApp07이라는 논리 앱의 트리거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="04c85-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04c85-118">PARAMETERS</span></span>

### <span data-ttu-id="04c85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c85-119">-DefaultProfile</span></span>
<span data-ttu-id="04c85-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="04c85-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04c85-121">-Name</span><span class="sxs-lookup"><span data-stu-id="04c85-121">-Name</span></span>
<span data-ttu-id="04c85-122">이 cmdlet이 트리거를 받을 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c85-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c85-123">-ResourceGroupName</span></span>
<span data-ttu-id="04c85-124">이 cmdlet이 트리거를 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c85-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="04c85-125">-TriggerName</span></span>
<span data-ttu-id="04c85-126">이 cmdlet이 얻을 트리거의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04c85-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c85-127">CommonParameters</span></span>
<span data-ttu-id="04c85-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04c85-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c85-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="04c85-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c85-130">입력</span><span class="sxs-lookup"><span data-stu-id="04c85-130">INPUTS</span></span>

### <span data-ttu-id="04c85-131">System.String</span><span class="sxs-lookup"><span data-stu-id="04c85-131">System.String</span></span>

## <span data-ttu-id="04c85-132">출력</span><span class="sxs-lookup"><span data-stu-id="04c85-132">OUTPUTS</span></span>

### <span data-ttu-id="04c85-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="04c85-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="04c85-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04c85-134">NOTES</span></span>

## <span data-ttu-id="04c85-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04c85-135">RELATED LINKS</span></span>

[<span data-ttu-id="04c85-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="04c85-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="04c85-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="04c85-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


