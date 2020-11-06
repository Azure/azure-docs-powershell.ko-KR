---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: c74f4f89337d8fee4e6739cb145e9d2da0d4b81c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527499"
---
# <span data-ttu-id="d1543-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d1543-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="d1543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1543-102">SYNOPSIS</span></span>
<span data-ttu-id="d1543-103">통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1543-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1543-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1543-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1543-105">DESCRIPTION</span></span>
<span data-ttu-id="d1543-106">**Get-AzureRmIntegrationAccountPartner** cmdlet은 리소스 그룹에서 통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="d1543-107">통합 계정 이름, 리소스 그룹 이름, 파트너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="d1543-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d1543-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d1543-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d1543-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d1543-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d1543-112">EXAMPLES</span></span>

### <span data-ttu-id="d1543-113">예제 1: 통합 계정 파트너 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1543-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="d1543-114">이 명령은 IntegrationAccountPartner22 이라는 통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="d1543-115">예제 2: 통합 계정 이름을 사용 하 여 통합 계정 파트너 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1543-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="d1543-116">이 명령은 IntegrationAccount31 이라는 통합 계정의 통합 계정 파트너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="d1543-117">변수</span><span class="sxs-lookup"><span data-stu-id="d1543-117">PARAMETERS</span></span>

### <span data-ttu-id="d1543-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d1543-118">-Name</span></span>
<span data-ttu-id="d1543-119">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d1543-120">-(이름)</span><span class="sxs-lookup"><span data-stu-id="d1543-120">-PartnerName</span></span>
<span data-ttu-id="d1543-121">통합 계정 파트너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="d1543-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1543-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1543-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d1543-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1543-124">-DefaultProfile</span></span>
<span data-ttu-id="d1543-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1543-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1543-126">CommonParameters</span></span>
<span data-ttu-id="d1543-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1543-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1543-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1543-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1543-129">입력</span><span class="sxs-lookup"><span data-stu-id="d1543-129">INPUTS</span></span>

## <span data-ttu-id="d1543-130">출력</span><span class="sxs-lookup"><span data-stu-id="d1543-130">OUTPUTS</span></span>

### <span data-ttu-id="d1543-131">IntegrationAccountPartner를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="d1543-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="d1543-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d1543-132">NOTES</span></span>

## <span data-ttu-id="d1543-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1543-133">RELATED LINKS</span></span>

[<span data-ttu-id="d1543-134">새로운 AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d1543-134">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="d1543-135">제거-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d1543-135">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="d1543-136">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d1543-136">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


