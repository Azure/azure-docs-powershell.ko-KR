---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 1e847131a67e55fa7a9c520c6ce5a5d96f0475f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386226"
---
# <span data-ttu-id="b5dd0-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="b5dd0-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="b5dd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dd0-103">논리 앱의 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="b5dd0-104">구문</span><span class="sxs-lookup"><span data-stu-id="b5dd0-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5dd0-105">설명</span><span class="sxs-lookup"><span data-stu-id="b5dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="b5dd0-106">**Get-AzLogicAppRunHistory** cmdlet은 논리 앱의 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="b5dd0-107">이 cmdlet은 **WorkflowRun** 개체의 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="b5dd0-108">논리 앱 및 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="b5dd0-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b5dd0-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b5dd0-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b5dd0-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b5dd0-113">예제</span><span class="sxs-lookup"><span data-stu-id="b5dd0-113">EXAMPLES</span></span>

### <span data-ttu-id="b5dd0-114">예제 1: 논리 앱의 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="b5dd0-115">이 명령은 LogicApp03이라는 논리 앱의 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="b5dd0-116">예제 2: 논리 앱 실행 다운로드</span><span class="sxs-lookup"><span data-stu-id="b5dd0-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="b5dd0-117">이 명령은 LogicApp03이라는 논리 앱에 대해 실행된 특정 논리 앱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="b5dd0-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="b5dd0-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="b5dd0-119">이 명령은 NextPageLink를 따라 LogicApp03이라는 논리 앱의 전체 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="b5dd0-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="b5dd0-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="b5dd0-121">이 명령은 NextPageLink를 따라 결과 크기를 두 페이지로 제한하여 LogicApp03이라는 논리 앱의 실행 기록의 처음 두 페이지를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="b5dd0-122">각 페이지에는 30개 결과가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="b5dd0-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5dd0-123">PARAMETERS</span></span>

### <span data-ttu-id="b5dd0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5dd0-124">-DefaultProfile</span></span>
<span data-ttu-id="b5dd0-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b5dd0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5dd0-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="b5dd0-126">-FollowNextPageLink</span></span>
<span data-ttu-id="b5dd0-127">cmdlet이 다음 페이지 링크를 따라야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="b5dd0-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="b5dd0-128">-MaximumFollowNextPageLink</span></span>
<span data-ttu-id="b5dd0-129">FollowNextPageLink를 사용하는 경우 다음 페이지 링크를 따를 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="b5dd0-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b5dd0-130">-Name</span></span>
<span data-ttu-id="b5dd0-131">이 cmdlet이 실행 기록을 얻을 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5dd0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5dd0-132">-ResourceGroupName</span></span>
<span data-ttu-id="b5dd0-133">논리 앱을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="b5dd0-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="b5dd0-134">-RunName</span></span>
<span data-ttu-id="b5dd0-135">논리 앱의 실행 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="b5dd0-136">이 cmdlet은 이 cmdlet이 지정하는 워크플로 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="b5dd0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dd0-137">CommonParameters</span></span>
<span data-ttu-id="b5dd0-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dd0-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5dd0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dd0-140">입력</span><span class="sxs-lookup"><span data-stu-id="b5dd0-140">INPUTS</span></span>

### <span data-ttu-id="b5dd0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b5dd0-141">System.String</span></span>

## <span data-ttu-id="b5dd0-142">출력</span><span class="sxs-lookup"><span data-stu-id="b5dd0-142">OUTPUTS</span></span>

### <span data-ttu-id="b5dd0-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="b5dd0-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="b5dd0-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5dd0-144">NOTES</span></span>

## <span data-ttu-id="b5dd0-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5dd0-145">RELATED LINKS</span></span>

[<span data-ttu-id="b5dd0-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="b5dd0-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="b5dd0-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b5dd0-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="b5dd0-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="b5dd0-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


