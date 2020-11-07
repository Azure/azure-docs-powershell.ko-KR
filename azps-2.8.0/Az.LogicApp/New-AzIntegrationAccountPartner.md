---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: fe54643e3425d495a78d6a925f9518d965b77d77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689510"
---
# <span data-ttu-id="73c64-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="73c64-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="73c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c64-102">SYNOPSIS</span></span>
<span data-ttu-id="73c64-103">통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="73c64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73c64-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73c64-105">DESCRIPTION</span></span>
<span data-ttu-id="73c64-106">**새 AzIntegrationAccountPartner** cmdlet은 통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="73c64-107">이 cmdlet은 통합 계정 파트너를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="73c64-108">통합 계정 이름, 리소스 그룹 이름, 파트너 이름, 파트너 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="73c64-109">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="73c64-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73c64-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73c64-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73c64-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73c64-114">예제의</span><span class="sxs-lookup"><span data-stu-id="73c64-114">EXAMPLES</span></span>

### <span data-ttu-id="73c64-115">예제 1: 통합 계정 파트너 만들기</span><span class="sxs-lookup"><span data-stu-id="73c64-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="73c64-116">이 명령은 지정 된 리소스 그룹에 IntegrationAccountPartner22 이라는 통합 계정 파트너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="73c64-117">변수</span><span class="sxs-lookup"><span data-stu-id="73c64-117">PARAMETERS</span></span>

### <span data-ttu-id="73c64-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="73c64-118">-BusinessIdentities</span></span>
<span data-ttu-id="73c64-119">통합 계정 파트너에 대 한 비즈니스 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="73c64-120">해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c64-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c64-121">-DefaultProfile</span></span>
<span data-ttu-id="73c64-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="73c64-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73c64-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="73c64-123">-Metadata</span></span>
<span data-ttu-id="73c64-124">파트너에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="73c64-125">-이름</span><span class="sxs-lookup"><span data-stu-id="73c64-125">-Name</span></span>
<span data-ttu-id="73c64-126">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="73c64-127">-(이름)</span><span class="sxs-lookup"><span data-stu-id="73c64-127">-PartnerName</span></span>
<span data-ttu-id="73c64-128">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="73c64-129">-용 유형</span><span class="sxs-lookup"><span data-stu-id="73c64-129">-PartnerType</span></span>
<span data-ttu-id="73c64-130">통합 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="73c64-131">이 매개 변수는 B2B 유형을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-131">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="73c64-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c64-132">-ResourceGroupName</span></span>
<span data-ttu-id="73c64-133">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73c64-134">-확인</span><span class="sxs-lookup"><span data-stu-id="73c64-134">-Confirm</span></span>
<span data-ttu-id="73c64-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c64-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c64-136">-WhatIf</span></span>
<span data-ttu-id="73c64-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c64-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c64-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c64-139">CommonParameters</span></span>
<span data-ttu-id="73c64-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73c64-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c64-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c64-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c64-142">입력</span><span class="sxs-lookup"><span data-stu-id="73c64-142">INPUTS</span></span>

### <span data-ttu-id="73c64-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73c64-143">System.String</span></span>

## <span data-ttu-id="73c64-144">출력</span><span class="sxs-lookup"><span data-stu-id="73c64-144">OUTPUTS</span></span>

### <span data-ttu-id="73c64-145">IntegrationAccountPartner를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="73c64-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="73c64-146">상속자</span><span class="sxs-lookup"><span data-stu-id="73c64-146">NOTES</span></span>

## <span data-ttu-id="73c64-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73c64-147">RELATED LINKS</span></span>

[<span data-ttu-id="73c64-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="73c64-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="73c64-149">제거-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="73c64-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="73c64-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="73c64-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


