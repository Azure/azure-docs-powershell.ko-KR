---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008971"
---
# <span data-ttu-id="5f530-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="5f530-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="5f530-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f530-102">SYNOPSIS</span></span>

<span data-ttu-id="5f530-103">논리 앱 실행에서 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="5f530-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f530-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f530-105">설명</span><span class="sxs-lookup"><span data-stu-id="5f530-105">DESCRIPTION</span></span>

<span data-ttu-id="5f530-106">**Get-AzLogicAppRunAction** cmdlet은 논리 앱 실행에서 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="5f530-107">이 cmdlet은 **WorkflowRunAction** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="5f530-108">논리 앱, 리소스 그룹 및 실행을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="5f530-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5f530-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5f530-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5f530-112">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5f530-113">예제</span><span class="sxs-lookup"><span data-stu-id="5f530-113">EXAMPLES</span></span>

### <span data-ttu-id="5f530-114">예제 1: Logic App 실행에서 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="5f530-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
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

<span data-ttu-id="5f530-115">이 명령은 ID 08559251844236971838804972CU26을 사용하여 실행에 대한 LogicApp05라는 논리 앱에서 특정 논리 앱 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="5f530-116">예제 2: Logic App 실행에서 모든 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="5f530-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="5f530-117">이 명령은 LogicApp05라는 논리 앱의 식별자 0855925184423369718380498702CU26을 사용하여 실행에서 모든 논리 앱 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="5f530-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5f530-118">PARAMETERS</span></span>

### <span data-ttu-id="5f530-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="5f530-119">-ActionName</span></span>

<span data-ttu-id="5f530-120">논리 앱 실행에서 작업 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="5f530-121">이 cmdlet은 이 매개 변수가 지정하는 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f530-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f530-122">-DefaultProfile</span></span>

<span data-ttu-id="5f530-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5f530-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f530-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="5f530-124">-FollowNextPageLink</span></span>

<span data-ttu-id="5f530-125">cmdlet이 다음 페이지 링크를 따라야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="5f530-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="5f530-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="5f530-127">FollowNextPageLink를 사용하는 경우 다음 페이지 링크를 팔로우할 수 있는 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="5f530-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5f530-128">-Name</span></span>

<span data-ttu-id="5f530-129">이 cmdlet에서 작업을 수행하게 하는 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="5f530-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f530-130">-ResourceGroupName</span></span>

<span data-ttu-id="5f530-131">이 cmdlet에서 작업을 수행하게 하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="5f530-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="5f530-132">-RunName</span></span>

<span data-ttu-id="5f530-133">논리 앱의 실행 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="5f530-134">이 cmdlet은 이 매개 변수가 지정하는 실행에 대한 작업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f530-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f530-135">CommonParameters</span></span>

<span data-ttu-id="5f530-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f530-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f530-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f530-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f530-138">입력</span><span class="sxs-lookup"><span data-stu-id="5f530-138">INPUTS</span></span>

### <span data-ttu-id="5f530-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5f530-139">System.String</span></span>

## <span data-ttu-id="5f530-140">출력</span><span class="sxs-lookup"><span data-stu-id="5f530-140">OUTPUTS</span></span>

### <span data-ttu-id="5f530-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="5f530-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="5f530-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f530-142">NOTES</span></span>

## <span data-ttu-id="5f530-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f530-143">RELATED LINKS</span></span>

[<span data-ttu-id="5f530-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="5f530-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="5f530-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="5f530-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
