---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711711"
---
# <span data-ttu-id="038d5-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="038d5-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="038d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="038d5-102">SYNOPSIS</span></span>
<span data-ttu-id="038d5-103">리소스 그룹에서 논리 앱을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="038d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="038d5-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="038d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="038d5-105">DESCRIPTION</span></span>
<span data-ttu-id="038d5-106">**AzureRmLogicApp** Cmdlet은 로직 앱 기능을 사용 하 여 논리 앱을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="038d5-107">이름, 리소스 그룹 및 트리거를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="038d5-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="038d5-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="038d5-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="038d5-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="038d5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="038d5-112">EXAMPLES</span></span>

### <span data-ttu-id="038d5-113">예제 1: 논리 앱 실행</span><span class="sxs-lookup"><span data-stu-id="038d5-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="038d5-114">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 논리 앱을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="038d5-115">변수</span><span class="sxs-lookup"><span data-stu-id="038d5-115">PARAMETERS</span></span>

### <span data-ttu-id="038d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038d5-116">-DefaultProfile</span></span>
<span data-ttu-id="038d5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="038d5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="038d5-118">-이름</span><span class="sxs-lookup"><span data-stu-id="038d5-118">-Name</span></span>
<span data-ttu-id="038d5-119">이 cmdlet이 시작 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="038d5-120">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="038d5-120">-Parameters</span></span>
<span data-ttu-id="038d5-121">논리 앱의 parameters 컬렉션 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="038d5-122">해시 테이블, 사전 \<string\> 또는 사전을 지정 \<string, WorkflowParameter\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="038d5-124">이 cmdlet이 시작 하는 논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="038d5-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="038d5-125">-TriggerName</span></span>
<span data-ttu-id="038d5-126">이 cmdlet이 시작 되는 논리 앱 트리거의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="038d5-127">-확인</span><span class="sxs-lookup"><span data-stu-id="038d5-127">-Confirm</span></span>
<span data-ttu-id="038d5-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="038d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="038d5-129">-WhatIf</span></span>
<span data-ttu-id="038d5-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="038d5-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="038d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038d5-132">CommonParameters</span></span>
<span data-ttu-id="038d5-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038d5-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038d5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038d5-135">입력</span><span class="sxs-lookup"><span data-stu-id="038d5-135">INPUTS</span></span>

### <span data-ttu-id="038d5-136">않아야</span><span class="sxs-lookup"><span data-stu-id="038d5-136">None</span></span>
<span data-ttu-id="038d5-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="038d5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="038d5-138">출력</span><span class="sxs-lookup"><span data-stu-id="038d5-138">OUTPUTS</span></span>

### <span data-ttu-id="038d5-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="038d5-139">System.Object</span></span>

## <span data-ttu-id="038d5-140">상속자</span><span class="sxs-lookup"><span data-stu-id="038d5-140">NOTES</span></span>

## <span data-ttu-id="038d5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="038d5-141">RELATED LINKS</span></span>

[<span data-ttu-id="038d5-142">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="038d5-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="038d5-143">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="038d5-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="038d5-144">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="038d5-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="038d5-145">제거-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="038d5-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="038d5-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="038d5-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="038d5-147">중지-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="038d5-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


