---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386142"
---
# <span data-ttu-id="ba211-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba211-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="ba211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba211-102">SYNOPSIS</span></span>
<span data-ttu-id="ba211-103">리소스 그룹에서 논리 앱을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="ba211-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba211-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba211-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba211-105">DESCRIPTION</span></span>
<span data-ttu-id="ba211-106">**Start-AzLogicApp** cmdlet은 Logic Apps 기능을 사용하여 논리 앱을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="ba211-107">이름, 리소스 그룹 및 트리거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="ba211-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba211-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba211-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba211-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba211-112">예제</span><span class="sxs-lookup"><span data-stu-id="ba211-112">EXAMPLES</span></span>

### <span data-ttu-id="ba211-113">예제 1: 논리 앱 실행</span><span class="sxs-lookup"><span data-stu-id="ba211-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="ba211-114">이 명령은 ResourceGroup11이라는 리소스 그룹에서 논리 앱을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ba211-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba211-115">PARAMETERS</span></span>

### <span data-ttu-id="ba211-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba211-116">-DefaultProfile</span></span>
<span data-ttu-id="ba211-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ba211-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba211-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ba211-118">-Name</span></span>
<span data-ttu-id="ba211-119">이 cmdlet이 시작하는 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ba211-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ba211-120">-Parameters</span></span>
<span data-ttu-id="ba211-121">논리 앱의 매개 변수 컬렉션 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="ba211-122">해시 테이블, 사전 \<string\> 또는 사전을 \<string, WorkflowParameter\> 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba211-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba211-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba211-124">이 cmdlet이 시작하는 논리 앱을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ba211-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ba211-125">-TriggerName</span></span>
<span data-ttu-id="ba211-126">이 cmdlet이 시작하는 논리 앱의 트리거 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ba211-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba211-127">-Confirm</span></span>
<span data-ttu-id="ba211-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba211-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba211-129">-WhatIf</span></span>
<span data-ttu-id="ba211-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ba211-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba211-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba211-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba211-132">CommonParameters</span></span>
<span data-ttu-id="ba211-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba211-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba211-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ba211-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba211-135">입력</span><span class="sxs-lookup"><span data-stu-id="ba211-135">INPUTS</span></span>

### <span data-ttu-id="ba211-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ba211-136">System.String</span></span>

## <span data-ttu-id="ba211-137">출력</span><span class="sxs-lookup"><span data-stu-id="ba211-137">OUTPUTS</span></span>

### <span data-ttu-id="ba211-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="ba211-138">System.Void</span></span>

## <span data-ttu-id="ba211-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba211-139">NOTES</span></span>

## <span data-ttu-id="ba211-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba211-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba211-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba211-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="ba211-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="ba211-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="ba211-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba211-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="ba211-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba211-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="ba211-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba211-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="ba211-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="ba211-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


