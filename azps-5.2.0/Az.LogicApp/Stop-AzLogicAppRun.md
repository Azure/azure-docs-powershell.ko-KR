---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343562"
---
# <span data-ttu-id="a78e7-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a78e7-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="a78e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a78e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a78e7-103">논리 앱의 실행을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="a78e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="a78e7-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a78e7-105">설명</span><span class="sxs-lookup"><span data-stu-id="a78e7-105">DESCRIPTION</span></span>
<span data-ttu-id="a78e7-106">**Stop-AzLogicAppRun** cmdlet은 논리 앱의 실행을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="a78e7-107">논리 앱, 리소스 그룹 및 실행을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="a78e7-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a78e7-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a78e7-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a78e7-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a78e7-112">예제</span><span class="sxs-lookup"><span data-stu-id="a78e7-112">EXAMPLES</span></span>

### <span data-ttu-id="a78e7-113">예제 1: 논리 앱 실행 취소</span><span class="sxs-lookup"><span data-stu-id="a78e7-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="a78e7-114">이 명령은 LogicApp03이라는 논리 앱의 실행을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="a78e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a78e7-115">PARAMETERS</span></span>

### <span data-ttu-id="a78e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78e7-116">-DefaultProfile</span></span>
<span data-ttu-id="a78e7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a78e7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a78e7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a78e7-118">-Force</span></span>
<span data-ttu-id="a78e7-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a78e7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a78e7-120">-Name</span></span>
<span data-ttu-id="a78e7-121">이 cmdlet이 실행을 취소하는 논리 앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="a78e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="a78e7-123">이 cmdlet이 실행을 취소하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="a78e7-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="a78e7-124">-RunName</span></span>
<span data-ttu-id="a78e7-125">이 cmdlet이 취소하는 논리 앱 실행의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="a78e7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a78e7-126">-Confirm</span></span>
<span data-ttu-id="a78e7-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a78e7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78e7-128">-WhatIf</span></span>
<span data-ttu-id="a78e7-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a78e7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a78e7-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a78e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78e7-131">CommonParameters</span></span>
<span data-ttu-id="a78e7-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a78e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78e7-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a78e7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78e7-134">입력</span><span class="sxs-lookup"><span data-stu-id="a78e7-134">INPUTS</span></span>

### <span data-ttu-id="a78e7-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a78e7-135">System.String</span></span>

## <span data-ttu-id="a78e7-136">출력</span><span class="sxs-lookup"><span data-stu-id="a78e7-136">OUTPUTS</span></span>

### <span data-ttu-id="a78e7-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="a78e7-137">System.Void</span></span>

## <span data-ttu-id="a78e7-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a78e7-138">NOTES</span></span>

## <span data-ttu-id="a78e7-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a78e7-139">RELATED LINKS</span></span>

[<span data-ttu-id="a78e7-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a78e7-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


