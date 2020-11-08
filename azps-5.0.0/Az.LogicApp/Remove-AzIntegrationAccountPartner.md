---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218959"
---
# <span data-ttu-id="c8877-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c8877-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="c8877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8877-102">SYNOPSIS</span></span>
<span data-ttu-id="c8877-103">통합 계정 파트너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="c8877-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8877-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8877-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8877-105">DESCRIPTION</span></span>
<span data-ttu-id="c8877-106">**AzIntegrationAccountPartner** cmdlet은 리소스 그룹에서 통합 계정 파트너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="c8877-107">통합 계정 이름, 리소스 그룹 이름, 파트너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="c8877-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c8877-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c8877-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c8877-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c8877-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c8877-112">EXAMPLES</span></span>

### <span data-ttu-id="c8877-113">예제 1: 통합 계정 파트너 제거</span><span class="sxs-lookup"><span data-stu-id="c8877-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="c8877-114">이 명령은 IntegrationAccountPartner1 이라는 통합 계정 파트너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="c8877-115">변수</span><span class="sxs-lookup"><span data-stu-id="c8877-115">PARAMETERS</span></span>

### <span data-ttu-id="c8877-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8877-116">-DefaultProfile</span></span>
<span data-ttu-id="c8877-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c8877-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8877-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c8877-118">-Force</span></span>
<span data-ttu-id="c8877-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8877-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c8877-120">-Name</span></span>
<span data-ttu-id="c8877-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c8877-122">-(이름)</span><span class="sxs-lookup"><span data-stu-id="c8877-122">-PartnerName</span></span>
<span data-ttu-id="c8877-123">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="c8877-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8877-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8877-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c8877-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c8877-126">-Confirm</span></span>
<span data-ttu-id="c8877-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8877-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8877-128">-WhatIf</span></span>
<span data-ttu-id="c8877-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8877-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8877-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8877-131">CommonParameters</span></span>
<span data-ttu-id="c8877-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8877-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8877-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8877-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8877-134">입력</span><span class="sxs-lookup"><span data-stu-id="c8877-134">INPUTS</span></span>

### <span data-ttu-id="c8877-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c8877-135">System.String</span></span>

## <span data-ttu-id="c8877-136">출력</span><span class="sxs-lookup"><span data-stu-id="c8877-136">OUTPUTS</span></span>

### <span data-ttu-id="c8877-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="c8877-137">System.Void</span></span>

## <span data-ttu-id="c8877-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c8877-138">NOTES</span></span>

## <span data-ttu-id="c8877-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8877-139">RELATED LINKS</span></span>

[<span data-ttu-id="c8877-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c8877-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="c8877-141">새로운 AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c8877-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="c8877-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="c8877-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


