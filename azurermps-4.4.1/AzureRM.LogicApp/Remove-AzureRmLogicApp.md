---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 6b76440b2d9e61075ac19e5a6fa0846a95a77669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703711"
---
# <span data-ttu-id="e4de2-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e4de2-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="e4de2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4de2-102">SYNOPSIS</span></span>
<span data-ttu-id="e4de2-103">리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4de2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4de2-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4de2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e4de2-105">DESCRIPTION</span></span>
<span data-ttu-id="e4de2-106">**AzureRmLogicApp** Cmdlet은 논리 앱 기능을 사용 하 여 리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="e4de2-107">논리 앱 및 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="e4de2-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e4de2-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e4de2-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e4de2-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e4de2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e4de2-112">EXAMPLES</span></span>

### <span data-ttu-id="e4de2-113">예제 1: 논리 앱 제거</span><span class="sxs-lookup"><span data-stu-id="e4de2-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="e4de2-114">이 명령은 리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="e4de2-115">명령에 *Force* 매개 변수가 포함 되어 있어 명령에 대 한 확인 메시지가 표시 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="e4de2-116">변수</span><span class="sxs-lookup"><span data-stu-id="e4de2-116">PARAMETERS</span></span>

### <span data-ttu-id="e4de2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e4de2-117">-Force</span></span>
<span data-ttu-id="e4de2-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4de2-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e4de2-119">-Name</span></span>
<span data-ttu-id="e4de2-120">이 cmdlet이 제거 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-120">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4de2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4de2-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4de2-122">이 cmdlet이 제거 하는 논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-122">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4de2-123">-확인</span><span class="sxs-lookup"><span data-stu-id="e4de2-123">-Confirm</span></span>
<span data-ttu-id="e4de2-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4de2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4de2-125">-WhatIf</span></span>
<span data-ttu-id="e4de2-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4de2-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4de2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4de2-128">-DefaultProfile</span></span>
<span data-ttu-id="e4de2-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4de2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4de2-130">CommonParameters</span></span>
<span data-ttu-id="e4de2-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4de2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4de2-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4de2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4de2-133">입력</span><span class="sxs-lookup"><span data-stu-id="e4de2-133">INPUTS</span></span>

## <span data-ttu-id="e4de2-134">출력</span><span class="sxs-lookup"><span data-stu-id="e4de2-134">OUTPUTS</span></span>

### <span data-ttu-id="e4de2-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e4de2-135">System.Object</span></span>

## <span data-ttu-id="e4de2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e4de2-136">NOTES</span></span>

## <span data-ttu-id="e4de2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4de2-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4de2-138">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e4de2-138">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="e4de2-139">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e4de2-139">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="e4de2-140">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e4de2-140">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="e4de2-141">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e4de2-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


