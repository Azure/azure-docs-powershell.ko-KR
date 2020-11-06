---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: c6c2c356557d2d9d40a4012a7deee5aec0e73aa4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538139"
---
# <span data-ttu-id="baeff-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="baeff-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="baeff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baeff-102">SYNOPSIS</span></span>
<span data-ttu-id="baeff-103">논리 앱의 실행을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baeff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="baeff-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baeff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="baeff-105">DESCRIPTION</span></span>
<span data-ttu-id="baeff-106">**AzureRmLogicAppRun** cmdlet은 논리 앱의 실행을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="baeff-107">논리 앱, 리소스 그룹 및 실행을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="baeff-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="baeff-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="baeff-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="baeff-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="baeff-112">예제의</span><span class="sxs-lookup"><span data-stu-id="baeff-112">EXAMPLES</span></span>

### <span data-ttu-id="baeff-113">예제 1: 논리 앱 실행 취소</span><span class="sxs-lookup"><span data-stu-id="baeff-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="baeff-114">이 명령은 LogicApp03 이라는 논리 앱의 실행을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="baeff-115">변수</span><span class="sxs-lookup"><span data-stu-id="baeff-115">PARAMETERS</span></span>

### <span data-ttu-id="baeff-116">-Force</span><span class="sxs-lookup"><span data-stu-id="baeff-116">-Force</span></span>
<span data-ttu-id="baeff-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="baeff-118">-이름</span><span class="sxs-lookup"><span data-stu-id="baeff-118">-Name</span></span>
<span data-ttu-id="baeff-119">이 cmdlet이 실행을 취소 하는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-119">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="baeff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baeff-120">-ResourceGroupName</span></span>
<span data-ttu-id="baeff-121">이 cmdlet이 실행을 취소 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-121">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="baeff-122">-RunName</span><span class="sxs-lookup"><span data-stu-id="baeff-122">-RunName</span></span>
<span data-ttu-id="baeff-123">이 cmdlet이 취소 하는 논리 앱 실행의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-123">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="baeff-124">-확인</span><span class="sxs-lookup"><span data-stu-id="baeff-124">-Confirm</span></span>
<span data-ttu-id="baeff-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baeff-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baeff-126">-WhatIf</span></span>
<span data-ttu-id="baeff-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baeff-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baeff-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baeff-129">-DefaultProfile</span></span>
<span data-ttu-id="baeff-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baeff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baeff-131">CommonParameters</span></span>
<span data-ttu-id="baeff-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="baeff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baeff-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baeff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baeff-134">입력</span><span class="sxs-lookup"><span data-stu-id="baeff-134">INPUTS</span></span>

## <span data-ttu-id="baeff-135">출력</span><span class="sxs-lookup"><span data-stu-id="baeff-135">OUTPUTS</span></span>

### <span data-ttu-id="baeff-136">System. 개체</span><span class="sxs-lookup"><span data-stu-id="baeff-136">System.Object</span></span>

## <span data-ttu-id="baeff-137">상속자</span><span class="sxs-lookup"><span data-stu-id="baeff-137">NOTES</span></span>

## <span data-ttu-id="baeff-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="baeff-138">RELATED LINKS</span></span>

[<span data-ttu-id="baeff-139">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="baeff-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


