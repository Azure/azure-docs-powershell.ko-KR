---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: c1f96d462d1556078159d70a47a9869ec21a0e63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689539"
---
# <span data-ttu-id="448fa-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="448fa-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="448fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="448fa-102">SYNOPSIS</span></span>
<span data-ttu-id="448fa-103">통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-103">Gets integration account partners.</span></span>

## <span data-ttu-id="448fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="448fa-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="448fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="448fa-105">DESCRIPTION</span></span>
<span data-ttu-id="448fa-106">**Get-AzIntegrationAccountPartner** cmdlet은 리소스 그룹에서 통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="448fa-107">통합 계정 이름, 리소스 그룹 이름, 파트너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="448fa-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="448fa-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="448fa-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="448fa-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="448fa-112">예제의</span><span class="sxs-lookup"><span data-stu-id="448fa-112">EXAMPLES</span></span>

### <span data-ttu-id="448fa-113">예제 1: 통합 계정 파트너 가져오기</span><span class="sxs-lookup"><span data-stu-id="448fa-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="448fa-114">이 명령은 IntegrationAccountPartner22 이라는 통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="448fa-115">예제 2: 통합 계정 이름을 사용 하 여 통합 계정 파트너 가져오기</span><span class="sxs-lookup"><span data-stu-id="448fa-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="448fa-116">이 명령은 IntegrationAccount31 이라는 통합 계정의 통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="448fa-117">변수</span><span class="sxs-lookup"><span data-stu-id="448fa-117">PARAMETERS</span></span>

### <span data-ttu-id="448fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448fa-118">-DefaultProfile</span></span>
<span data-ttu-id="448fa-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="448fa-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="448fa-120">-이름</span><span class="sxs-lookup"><span data-stu-id="448fa-120">-Name</span></span>
<span data-ttu-id="448fa-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448fa-122">-(이름)</span><span class="sxs-lookup"><span data-stu-id="448fa-122">-PartnerName</span></span>
<span data-ttu-id="448fa-123">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="448fa-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="448fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448fa-126">CommonParameters</span></span>
<span data-ttu-id="448fa-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="448fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448fa-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448fa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448fa-129">입력</span><span class="sxs-lookup"><span data-stu-id="448fa-129">INPUTS</span></span>

### <span data-ttu-id="448fa-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="448fa-130">System.String</span></span>

## <span data-ttu-id="448fa-131">출력</span><span class="sxs-lookup"><span data-stu-id="448fa-131">OUTPUTS</span></span>

### <span data-ttu-id="448fa-132">IntegrationAccountPartner를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="448fa-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="448fa-133">상속자</span><span class="sxs-lookup"><span data-stu-id="448fa-133">NOTES</span></span>

## <span data-ttu-id="448fa-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="448fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="448fa-135">새로운 AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="448fa-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="448fa-136">제거-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="448fa-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="448fa-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="448fa-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)

