---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 3650e04b8c6d254b396072c55d39cde38a1328f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531692"
---
# <span data-ttu-id="fe23e-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe23e-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="fe23e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe23e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe23e-103">리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe23e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe23e-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe23e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe23e-105">DESCRIPTION</span></span>
<span data-ttu-id="fe23e-106">**AzureRmLogicApp** Cmdlet은 논리 앱 기능을 사용 하 여 리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="fe23e-107">논리 앱 및 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="fe23e-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fe23e-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fe23e-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fe23e-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fe23e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="fe23e-112">EXAMPLES</span></span>

### <span data-ttu-id="fe23e-113">예제 1: 논리 앱 제거</span><span class="sxs-lookup"><span data-stu-id="fe23e-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="fe23e-114">이 명령은 리소스 그룹에서 논리 앱을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="fe23e-115">명령에 *Force* 매개 변수가 포함 되어 있어 명령에 대 한 확인 메시지가 표시 되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="fe23e-116">변수</span><span class="sxs-lookup"><span data-stu-id="fe23e-116">PARAMETERS</span></span>

### <span data-ttu-id="fe23e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe23e-117">-DefaultProfile</span></span>
<span data-ttu-id="fe23e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fe23e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fe23e-119">-Force</span></span>
<span data-ttu-id="fe23e-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fe23e-121">-Name</span></span>
<span data-ttu-id="fe23e-122">이 cmdlet이 제거 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe23e-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe23e-124">이 cmdlet이 제거 하는 논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe23e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="fe23e-125">-Confirm</span></span>
<span data-ttu-id="fe23e-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe23e-127">-WhatIf</span></span>
<span data-ttu-id="fe23e-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe23e-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe23e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe23e-130">CommonParameters</span></span>
<span data-ttu-id="fe23e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe23e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe23e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe23e-133">입력</span><span class="sxs-lookup"><span data-stu-id="fe23e-133">INPUTS</span></span>

### <span data-ttu-id="fe23e-134">않아야</span><span class="sxs-lookup"><span data-stu-id="fe23e-134">None</span></span>
<span data-ttu-id="fe23e-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe23e-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe23e-136">출력</span><span class="sxs-lookup"><span data-stu-id="fe23e-136">OUTPUTS</span></span>

### <span data-ttu-id="fe23e-137">System. 개체</span><span class="sxs-lookup"><span data-stu-id="fe23e-137">System.Object</span></span>

## <span data-ttu-id="fe23e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="fe23e-138">NOTES</span></span>

## <span data-ttu-id="fe23e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe23e-139">RELATED LINKS</span></span>

[<span data-ttu-id="fe23e-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe23e-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="fe23e-141">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe23e-141">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="fe23e-142">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe23e-142">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="fe23e-143">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe23e-143">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


