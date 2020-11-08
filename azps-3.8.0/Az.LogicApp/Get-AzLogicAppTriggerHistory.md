---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044342"
---
# <span data-ttu-id="0eecd-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="0eecd-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="0eecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eecd-102">SYNOPSIS</span></span>
<span data-ttu-id="0eecd-103">논리 앱의 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="0eecd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0eecd-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eecd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0eecd-105">DESCRIPTION</span></span>
<span data-ttu-id="0eecd-106">**AzLogicAppTriggerHistory** Cmdlet은 로직 앱 기능에서 논리 앱의 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="0eecd-107">이 cmdlet은 **Workflowtriggerhistory** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="0eecd-108">논리 앱, 리소스 그룹 및 트리거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="0eecd-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0eecd-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0eecd-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0eecd-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0eecd-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0eecd-113">EXAMPLES</span></span>

### <span data-ttu-id="0eecd-114">예제 1: 논리 앱의 트리거 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="0eecd-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="0eecd-115">이 명령은 LogicApp03 이라는 논리 앱의 트리거에 대 한 특정 논리 앱 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="0eecd-116">예제 2: 논리 앱의 트리거 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="0eecd-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="0eecd-117">이 명령은 LogicApp07 이라는 논리 앱의 트리거에 대 한 워크플로 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="0eecd-118">변수</span><span class="sxs-lookup"><span data-stu-id="0eecd-118">PARAMETERS</span></span>

### <span data-ttu-id="0eecd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eecd-119">-DefaultProfile</span></span>
<span data-ttu-id="0eecd-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0eecd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eecd-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="0eecd-121">-HistoryName</span></span>
<span data-ttu-id="0eecd-122">이 cmdlet이 가져오는 기록의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-122">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eecd-123">-이름</span><span class="sxs-lookup"><span data-stu-id="0eecd-123">-Name</span></span>
<span data-ttu-id="0eecd-124">이 cmdlet이 트리거 기록을 가져오는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="0eecd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eecd-125">-ResourceGroupName</span></span>
<span data-ttu-id="0eecd-126">이 cmdlet에서 기록을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0eecd-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0eecd-127">-TriggerName</span></span>
<span data-ttu-id="0eecd-128">이 cmdlet에서 기록을 가져오는 트리거의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0eecd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eecd-129">CommonParameters</span></span>
<span data-ttu-id="0eecd-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eecd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eecd-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eecd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eecd-132">입력</span><span class="sxs-lookup"><span data-stu-id="0eecd-132">INPUTS</span></span>

### <span data-ttu-id="0eecd-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0eecd-133">System.String</span></span>

## <span data-ttu-id="0eecd-134">출력</span><span class="sxs-lookup"><span data-stu-id="0eecd-134">OUTPUTS</span></span>

### <span data-ttu-id="0eecd-135">Microsoft. Azure.-... WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="0eecd-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="0eecd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0eecd-136">NOTES</span></span>

## <span data-ttu-id="0eecd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0eecd-137">RELATED LINKS</span></span>

[<span data-ttu-id="0eecd-138">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0eecd-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="0eecd-139">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="0eecd-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="0eecd-140">시작-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0eecd-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


