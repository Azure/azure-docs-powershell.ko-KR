---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495288"
---
# <span data-ttu-id="17eb7-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17eb7-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="17eb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="17eb7-103">통합 계정 파트너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-103">Gets integration account partners.</span></span>

## <span data-ttu-id="17eb7-104">구문</span><span class="sxs-lookup"><span data-stu-id="17eb7-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17eb7-105">설명</span><span class="sxs-lookup"><span data-stu-id="17eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="17eb7-106">**Get-AzIntegrationAccountPartner** cmdlet은 리소스 그룹에서 통합 계정 파트너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="17eb7-107">통합 계정 이름, 리소스 그룹 이름 및 파트너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="17eb7-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="17eb7-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="17eb7-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="17eb7-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="17eb7-112">예제</span><span class="sxs-lookup"><span data-stu-id="17eb7-112">EXAMPLES</span></span>

### <span data-ttu-id="17eb7-113">예제 1: 통합 계정 파트너 얻기</span><span class="sxs-lookup"><span data-stu-id="17eb7-113">Example 1: Get an integration account partner</span></span>
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

<span data-ttu-id="17eb7-114">이 명령은 IntegrationAccountPartner22라는 통합 계정 파트너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="17eb7-115">예제 2: 통합 계정 이름을 사용하여 통합 계정 파트너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-115">Example 2: Get an integration account partners by using an integration account name</span></span>
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

<span data-ttu-id="17eb7-116">이 명령은 IntegrationAccount31이라는 통합 계정에 대한 통합 계정 파트너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="17eb7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17eb7-117">PARAMETERS</span></span>

### <span data-ttu-id="17eb7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17eb7-118">-DefaultProfile</span></span>
<span data-ttu-id="17eb7-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17eb7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17eb7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="17eb7-120">-Name</span></span>
<span data-ttu-id="17eb7-121">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="17eb7-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="17eb7-122">-PartnerName</span></span>
<span data-ttu-id="17eb7-123">통합 계정 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="17eb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17eb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="17eb7-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="17eb7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17eb7-126">CommonParameters</span></span>
<span data-ttu-id="17eb7-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17eb7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17eb7-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="17eb7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17eb7-129">입력</span><span class="sxs-lookup"><span data-stu-id="17eb7-129">INPUTS</span></span>

### <span data-ttu-id="17eb7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="17eb7-130">System.String</span></span>

## <span data-ttu-id="17eb7-131">출력</span><span class="sxs-lookup"><span data-stu-id="17eb7-131">OUTPUTS</span></span>

### <span data-ttu-id="17eb7-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17eb7-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="17eb7-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17eb7-133">NOTES</span></span>

## <span data-ttu-id="17eb7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17eb7-134">RELATED LINKS</span></span>

[<span data-ttu-id="17eb7-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17eb7-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="17eb7-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17eb7-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="17eb7-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="17eb7-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


