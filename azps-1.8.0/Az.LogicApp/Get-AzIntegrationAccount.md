---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: bf57ffe0823ced37eaf58e9321c4330002c9be48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867774"
---
# <span data-ttu-id="31141-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="31141-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="31141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31141-102">SYNOPSIS</span></span>
<span data-ttu-id="31141-103">통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31141-103">Gets integration accounts.</span></span>

## <span data-ttu-id="31141-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31141-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31141-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31141-105">DESCRIPTION</span></span>
<span data-ttu-id="31141-106">**Get-AzIntegrationAccount** cmdlet은 리소스 그룹에서 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31141-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="31141-107">통합 계정 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="31141-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="31141-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="31141-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="31141-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="31141-112">예제의</span><span class="sxs-lookup"><span data-stu-id="31141-112">EXAMPLES</span></span>

### <span data-ttu-id="31141-113">예제 1: 이름으로 통합 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="31141-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="31141-114">이 명령은 지정 된 리소스 그룹에서 IntegrationAccount31 이라는 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31141-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="31141-115">예제 2: 리소스 그룹의 통합 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="31141-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="31141-116">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31141-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="31141-117">예제 3: 모든 통합 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="31141-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="31141-118">이 명령은 Azure 구독에 있는 모든 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31141-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="31141-119">변수</span><span class="sxs-lookup"><span data-stu-id="31141-119">PARAMETERS</span></span>

### <span data-ttu-id="31141-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31141-120">-DefaultProfile</span></span>
<span data-ttu-id="31141-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31141-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31141-122">-이름</span><span class="sxs-lookup"><span data-stu-id="31141-122">-Name</span></span>
<span data-ttu-id="31141-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="31141-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31141-124">-ResourceGroupName</span></span>
<span data-ttu-id="31141-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="31141-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31141-126">CommonParameters</span></span>
<span data-ttu-id="31141-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31141-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31141-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31141-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31141-129">입력</span><span class="sxs-lookup"><span data-stu-id="31141-129">INPUTS</span></span>

### <span data-ttu-id="31141-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31141-130">System.String</span></span>

## <span data-ttu-id="31141-131">출력</span><span class="sxs-lookup"><span data-stu-id="31141-131">OUTPUTS</span></span>

### <span data-ttu-id="31141-132">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="31141-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="31141-133">상속자</span><span class="sxs-lookup"><span data-stu-id="31141-133">NOTES</span></span>

## <span data-ttu-id="31141-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31141-134">RELATED LINKS</span></span>

[<span data-ttu-id="31141-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="31141-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="31141-136">새로운 AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="31141-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="31141-137">제거-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="31141-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="31141-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="31141-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


