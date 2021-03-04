---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: c109839692ea20f1fbbcced50df9c4167322b1b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952459"
---
# <span data-ttu-id="90856-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="90856-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="90856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90856-102">SYNOPSIS</span></span>
<span data-ttu-id="90856-103">리소스 그룹에서 논리 앱을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="90856-104">구문</span><span class="sxs-lookup"><span data-stu-id="90856-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90856-105">설명</span><span class="sxs-lookup"><span data-stu-id="90856-105">DESCRIPTION</span></span>
<span data-ttu-id="90856-106">**Start-AzLogicApp** cmdlet은 Logic Apps 기능을 사용하여 논리 앱을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="90856-107">이름, 리소스 그룹 및 트리거를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="90856-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="90856-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="90856-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="90856-111">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90856-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="90856-112">예제</span><span class="sxs-lookup"><span data-stu-id="90856-112">EXAMPLES</span></span>

### <span data-ttu-id="90856-113">예제 1: 논리 앱 실행</span><span class="sxs-lookup"><span data-stu-id="90856-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="90856-114">이 명령은 ResourceGroup11이라는 리소스 그룹에서 논리 앱을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="90856-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90856-115">PARAMETERS</span></span>

### <span data-ttu-id="90856-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90856-116">-DefaultProfile</span></span>
<span data-ttu-id="90856-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90856-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90856-118">-Name</span><span class="sxs-lookup"><span data-stu-id="90856-118">-Name</span></span>
<span data-ttu-id="90856-119">이 cmdlet이 시작하는 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="90856-120">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="90856-120">-Parameters</span></span>
<span data-ttu-id="90856-121">논리 앱의 매개 변수 컬렉션 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="90856-122">해시 테이블, 사전 \<string\> 또는 \<string, WorkflowParameter\> 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="90856-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90856-123">-ResourceGroupName</span></span>
<span data-ttu-id="90856-124">이 cmdlet이 시작하는 논리 앱을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="90856-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="90856-125">-TriggerName</span></span>
<span data-ttu-id="90856-126">이 cmdlet이 시작하는 논리 앱의 트리거 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="90856-127">-확인</span><span class="sxs-lookup"><span data-stu-id="90856-127">-Confirm</span></span>
<span data-ttu-id="90856-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90856-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90856-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90856-129">-WhatIf</span></span>
<span data-ttu-id="90856-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="90856-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90856-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90856-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90856-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90856-132">CommonParameters</span></span>
<span data-ttu-id="90856-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90856-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90856-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="90856-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90856-135">입력</span><span class="sxs-lookup"><span data-stu-id="90856-135">INPUTS</span></span>

### <span data-ttu-id="90856-136">System.String</span><span class="sxs-lookup"><span data-stu-id="90856-136">System.String</span></span>

## <span data-ttu-id="90856-137">출력</span><span class="sxs-lookup"><span data-stu-id="90856-137">OUTPUTS</span></span>

### <span data-ttu-id="90856-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="90856-138">System.Void</span></span>

## <span data-ttu-id="90856-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90856-139">NOTES</span></span>

## <span data-ttu-id="90856-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90856-140">RELATED LINKS</span></span>

[<span data-ttu-id="90856-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="90856-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="90856-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="90856-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="90856-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="90856-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="90856-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="90856-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="90856-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="90856-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="90856-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="90856-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


