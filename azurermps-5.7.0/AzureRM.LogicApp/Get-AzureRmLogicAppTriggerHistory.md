---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 05a47123974ea3aed871e2ada3fb14981f654b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528116"
---
# <span data-ttu-id="b4e78-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="b4e78-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="b4e78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e78-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e78-103">논리 앱의 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4e78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4e78-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e78-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4e78-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e78-106">**AzureRmLogicAppTriggerHistory** Cmdlet은 로직 앱 기능에서 논리 앱의 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="b4e78-107">이 cmdlet은 **Workflowtriggerhistory** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="b4e78-108">논리 앱, 리소스 그룹 및 트리거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-108">Specify the logic app, resource group, and trigger.</span></span>

<span data-ttu-id="b4e78-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b4e78-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b4e78-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b4e78-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b4e78-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b4e78-113">EXAMPLES</span></span>

### <span data-ttu-id="b4e78-114">예제 1: 논리 앱의 트리거 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4e78-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="b4e78-115">이 명령은 LogicApp03 이라는 논리 앱의 트리거에 대 한 특정 논리 앱 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="b4e78-116">예제 2: 논리 앱의 트리거 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4e78-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="b4e78-117">이 명령은 LogicApp07 이라는 논리 앱의 트리거에 대 한 워크플로 트리거 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="b4e78-118">변수</span><span class="sxs-lookup"><span data-stu-id="b4e78-118">PARAMETERS</span></span>

### <span data-ttu-id="b4e78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e78-119">-DefaultProfile</span></span>
<span data-ttu-id="b4e78-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4e78-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e78-121">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="b4e78-121">-HistoryName</span></span>
<span data-ttu-id="b4e78-122">이 cmdlet이 가져오는 기록의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-122">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e78-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b4e78-123">-Name</span></span>
<span data-ttu-id="b4e78-124">이 cmdlet이 트리거 기록을 가져오는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e78-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4e78-126">이 cmdlet에서 기록을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e78-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="b4e78-127">-TriggerName</span></span>
<span data-ttu-id="b4e78-128">이 cmdlet에서 기록을 가져오는 트리거의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e78-129">CommonParameters</span></span>
<span data-ttu-id="b4e78-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e78-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e78-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e78-132">입력</span><span class="sxs-lookup"><span data-stu-id="b4e78-132">INPUTS</span></span>

### <span data-ttu-id="b4e78-133">않아야</span><span class="sxs-lookup"><span data-stu-id="b4e78-133">None</span></span>
<span data-ttu-id="b4e78-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4e78-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4e78-135">출력</span><span class="sxs-lookup"><span data-stu-id="b4e78-135">OUTPUTS</span></span>

### <span data-ttu-id="b4e78-136">Microsoft. Azure.-... WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="b4e78-136">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="b4e78-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b4e78-137">NOTES</span></span>

## <span data-ttu-id="b4e78-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4e78-138">RELATED LINKS</span></span>

[<span data-ttu-id="b4e78-139">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="b4e78-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="b4e78-140">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="b4e78-140">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="b4e78-141">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b4e78-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


