---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492835"
---
# <span data-ttu-id="3736d-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3736d-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="3736d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3736d-102">SYNOPSIS</span></span>
<span data-ttu-id="3736d-103">리소스 그룹에서 논리 앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="3736d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3736d-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3736d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3736d-105">DESCRIPTION</span></span>
<span data-ttu-id="3736d-106">**Remove-AzLogicApp** cmdlet은 Logic Apps 기능을 사용하여 리소스 그룹에서 논리 앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="3736d-107">논리 앱 및 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="3736d-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3736d-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3736d-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3736d-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3736d-112">예제</span><span class="sxs-lookup"><span data-stu-id="3736d-112">EXAMPLES</span></span>

### <span data-ttu-id="3736d-113">예제 1: 논리 앱 제거</span><span class="sxs-lookup"><span data-stu-id="3736d-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="3736d-114">이 명령은 리소스 그룹에서 논리 앱을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="3736d-115">이 명령에는 *명령에* 확인 메시지가 표시되지 않도록 하는 Force 매개 변수가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="3736d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3736d-116">PARAMETERS</span></span>

### <span data-ttu-id="3736d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3736d-117">-DefaultProfile</span></span>
<span data-ttu-id="3736d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3736d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3736d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3736d-119">-Force</span></span>
<span data-ttu-id="3736d-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3736d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3736d-121">-Name</span></span>
<span data-ttu-id="3736d-122">이 cmdlet이 제거하는 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3736d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3736d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3736d-124">이 cmdlet에서 제거하는 논리 앱을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3736d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3736d-125">-Confirm</span></span>
<span data-ttu-id="3736d-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3736d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3736d-127">-WhatIf</span></span>
<span data-ttu-id="3736d-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3736d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3736d-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3736d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3736d-130">CommonParameters</span></span>
<span data-ttu-id="3736d-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3736d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3736d-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3736d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3736d-133">입력</span><span class="sxs-lookup"><span data-stu-id="3736d-133">INPUTS</span></span>

### <span data-ttu-id="3736d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3736d-134">System.String</span></span>

## <span data-ttu-id="3736d-135">출력</span><span class="sxs-lookup"><span data-stu-id="3736d-135">OUTPUTS</span></span>

### <span data-ttu-id="3736d-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="3736d-136">System.Void</span></span>

## <span data-ttu-id="3736d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3736d-137">NOTES</span></span>

## <span data-ttu-id="3736d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3736d-138">RELATED LINKS</span></span>

[<span data-ttu-id="3736d-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3736d-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="3736d-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3736d-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="3736d-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3736d-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="3736d-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3736d-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


