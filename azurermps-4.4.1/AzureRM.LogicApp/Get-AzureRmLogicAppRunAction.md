---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 49968330f56fe0891adb9c5a62a1264700f53224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534927"
---
# <span data-ttu-id="b2f81-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="b2f81-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="b2f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2f81-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f81-103">논리 앱 실행에서 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2f81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2f81-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2f81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2f81-105">DESCRIPTION</span></span>
<span data-ttu-id="b2f81-106">**Get-AzureRmLogicAppRunAction** cmdlet은 논리 앱 실행에서 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="b2f81-107">이 cmdlet은 **Workflowrunaction** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="b2f81-108">논리 앱, 리소스 그룹 및 실행을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-108">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="b2f81-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b2f81-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b2f81-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b2f81-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b2f81-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b2f81-113">EXAMPLES</span></span>

### <span data-ttu-id="b2f81-114">예제 1: 논리 앱 실행에서 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2f81-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="b2f81-115">이 명령은 LogicAppRun56 이라는 실행에 대 한 LogicApp05 이라는 논리 앱에서 특정 논리 앱 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="b2f81-116">예제 2: 논리 앱 실행에서 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="b2f81-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="b2f81-117">이 명령은 LogicApp05 이라는 논리 앱의 LogicAppRun56 라는 실행에서 모든 논리 앱 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="b2f81-118">변수</span><span class="sxs-lookup"><span data-stu-id="b2f81-118">PARAMETERS</span></span>

### <span data-ttu-id="b2f81-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="b2f81-119">-ActionName</span></span>
<span data-ttu-id="b2f81-120">논리 앱 실행에서 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="b2f81-121">이 cmdlet은이 매개 변수에서 지정 하는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2f81-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b2f81-122">-Name</span></span>
<span data-ttu-id="b2f81-123">이 cmdlet이 동작을 가져오는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-123">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="b2f81-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2f81-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2f81-125">이 cmdlet이 동작을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-125">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="b2f81-126">-RunName</span><span class="sxs-lookup"><span data-stu-id="b2f81-126">-RunName</span></span>
<span data-ttu-id="b2f81-127">논리 앱 실행의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-127">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="b2f81-128">이 cmdlet은이 매개 변수에서 지정 하는 실행에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-128">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2f81-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2f81-129">-DefaultProfile</span></span>
<span data-ttu-id="b2f81-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2f81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f81-131">CommonParameters</span></span>
<span data-ttu-id="b2f81-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2f81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f81-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f81-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f81-134">입력</span><span class="sxs-lookup"><span data-stu-id="b2f81-134">INPUTS</span></span>

## <span data-ttu-id="b2f81-135">출력</span><span class="sxs-lookup"><span data-stu-id="b2f81-135">OUTPUTS</span></span>

### <span data-ttu-id="b2f81-136">Microsoft. Azure. i a m. 모델. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="b2f81-136">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="b2f81-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b2f81-137">NOTES</span></span>

## <span data-ttu-id="b2f81-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2f81-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2f81-139">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="b2f81-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="b2f81-140">중지-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="b2f81-140">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


