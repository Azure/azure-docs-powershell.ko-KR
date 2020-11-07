---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ae9b9f37a20f63a502da2904fd6d94f8a6aa281f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867602"
---
# <span data-ttu-id="b01d8-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b01d8-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="b01d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b01d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b01d8-103">통합 계정 파트너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="b01d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b01d8-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b01d8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b01d8-105">DESCRIPTION</span></span>
<span data-ttu-id="b01d8-106">**Set-AzIntegrationAccountPartner** cmdlet은 통합 계정 파트너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="b01d8-107">이 cmdlet은 통합 계정 파트너를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="b01d8-108">통합 계정 이름, 리소스 그룹 이름, 파트너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="b01d8-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b01d8-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b01d8-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b01d8-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b01d8-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b01d8-113">EXAMPLES</span></span>

### <span data-ttu-id="b01d8-114">예제 1: 통합 계정 파트너 수정</span><span class="sxs-lookup"><span data-stu-id="b01d8-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="b01d8-115">이 명령은 지정 된 리소스 그룹에서 IntegrationAccountPartner22 이라는 통합 계정 파트너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="b01d8-116">변수</span><span class="sxs-lookup"><span data-stu-id="b01d8-116">PARAMETERS</span></span>

### <span data-ttu-id="b01d8-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="b01d8-117">-BusinessIdentities</span></span>
<span data-ttu-id="b01d8-118">통합 계정 파트너에 대 한 비즈니스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="b01d8-119">해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-119">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01d8-120">-DefaultProfile</span></span>
<span data-ttu-id="b01d8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b01d8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b01d8-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b01d8-122">-Force</span></span>
<span data-ttu-id="b01d8-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b01d8-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b01d8-124">-Metadata</span></span>
<span data-ttu-id="b01d8-125">파트너에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-125">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d8-126">-이름</span><span class="sxs-lookup"><span data-stu-id="b01d8-126">-Name</span></span>
<span data-ttu-id="b01d8-127">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-127">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b01d8-128">-(이름)</span><span class="sxs-lookup"><span data-stu-id="b01d8-128">-PartnerName</span></span>
<span data-ttu-id="b01d8-129">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="b01d8-130">-용 유형</span><span class="sxs-lookup"><span data-stu-id="b01d8-130">-PartnerType</span></span>
<span data-ttu-id="b01d8-131">통합 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="b01d8-132">이 매개 변수는 B2B 유형을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-132">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b01d8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b01d8-133">-ResourceGroupName</span></span>
<span data-ttu-id="b01d8-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b01d8-135">-확인</span><span class="sxs-lookup"><span data-stu-id="b01d8-135">-Confirm</span></span>
<span data-ttu-id="b01d8-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b01d8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b01d8-137">-WhatIf</span></span>
<span data-ttu-id="b01d8-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b01d8-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b01d8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01d8-140">CommonParameters</span></span>
<span data-ttu-id="b01d8-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b01d8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01d8-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01d8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01d8-143">입력</span><span class="sxs-lookup"><span data-stu-id="b01d8-143">INPUTS</span></span>

### <span data-ttu-id="b01d8-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b01d8-144">System.String</span></span>

## <span data-ttu-id="b01d8-145">출력</span><span class="sxs-lookup"><span data-stu-id="b01d8-145">OUTPUTS</span></span>

### <span data-ttu-id="b01d8-146">IntegrationAccountPartner를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="b01d8-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="b01d8-147">상속자</span><span class="sxs-lookup"><span data-stu-id="b01d8-147">NOTES</span></span>

## <span data-ttu-id="b01d8-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b01d8-148">RELATED LINKS</span></span>

[<span data-ttu-id="b01d8-149">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b01d8-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b01d8-150">새로운 AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b01d8-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b01d8-151">제거-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b01d8-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


