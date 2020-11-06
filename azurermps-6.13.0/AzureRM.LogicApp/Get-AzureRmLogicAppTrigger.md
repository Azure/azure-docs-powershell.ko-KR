---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: 6066a08774be9f5e3fa67a07b0d868947384f518
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535851"
---
# <span data-ttu-id="07a26-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="07a26-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="07a26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a26-102">SYNOPSIS</span></span>
<span data-ttu-id="07a26-103">논리 앱의 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07a26-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07a26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07a26-105">DESCRIPTION</span></span>
<span data-ttu-id="07a26-106">**Get-AzureRmLogicAppTrigger** cmdlet은 논리 앱에서 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="07a26-107">이 cmdlet은 **Workflowtrigger** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="07a26-108">워크플로, 리소스 그룹 및 트리거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="07a26-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="07a26-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="07a26-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="07a26-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="07a26-113">예제의</span><span class="sxs-lookup"><span data-stu-id="07a26-113">EXAMPLES</span></span>

### <span data-ttu-id="07a26-114">예제 1: 논리 앱의 트리거 가져오기</span><span class="sxs-lookup"><span data-stu-id="07a26-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="07a26-115">이 명령은 LogicApp05 이라는 논리 앱에서 Trigger01 이라는 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="07a26-116">예제 2: 논리 앱의 모든 트리거 가져오기</span><span class="sxs-lookup"><span data-stu-id="07a26-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="07a26-117">이 명령은 LogicApp07 이라는 논리 앱의 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="07a26-118">변수</span><span class="sxs-lookup"><span data-stu-id="07a26-118">PARAMETERS</span></span>

### <span data-ttu-id="07a26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a26-119">-DefaultProfile</span></span>
<span data-ttu-id="07a26-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="07a26-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07a26-121">-이름</span><span class="sxs-lookup"><span data-stu-id="07a26-121">-Name</span></span>
<span data-ttu-id="07a26-122">이 cmdlet이 트리거를 가져오는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="07a26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a26-123">-ResourceGroupName</span></span>
<span data-ttu-id="07a26-124">이 cmdlet이 트리거를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="07a26-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="07a26-125">-TriggerName</span></span>
<span data-ttu-id="07a26-126">이 cmdlet이 가져오는 트리거의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07a26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a26-127">CommonParameters</span></span>
<span data-ttu-id="07a26-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07a26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a26-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a26-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a26-130">입력</span><span class="sxs-lookup"><span data-stu-id="07a26-130">INPUTS</span></span>

### <span data-ttu-id="07a26-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07a26-131">System.String</span></span>

## <span data-ttu-id="07a26-132">출력</span><span class="sxs-lookup"><span data-stu-id="07a26-132">OUTPUTS</span></span>

### <span data-ttu-id="07a26-133">Microsoft. Azure. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="07a26-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="07a26-134">상속자</span><span class="sxs-lookup"><span data-stu-id="07a26-134">NOTES</span></span>

## <span data-ttu-id="07a26-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07a26-135">RELATED LINKS</span></span>

[<span data-ttu-id="07a26-136">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="07a26-136">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="07a26-137">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="07a26-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


