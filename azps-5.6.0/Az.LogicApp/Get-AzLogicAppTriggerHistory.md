---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 7c0d34ad56021e2fb4f74aef1bed41ca38c918c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008880"
---
# <span data-ttu-id="83825-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="83825-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="83825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83825-102">SYNOPSIS</span></span>

<span data-ttu-id="83825-103">논리 앱에서 트리거의 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="83825-104">구문</span><span class="sxs-lookup"><span data-stu-id="83825-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83825-105">설명</span><span class="sxs-lookup"><span data-stu-id="83825-105">DESCRIPTION</span></span>

<span data-ttu-id="83825-106">**Get-AzLogicAppTriggerHistory** cmdlet은 Logic Apps 기능의 논리 앱에서 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="83825-107">이 cmdlet은 **WorkflowTriggerHistory 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="83825-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="83825-108">논리 앱, 리소스 그룹 및 트리거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="83825-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="83825-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="83825-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="83825-112">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83825-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="83825-113">예제</span><span class="sxs-lookup"><span data-stu-id="83825-113">EXAMPLES</span></span>

### <span data-ttu-id="83825-114">예제 1: 논리 앱의 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-114">Example 1: Get a trigger history of a logic app</span></span>

```powershell
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

<span data-ttu-id="83825-115">이 명령은 LogicApp03이라는 논리 앱에서 트리거에 대한 특정 논리 앱 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="83825-116">예제 2: 논리 앱의 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-116">Example 2: Get trigger histories of a logic app</span></span>

```powershell
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

<span data-ttu-id="83825-117">이 명령은 LogicApp07이라는 논리 앱에서 트리거에 대한 워크플로 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="83825-118">예제 3: 논리 앱의 전체 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="83825-119">이 명령은 NextPageLink를 따라 LogicApp08이라는 논리 앱의 트리거에 대한 전체 워크플로 트리거 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="83825-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="83825-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="83825-121">이 명령은 NextPageLink를 따라 결과 크기를 두 페이지로 제한하여 LogicApp09라는 논리 앱의 트리거에 대한 워크플로 트리거 기록의 처음 두 페이지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="83825-122">각 페이지에는 30개 결과가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83825-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="83825-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="83825-123">PARAMETERS</span></span>

### <span data-ttu-id="83825-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83825-124">-DefaultProfile</span></span>

<span data-ttu-id="83825-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="83825-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83825-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="83825-126">-FollowNextPageLink</span></span>

<span data-ttu-id="83825-127">cmdlet이 다음 페이지 링크를 따라야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="83825-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83825-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="83825-128">-HistoryName</span></span>

<span data-ttu-id="83825-129">이 cmdlet이 얻을 기록의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-129">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="83825-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="83825-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="83825-131">FollowNextPageLink를 사용하는 경우 다음 페이지 링크를 팔로우할 수 있는 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83825-132">-Name</span><span class="sxs-lookup"><span data-stu-id="83825-132">-Name</span></span>

<span data-ttu-id="83825-133">이 cmdlet에서 트리거 기록을 얻을 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="83825-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83825-134">-ResourceGroupName</span></span>

<span data-ttu-id="83825-135">이 cmdlet이 기록을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="83825-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="83825-136">-TriggerName</span></span>

<span data-ttu-id="83825-137">이 cmdlet이 기록을 얻을 트리거의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="83825-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83825-138">CommonParameters</span></span>

<span data-ttu-id="83825-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83825-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83825-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83825-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83825-141">입력</span><span class="sxs-lookup"><span data-stu-id="83825-141">INPUTS</span></span>

### <span data-ttu-id="83825-142">System.String</span><span class="sxs-lookup"><span data-stu-id="83825-142">System.String</span></span>

## <span data-ttu-id="83825-143">출력</span><span class="sxs-lookup"><span data-stu-id="83825-143">OUTPUTS</span></span>

### <span data-ttu-id="83825-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="83825-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="83825-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83825-145">NOTES</span></span>

## <span data-ttu-id="83825-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83825-146">RELATED LINKS</span></span>

[<span data-ttu-id="83825-147">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="83825-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="83825-148">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="83825-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="83825-149">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="83825-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
