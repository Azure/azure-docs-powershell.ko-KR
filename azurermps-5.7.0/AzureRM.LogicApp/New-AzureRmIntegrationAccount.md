---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 44dc417521b49d47b9c060b987c82ddd06b7f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528115"
---
# <span data-ttu-id="1a4e5-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1a4e5-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="1a4e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4e5-103">통합 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a4e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a4e5-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a4e5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1a4e5-105">DESCRIPTION</span></span>
<span data-ttu-id="1a4e5-106">**새 AzureRmIntegrationAccount** cmdlet은 통합 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="1a4e5-107">이 cmdlet은 통합 계정을 나타내는 개체를 반환 합니다. 이름, 위치, 리소스 그룹 이름 및 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="1a4e5-108">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="1a4e5-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1a4e5-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1a4e5-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1a4e5-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1a4e5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="1a4e5-113">EXAMPLES</span></span>

### <span data-ttu-id="1a4e5-114">예제 1: 통합 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="1a4e5-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1a4e5-115">이 명령은 지정 된 리소스 그룹에 IntegrationAccount31 이라는 통합 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="1a4e5-116">변수</span><span class="sxs-lookup"><span data-stu-id="1a4e5-116">PARAMETERS</span></span>

### <span data-ttu-id="1a4e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4e5-117">-DefaultProfile</span></span>
<span data-ttu-id="1a4e5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1a4e5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a4e5-119">-위치</span><span class="sxs-lookup"><span data-stu-id="1a4e5-119">-Location</span></span>
<span data-ttu-id="1a4e5-120">통합 계정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-120">Specifies a location for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4e5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1a4e5-121">-Name</span></span>
<span data-ttu-id="1a4e5-122">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-122">Specifies a name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a4e5-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a4e5-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="1a4e5-125">-Sku</span></span>
<span data-ttu-id="1a4e5-126">통합 계정에 대 한 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="1a4e5-127">-확인</span><span class="sxs-lookup"><span data-stu-id="1a4e5-127">-Confirm</span></span>
<span data-ttu-id="1a4e5-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a4e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a4e5-129">-WhatIf</span></span>
<span data-ttu-id="1a4e5-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a4e5-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a4e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4e5-132">CommonParameters</span></span>
<span data-ttu-id="1a4e5-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4e5-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a4e5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4e5-135">입력</span><span class="sxs-lookup"><span data-stu-id="1a4e5-135">INPUTS</span></span>

### <span data-ttu-id="1a4e5-136">않아야</span><span class="sxs-lookup"><span data-stu-id="1a4e5-136">None</span></span>
<span data-ttu-id="1a4e5-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a4e5-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a4e5-138">출력</span><span class="sxs-lookup"><span data-stu-id="1a4e5-138">OUTPUTS</span></span>

### <span data-ttu-id="1a4e5-139">IntegrationAccount를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="1a4e5-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="1a4e5-140">상속자</span><span class="sxs-lookup"><span data-stu-id="1a4e5-140">NOTES</span></span>

## <span data-ttu-id="1a4e5-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a4e5-141">RELATED LINKS</span></span>

[<span data-ttu-id="1a4e5-142">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1a4e5-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="1a4e5-143">제거-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1a4e5-143">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="1a4e5-144">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1a4e5-144">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


