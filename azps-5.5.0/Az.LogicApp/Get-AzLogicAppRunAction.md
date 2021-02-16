---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 175667480977e55cc93486f252a8f84080c64b5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180369"
---
# <span data-ttu-id="13f29-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="13f29-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="13f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f29-102">SYNOPSIS</span></span>

<span data-ttu-id="13f29-103">논리 앱 실행에서 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="13f29-104">구문</span><span class="sxs-lookup"><span data-stu-id="13f29-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13f29-105">설명</span><span class="sxs-lookup"><span data-stu-id="13f29-105">DESCRIPTION</span></span>

<span data-ttu-id="13f29-106">**Get-AzLogicAppRunAction** cmdlet은 논리 앱 실행에서 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="13f29-107">이 cmdlet은 **WorkflowRunAction 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="13f29-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="13f29-108">논리 앱, 리소스 그룹 및 실행을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="13f29-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="13f29-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="13f29-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="13f29-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="13f29-113">예제</span><span class="sxs-lookup"><span data-stu-id="13f29-113">EXAMPLES</span></span>

### <span data-ttu-id="13f29-114">예제 1: 논리 앱 실행에서 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="13f29-114">Example 1: Get an action from a Logic App run</span></span>

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

<span data-ttu-id="13f29-115">이 명령은 식별자가 0858592518442369718380498702CU26인 실행을 위해 LogicApp05라는 논리 앱에서 특정 논리 앱 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="13f29-116">예제 2: 논리 앱 실행에서 모든 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="13f29-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="13f29-117">이 명령은 LogicApp05라는 논리 앱의 식별자 08585925184423369718380498702CU26을 사용하여 실행에서 모든 논리 앱 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="13f29-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13f29-118">PARAMETERS</span></span>

### <span data-ttu-id="13f29-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="13f29-119">-ActionName</span></span>

<span data-ttu-id="13f29-120">논리 앱 실행에서 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="13f29-121">이 cmdlet은 이 매개 변수가 지정하는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="13f29-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f29-122">-DefaultProfile</span></span>

<span data-ttu-id="13f29-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="13f29-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13f29-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="13f29-124">-FollowNextPageLink</span></span>

<span data-ttu-id="13f29-125">cmdlet이 다음 페이지 링크를 따라야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="13f29-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="13f29-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="13f29-127">FollowNextPageLink를 사용하는 경우 다음 페이지 링크를 따를 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="13f29-128">-Name</span><span class="sxs-lookup"><span data-stu-id="13f29-128">-Name</span></span>

<span data-ttu-id="13f29-129">이 cmdlet이 작업을 받을 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="13f29-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f29-130">-ResourceGroupName</span></span>

<span data-ttu-id="13f29-131">이 cmdlet이 작업을 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="13f29-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="13f29-132">-RunName</span></span>

<span data-ttu-id="13f29-133">논리 앱 실행의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="13f29-134">이 cmdlet은 이 매개 변수가 지정하는 실행에 대한 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="13f29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f29-135">CommonParameters</span></span>

<span data-ttu-id="13f29-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13f29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f29-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13f29-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f29-138">입력</span><span class="sxs-lookup"><span data-stu-id="13f29-138">INPUTS</span></span>

### <span data-ttu-id="13f29-139">System.String</span><span class="sxs-lookup"><span data-stu-id="13f29-139">System.String</span></span>

## <span data-ttu-id="13f29-140">출력</span><span class="sxs-lookup"><span data-stu-id="13f29-140">OUTPUTS</span></span>

### <span data-ttu-id="13f29-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="13f29-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="13f29-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13f29-142">NOTES</span></span>

## <span data-ttu-id="13f29-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13f29-143">RELATED LINKS</span></span>

[<span data-ttu-id="13f29-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="13f29-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="13f29-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="13f29-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
