---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033897"
---
# <span data-ttu-id="6190c-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6190c-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="6190c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6190c-102">SYNOPSIS</span></span>
<span data-ttu-id="6190c-103">리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="6190c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6190c-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6190c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6190c-105">DESCRIPTION</span></span>
<span data-ttu-id="6190c-106">**AzLogicApp** Cmdlet은 논리 앱 기능을 사용 하 여 리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="6190c-107">논리 앱 및 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="6190c-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6190c-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6190c-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6190c-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6190c-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6190c-112">EXAMPLES</span></span>

### <span data-ttu-id="6190c-113">예제 1: 논리 앱 제거</span><span class="sxs-lookup"><span data-stu-id="6190c-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="6190c-114">이 명령은 리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="6190c-115">명령에 *Force* 매개 변수가 포함 되어 있어 명령에 대 한 확인 메시지가 표시 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="6190c-116">변수</span><span class="sxs-lookup"><span data-stu-id="6190c-116">PARAMETERS</span></span>

### <span data-ttu-id="6190c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6190c-117">-DefaultProfile</span></span>
<span data-ttu-id="6190c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6190c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6190c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6190c-119">-Force</span></span>
<span data-ttu-id="6190c-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6190c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6190c-121">-Name</span></span>
<span data-ttu-id="6190c-122">이 cmdlet이 제거 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6190c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6190c-123">-ResourceGroupName</span></span>
<span data-ttu-id="6190c-124">이 cmdlet이 제거 하는 논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6190c-125">-확인</span><span class="sxs-lookup"><span data-stu-id="6190c-125">-Confirm</span></span>
<span data-ttu-id="6190c-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6190c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6190c-127">-WhatIf</span></span>
<span data-ttu-id="6190c-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6190c-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6190c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6190c-130">CommonParameters</span></span>
<span data-ttu-id="6190c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6190c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6190c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6190c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6190c-133">입력</span><span class="sxs-lookup"><span data-stu-id="6190c-133">INPUTS</span></span>

### <span data-ttu-id="6190c-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6190c-134">System.String</span></span>

## <span data-ttu-id="6190c-135">출력</span><span class="sxs-lookup"><span data-stu-id="6190c-135">OUTPUTS</span></span>

### <span data-ttu-id="6190c-136">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6190c-136">System.Void</span></span>

## <span data-ttu-id="6190c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6190c-137">NOTES</span></span>

## <span data-ttu-id="6190c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6190c-138">RELATED LINKS</span></span>

[<span data-ttu-id="6190c-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6190c-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="6190c-140">새로운 AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6190c-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="6190c-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6190c-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="6190c-142">시작-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6190c-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


