---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 8ad8714a59ac9f0beb0c070d5f9f89c4fbd20a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532783"
---
# <span data-ttu-id="2cf88-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cf88-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="2cf88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf88-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf88-103">통합 계정 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cf88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2cf88-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2cf88-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf88-106">**Get-AzureRmIntegrationAccountSchema** cmdlet은 통합 계정 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="2cf88-107">통합 계정 이름, 리소스 그룹 이름 및 스키마 이름 지정</span><span class="sxs-lookup"><span data-stu-id="2cf88-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="2cf88-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2cf88-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2cf88-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2cf88-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2cf88-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2cf88-112">EXAMPLES</span></span>

### <span data-ttu-id="2cf88-113">예제 1: 통합 계정 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="2cf88-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="2cf88-114">이 명령은 IntegrationAccountSchema43 이라는 통합 계정 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="2cf88-115">예제 2: 리소스 그룹에 대 한 통합 계정 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="2cf88-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="2cf88-116">이 명령은 ResourceGroup11 이라는 리소스 그룹에 대 한 통합 계정 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2cf88-117">변수</span><span class="sxs-lookup"><span data-stu-id="2cf88-117">PARAMETERS</span></span>

### <span data-ttu-id="2cf88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf88-118">-DefaultProfile</span></span>
<span data-ttu-id="2cf88-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2cf88-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cf88-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2cf88-120">-Name</span></span>
<span data-ttu-id="2cf88-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="2cf88-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf88-122">-ResourceGroupName</span></span>
<span data-ttu-id="2cf88-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2cf88-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2cf88-124">-SchemaName</span></span>
<span data-ttu-id="2cf88-125">통합 계정 스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="2cf88-126">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="2cf88-127">.</span><span class="sxs-lookup"><span data-stu-id="2cf88-127">.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cf88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf88-128">CommonParameters</span></span>
<span data-ttu-id="2cf88-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf88-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf88-131">입력</span><span class="sxs-lookup"><span data-stu-id="2cf88-131">INPUTS</span></span>

### <span data-ttu-id="2cf88-132">않아야</span><span class="sxs-lookup"><span data-stu-id="2cf88-132">None</span></span>
<span data-ttu-id="2cf88-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2cf88-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2cf88-134">출력</span><span class="sxs-lookup"><span data-stu-id="2cf88-134">OUTPUTS</span></span>

### <span data-ttu-id="2cf88-135">IntegrationAccountSchema를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="2cf88-135">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="2cf88-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2cf88-136">NOTES</span></span>

## <span data-ttu-id="2cf88-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cf88-137">RELATED LINKS</span></span>

[<span data-ttu-id="2cf88-138">새로운 AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cf88-138">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="2cf88-139">제거-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cf88-139">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="2cf88-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cf88-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


