---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: f56878ac2aa2f625b5583805150fd16368d9f718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535856"
---
# <span data-ttu-id="b4997-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b4997-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="b4997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4997-102">SYNOPSIS</span></span>
<span data-ttu-id="b4997-103">통합 계정 맵을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4997-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4997-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4997-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4997-105">DESCRIPTION</span></span>
<span data-ttu-id="b4997-106">**Get-AzureRmIntegrationAccountMap** cmdlet은 리소스 그룹에서 통합 계정 맵을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="b4997-107">통합 계정 이름, 리소스 그룹 이름 및 지도 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="b4997-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b4997-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b4997-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b4997-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b4997-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b4997-112">EXAMPLES</span></span>

### <span data-ttu-id="b4997-113">예제 1: 통합 계정 맵 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4997-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="b4997-114">이 명령은 지정 된 리소스 그룹의 IntegrationAccountMap47 이라는 통합 계정 맵을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="b4997-115">예제 2: 통합 계정 이름을 기준으로 통합 거래처 지도 가져오기</span><span class="sxs-lookup"><span data-stu-id="b4997-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="b4997-116">이 명령은 통합 계정 이름과 통합 계정 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="b4997-117">변수</span><span class="sxs-lookup"><span data-stu-id="b4997-117">PARAMETERS</span></span>

### <span data-ttu-id="b4997-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4997-118">-DefaultProfile</span></span>
<span data-ttu-id="b4997-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4997-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4997-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="b4997-120">-MapName</span></span>
<span data-ttu-id="b4997-121">통합 계정 맵의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="b4997-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b4997-122">-Name</span></span>
<span data-ttu-id="b4997-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="b4997-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4997-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4997-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4997-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4997-126">CommonParameters</span></span>
<span data-ttu-id="b4997-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4997-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4997-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4997-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4997-129">입력</span><span class="sxs-lookup"><span data-stu-id="b4997-129">INPUTS</span></span>

### <span data-ttu-id="b4997-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4997-130">System.String</span></span>

## <span data-ttu-id="b4997-131">출력</span><span class="sxs-lookup"><span data-stu-id="b4997-131">OUTPUTS</span></span>

### <span data-ttu-id="b4997-132">IntegrationAccountMap를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="b4997-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b4997-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b4997-133">NOTES</span></span>

## <span data-ttu-id="b4997-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4997-134">RELATED LINKS</span></span>

[<span data-ttu-id="b4997-135">새로운 AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b4997-135">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b4997-136">제거-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b4997-136">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b4997-137">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b4997-137">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


