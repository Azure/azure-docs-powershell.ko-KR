---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329216"
---
# <span data-ttu-id="b9dbe-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b9dbe-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="b9dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="b9dbe-103">통합 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-103">Gets integration accounts.</span></span>

## <span data-ttu-id="b9dbe-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9dbe-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9dbe-105">설명</span><span class="sxs-lookup"><span data-stu-id="b9dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="b9dbe-106">**Get-AzIntegrationAccount** cmdlet은 리소스 그룹에서 통합 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="b9dbe-107">통합 계정 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="b9dbe-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b9dbe-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b9dbe-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b9dbe-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b9dbe-112">예제</span><span class="sxs-lookup"><span data-stu-id="b9dbe-112">EXAMPLES</span></span>

### <span data-ttu-id="b9dbe-113">예제 1: 이름으로 통합 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="b9dbe-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="b9dbe-114">이 명령은 지정된 리소스 그룹에서 IntegrationAccount31이라는 통합 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="b9dbe-115">예제 2: 리소스 그룹에서 통합 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="b9dbe-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="b9dbe-116">이 명령은 ResourceGroup11이라는 리소스 그룹에서 통합 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="b9dbe-117">예제 3: 모든 통합 계정 얻기</span><span class="sxs-lookup"><span data-stu-id="b9dbe-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="b9dbe-118">이 명령은 Azure 구독의 모든 통합 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="b9dbe-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9dbe-119">PARAMETERS</span></span>

### <span data-ttu-id="b9dbe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9dbe-120">-DefaultProfile</span></span>
<span data-ttu-id="b9dbe-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b9dbe-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9dbe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b9dbe-122">-Name</span></span>
<span data-ttu-id="b9dbe-123">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b9dbe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9dbe-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9dbe-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b9dbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9dbe-126">CommonParameters</span></span>
<span data-ttu-id="b9dbe-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9dbe-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b9dbe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9dbe-129">입력</span><span class="sxs-lookup"><span data-stu-id="b9dbe-129">INPUTS</span></span>

### <span data-ttu-id="b9dbe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b9dbe-130">System.String</span></span>

## <span data-ttu-id="b9dbe-131">출력</span><span class="sxs-lookup"><span data-stu-id="b9dbe-131">OUTPUTS</span></span>

### <span data-ttu-id="b9dbe-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b9dbe-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="b9dbe-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9dbe-133">NOTES</span></span>

## <span data-ttu-id="b9dbe-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9dbe-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9dbe-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b9dbe-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="b9dbe-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b9dbe-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="b9dbe-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b9dbe-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="b9dbe-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b9dbe-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


