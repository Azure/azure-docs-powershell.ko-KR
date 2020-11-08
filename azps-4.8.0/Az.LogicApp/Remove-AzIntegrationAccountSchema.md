---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048201"
---
# <span data-ttu-id="d6f69-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d6f69-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="d6f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f69-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f69-103">통합 계정 스키마를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="d6f69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6f69-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d6f69-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f69-106">**AzIntegrationAccountSchema** cmdlet은 리소스 그룹에서 통합 계정 스키마를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="d6f69-107">통합 계정 이름, 리소스 그룹 이름 및 스키마 이름 지정</span><span class="sxs-lookup"><span data-stu-id="d6f69-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="d6f69-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d6f69-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d6f69-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d6f69-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d6f69-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d6f69-112">EXAMPLES</span></span>

### <span data-ttu-id="d6f69-113">예제 1: 통합 계정 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="d6f69-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="d6f69-114">이 명령은 IntegrationAccountSchema43 이라는 통합 계정 스키마를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="d6f69-115">변수</span><span class="sxs-lookup"><span data-stu-id="d6f69-115">PARAMETERS</span></span>

### <span data-ttu-id="d6f69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f69-116">-DefaultProfile</span></span>
<span data-ttu-id="d6f69-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d6f69-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6f69-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d6f69-118">-Force</span></span>
<span data-ttu-id="d6f69-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d6f69-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d6f69-120">-Name</span></span>
<span data-ttu-id="d6f69-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f69-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f69-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6f69-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d6f69-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d6f69-124">-SchemaName</span></span>
<span data-ttu-id="d6f69-125">통합 계정 스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-125">Specifies the name of an integration account schema.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f69-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d6f69-126">-Confirm</span></span>
<span data-ttu-id="d6f69-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f69-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f69-128">-WhatIf</span></span>
<span data-ttu-id="d6f69-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f69-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f69-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f69-131">CommonParameters</span></span>
<span data-ttu-id="d6f69-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f69-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f69-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f69-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f69-134">입력</span><span class="sxs-lookup"><span data-stu-id="d6f69-134">INPUTS</span></span>

### <span data-ttu-id="d6f69-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6f69-135">System.String</span></span>

## <span data-ttu-id="d6f69-136">출력</span><span class="sxs-lookup"><span data-stu-id="d6f69-136">OUTPUTS</span></span>

### <span data-ttu-id="d6f69-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d6f69-137">System.Void</span></span>

## <span data-ttu-id="d6f69-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d6f69-138">NOTES</span></span>

## <span data-ttu-id="d6f69-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6f69-139">RELATED LINKS</span></span>

[<span data-ttu-id="d6f69-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d6f69-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="d6f69-141">새로운 AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d6f69-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="d6f69-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="d6f69-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


