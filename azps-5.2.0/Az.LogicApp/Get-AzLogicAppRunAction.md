---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356174"
---
# <span data-ttu-id="6a72a-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="6a72a-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="6a72a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a72a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a72a-103">논리 앱 실행에서 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="6a72a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6a72a-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a72a-105">설명</span><span class="sxs-lookup"><span data-stu-id="6a72a-105">DESCRIPTION</span></span>
<span data-ttu-id="6a72a-106">**Get-AzLogicAppRunAction** cmdlet은 논리 앱 실행에서 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="6a72a-107">이 cmdlet은 **WorkflowRunAction 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="6a72a-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="6a72a-108">논리 앱, 리소스 그룹 및 실행을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="6a72a-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6a72a-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6a72a-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6a72a-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6a72a-113">예제</span><span class="sxs-lookup"><span data-stu-id="6a72a-113">EXAMPLES</span></span>

### <span data-ttu-id="6a72a-114">예제 1: 논리 앱 실행에서 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="6a72a-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="6a72a-115">이 명령은 LogicAppRun56이라는 실행에 대한 LogicApp05라는 논리 앱에서 특정 논리 앱 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="6a72a-116">예제 2: 논리 앱 실행에서 모든 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="6a72a-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="6a72a-117">이 명령은 LogicApp05라는 논리 앱의 LogicAppRun56이라는 실행에서 모든 논리 앱 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="6a72a-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="6a72a-118">Example 3</span></span>

<span data-ttu-id="6a72a-119">이 명령은 LogicApp05라는 논리 앱의 LogicAppRun56이라는 실행에서 모든 논리 앱 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="6a72a-120">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="6a72a-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="6a72a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a72a-121">PARAMETERS</span></span>

### <span data-ttu-id="6a72a-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="6a72a-122">-ActionName</span></span>
<span data-ttu-id="6a72a-123">논리 앱 실행에서 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="6a72a-124">이 cmdlet은 이 매개 변수가 지정하는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a72a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a72a-125">-DefaultProfile</span></span>
<span data-ttu-id="6a72a-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6a72a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a72a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6a72a-127">-Name</span></span>
<span data-ttu-id="6a72a-128">이 cmdlet이 작업을 받을 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="6a72a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a72a-129">-ResourceGroupName</span></span>
<span data-ttu-id="6a72a-130">이 cmdlet이 작업을 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="6a72a-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="6a72a-131">-RunName</span></span>
<span data-ttu-id="6a72a-132">논리 앱 실행의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="6a72a-133">이 cmdlet은 이 매개 변수가 지정하는 실행에 대한 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a72a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a72a-134">CommonParameters</span></span>
<span data-ttu-id="6a72a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6a72a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a72a-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6a72a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a72a-137">입력</span><span class="sxs-lookup"><span data-stu-id="6a72a-137">INPUTS</span></span>

### <span data-ttu-id="6a72a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6a72a-138">System.String</span></span>

## <span data-ttu-id="6a72a-139">출력</span><span class="sxs-lookup"><span data-stu-id="6a72a-139">OUTPUTS</span></span>

### <span data-ttu-id="6a72a-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="6a72a-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="6a72a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6a72a-141">NOTES</span></span>

## <span data-ttu-id="6a72a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a72a-142">RELATED LINKS</span></span>

[<span data-ttu-id="6a72a-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="6a72a-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="6a72a-144">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="6a72a-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


