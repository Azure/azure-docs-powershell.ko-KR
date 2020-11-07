---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: 1ec020aa93b1a7e6964e8f85eb8a02c6a9f895cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689457"
---
# <span data-ttu-id="4a85b-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a85b-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="4a85b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a85b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a85b-103">리소스 그룹에서 논리 앱을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="4a85b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a85b-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a85b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4a85b-105">DESCRIPTION</span></span>
<span data-ttu-id="4a85b-106">**AzLogicApp** Cmdlet은 로직 앱 기능을 사용 하 여 논리 앱을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="4a85b-107">이름, 리소스 그룹 및 트리거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="4a85b-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4a85b-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4a85b-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4a85b-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4a85b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4a85b-112">EXAMPLES</span></span>

### <span data-ttu-id="4a85b-113">예제 1: 논리 앱 실행</span><span class="sxs-lookup"><span data-stu-id="4a85b-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="4a85b-114">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 논리 앱을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="4a85b-115">변수</span><span class="sxs-lookup"><span data-stu-id="4a85b-115">PARAMETERS</span></span>

### <span data-ttu-id="4a85b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a85b-116">-DefaultProfile</span></span>
<span data-ttu-id="4a85b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4a85b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a85b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4a85b-118">-Name</span></span>
<span data-ttu-id="4a85b-119">이 cmdlet이 시작 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="4a85b-120">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a85b-120">-Parameters</span></span>
<span data-ttu-id="4a85b-121">논리 앱의 parameters 컬렉션 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="4a85b-122">해시 테이블, 사전 \< 문자열 \> 또는 사전 \< 문자열 workflowparameter를 지정 \> 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="4a85b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a85b-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a85b-124">이 cmdlet이 시작 하는 논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="4a85b-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="4a85b-125">-TriggerName</span></span>
<span data-ttu-id="4a85b-126">이 cmdlet이 시작 되는 논리 앱 트리거의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="4a85b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="4a85b-127">-Confirm</span></span>
<span data-ttu-id="4a85b-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a85b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a85b-129">-WhatIf</span></span>
<span data-ttu-id="4a85b-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a85b-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a85b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a85b-132">CommonParameters</span></span>
<span data-ttu-id="4a85b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a85b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a85b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a85b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a85b-135">입력</span><span class="sxs-lookup"><span data-stu-id="4a85b-135">INPUTS</span></span>

### <span data-ttu-id="4a85b-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a85b-136">System.String</span></span>

## <span data-ttu-id="4a85b-137">출력</span><span class="sxs-lookup"><span data-stu-id="4a85b-137">OUTPUTS</span></span>

### <span data-ttu-id="4a85b-138">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4a85b-138">System.Void</span></span>

## <span data-ttu-id="4a85b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4a85b-139">NOTES</span></span>

## <span data-ttu-id="4a85b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a85b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4a85b-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a85b-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="4a85b-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="4a85b-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="4a85b-143">새로운 AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a85b-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="4a85b-144">제거-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a85b-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="4a85b-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4a85b-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="4a85b-146">중지-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="4a85b-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


