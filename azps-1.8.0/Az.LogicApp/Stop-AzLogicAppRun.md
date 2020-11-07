---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: eedfc6f0ab4bc150c2f1516a937fc47320b712be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867574"
---
# <span data-ttu-id="4f194-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="4f194-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="4f194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f194-102">SYNOPSIS</span></span>
<span data-ttu-id="4f194-103">논리 앱의 실행을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="4f194-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f194-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f194-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f194-105">DESCRIPTION</span></span>
<span data-ttu-id="4f194-106">**AzLogicAppRun** cmdlet은 논리 앱의 실행을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="4f194-107">논리 앱, 리소스 그룹 및 실행을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="4f194-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4f194-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4f194-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4f194-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4f194-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4f194-112">EXAMPLES</span></span>

### <span data-ttu-id="4f194-113">예제 1: 논리 앱 실행 취소</span><span class="sxs-lookup"><span data-stu-id="4f194-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="4f194-114">이 명령은 LogicApp03 이라는 논리 앱의 실행을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="4f194-115">변수</span><span class="sxs-lookup"><span data-stu-id="4f194-115">PARAMETERS</span></span>

### <span data-ttu-id="4f194-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f194-116">-DefaultProfile</span></span>
<span data-ttu-id="4f194-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f194-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f194-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4f194-118">-Force</span></span>
<span data-ttu-id="4f194-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f194-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4f194-120">-Name</span></span>
<span data-ttu-id="4f194-121">이 cmdlet이 실행을 취소 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="4f194-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f194-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f194-123">이 cmdlet이 실행을 취소 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="4f194-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="4f194-124">-RunName</span></span>
<span data-ttu-id="4f194-125">이 cmdlet이 취소 하는 논리 앱 실행의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="4f194-126">-확인</span><span class="sxs-lookup"><span data-stu-id="4f194-126">-Confirm</span></span>
<span data-ttu-id="4f194-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f194-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f194-128">-WhatIf</span></span>
<span data-ttu-id="4f194-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f194-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f194-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f194-131">CommonParameters</span></span>
<span data-ttu-id="4f194-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f194-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f194-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f194-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f194-134">입력</span><span class="sxs-lookup"><span data-stu-id="4f194-134">INPUTS</span></span>

### <span data-ttu-id="4f194-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f194-135">System.String</span></span>

## <span data-ttu-id="4f194-136">출력</span><span class="sxs-lookup"><span data-stu-id="4f194-136">OUTPUTS</span></span>

### <span data-ttu-id="4f194-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="4f194-137">System.Void</span></span>

## <span data-ttu-id="4f194-138">상속자</span><span class="sxs-lookup"><span data-stu-id="4f194-138">NOTES</span></span>

## <span data-ttu-id="4f194-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f194-139">RELATED LINKS</span></span>

[<span data-ttu-id="4f194-140">시작-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="4f194-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


