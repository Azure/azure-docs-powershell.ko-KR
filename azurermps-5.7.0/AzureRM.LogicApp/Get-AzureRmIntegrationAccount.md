---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: ee96c446ee0517363535b09ee320e04db7aeba38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532803"
---
# <span data-ttu-id="5d791-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5d791-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="5d791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d791-102">SYNOPSIS</span></span>
<span data-ttu-id="5d791-103">통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d791-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d791-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d791-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d791-105">DESCRIPTION</span></span>
<span data-ttu-id="5d791-106">**Get-AzureRmIntegrationAccount** cmdlet은 리소스 그룹에서 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="5d791-107">통합 계정 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="5d791-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5d791-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5d791-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5d791-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5d791-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5d791-112">EXAMPLES</span></span>

### <span data-ttu-id="5d791-113">예제 1: 이름으로 통합 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d791-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="5d791-114">이 명령은 지정 된 리소스 그룹에서 IntegrationAccount31 이라는 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="5d791-115">예제 2: 리소스 그룹의 통합 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d791-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="5d791-116">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="5d791-117">예제 3: 모든 통합 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d791-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="5d791-118">이 명령은 Azure 구독에 있는 모든 통합 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="5d791-119">변수</span><span class="sxs-lookup"><span data-stu-id="5d791-119">PARAMETERS</span></span>

### <span data-ttu-id="5d791-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d791-120">-DefaultProfile</span></span>
<span data-ttu-id="5d791-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d791-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d791-122">-이름</span><span class="sxs-lookup"><span data-stu-id="5d791-122">-Name</span></span>
<span data-ttu-id="5d791-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d791-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d791-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d791-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d791-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d791-126">CommonParameters</span></span>
<span data-ttu-id="5d791-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d791-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d791-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d791-129">입력</span><span class="sxs-lookup"><span data-stu-id="5d791-129">INPUTS</span></span>

### <span data-ttu-id="5d791-130">않아야</span><span class="sxs-lookup"><span data-stu-id="5d791-130">None</span></span>
<span data-ttu-id="5d791-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d791-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d791-132">출력</span><span class="sxs-lookup"><span data-stu-id="5d791-132">OUTPUTS</span></span>

### <span data-ttu-id="5d791-133">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="5d791-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="5d791-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5d791-134">NOTES</span></span>

## <span data-ttu-id="5d791-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d791-135">RELATED LINKS</span></span>

[<span data-ttu-id="5d791-136">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="5d791-136">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="5d791-137">새로운 AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5d791-137">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="5d791-138">제거-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5d791-138">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="5d791-139">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5d791-139">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


